# Long-Term Future Frame Prediction

We experiment with the use of latent variables for future frame prediction. Done at the LTS4 laboratory under Beril Besbinar. Details can be found in the attached report.

# Contents
------------
  * [Requirements](#requirements)
  * [Brief Project Structure](#brief-project-structure)
  * [Usage](#usage)
  * [Results](#results)
    * [Long-Term Prediction](#long-term-prediction)
    * [Out of Domain Runs (1 input object)](#out-of-domain-runs-1-input-object)
    * [Out of Domain Runs (3 input objects)](#out-of-domain-runs-3-input-objects)
    * [Generation Diversity](#generation-diversity)

# Requirements
------------
What we used to run the experiments

  * Python 2.7.3
  * Tensorflow 1.3.0
  * Ubuntu 14.04
  * NVIDIA GTX 780M

# Brief Project Structure
------------

    ├── models                         : Directory containing the scripts and pre-trained models
    │   ├── moving-mnist  
    │       ├── sample-train.ipynb     : Script to train
    │       ├── sample-test.ipynb      : Script to reproduce results
    │       ├── model.ckpt             : Tensorflow pre-trained model
    |
    ├── datasets                       : Directory the scripts to generate the dataset
    │   ├── gen-moving-mnist.ipynb     : Script to generate the moving-mnist dataset
    |
    ├── results                        : Directory containing all results in .gif format
    │   ├── moving-mnist
    │       ├── 2                      : Directory containing long-term prediction results for the moving-mnist with 2 digits
    |
    ├── others                         : Directory containing all other experiments (same structure as models)
    ├── Report.pdf                     : Report in pdf
    ├── README.md                      : The README guideline and explanation for our project.
    |

# Usage
------------

#### Testing
Launch `models\moving-mnist\sample-test.ipynb` 

#### Training
The training dataset was too large to be uploaded to github (~2GB). To train, run `datasets\gen-moving-mnist.ipynb` with the default main arguments to generate the dataset. Then run `models\moving-mnist\sample-train.ipynb`. Note that the saved model `model.ckpt` will be overwritten.

# Results
------------
## Long-Term Prediction

Reconstruction results for 2 input objects. The sequence is 200 frames long and both models received the ground truth as input for the first 20 frames. **Top: Ground Truth, Middle: RNN, Bottom: VRNN**

![Alt Text](/results/moving-shapes/2/0-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/1-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/2-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/3-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/4-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/5-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/6-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/7-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/8-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/9-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/10-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/11-2-shapes.gif) ![Alt Text](/results/moving-shapes/2/12-2-shapes.gif)

![Alt Text](/results/moving-mnist/2/0-2-digits.gif) ![Alt Text](/results/moving-mnist/2/1-2-digits.gif) ![Alt Text](/results/moving-mnist/2/2-2-digits.gif) ![Alt Text](/results/moving-mnist/2/3-2-digits.gif) ![Alt Text](/results/moving-mnist/2/4-2-digits.gif) ![Alt Text](/results/moving-mnist/2/5-2-digits.gif) ![Alt Text](/results/moving-mnist/2/6-2-digits.gif) ![Alt Text](/results/moving-mnist/2/7-2-digits.gif) ![Alt Text](/results/moving-mnist/2/8-2-digits.gif) ![Alt Text](/results/moving-mnist/2/9-2-digits.gif) ![Alt Text](/results/moving-mnist/2/10-2-digits.gif) ![Alt Text](/results/moving-mnist/2/11-2-digits.gif) ![Alt Text](/results/moving-mnist/2/12-2-digits.gif)

## Out of Domain Runs (1 input object)

Out of domain runs with 3 input objects. The sequence is 40 frames long and both models received the ground truth as input for the first 20 frames. **Top: Ground Truth, Middle: RNN, Bottom: VRNN**

![Alt Text](/results/moving-shapes/1/0-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/1-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/2-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/3-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/4-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/5-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/6-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/7-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/8-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/9-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/10-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/11-1-shapes.gif) ![Alt Text](/results/moving-shapes/1/12-1-shapes.gif)

![Alt Text](/results/moving-mnist/1/0-1-digits.gif) ![Alt Text](/results/moving-mnist/1/1-1-digits.gif) ![Alt Text](/results/moving-mnist/1/2-1-digits.gif) ![Alt Text](/results/moving-mnist/1/3-1-digits.gif) ![Alt Text](/results/moving-mnist/1/4-1-digits.gif) ![Alt Text](/results/moving-mnist/1/5-1-digits.gif) ![Alt Text](/results/moving-mnist/1/6-1-digits.gif) ![Alt Text](/results/moving-mnist/1/7-1-digits.gif) ![Alt Text](/results/moving-mnist/1/8-1-digits.gif) ![Alt Text](/results/moving-mnist/1/9-1-digits.gif) ![Alt Text](/results/moving-mnist/1/10-1-digits.gif) ![Alt Text](/results/moving-mnist/1/11-1-digits.gif) ![Alt Text](/results/moving-mnist/1/12-1-digits.gif)

## Out of Domain Runs (3 input objects)

Out of domain runs with 3 input objects. The sequence is 40 frames long and both models received the ground truth as input for the first 20 frames. **Top: Ground Truth, Middle: RNN, Bottom: VRNN**

![Alt Text](/results/moving-shapes/3/0-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/1-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/2-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/3-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/4-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/5-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/6-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/7-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/8-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/9-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/10-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/11-3-shapes.gif) ![Alt Text](/results/moving-shapes/3/12-3-shapes.gif)

![Alt Text](/results/moving-mnist/3/0-3-digits.gif) ![Alt Text](/results/moving-mnist/3/1-3-digits.gif) ![Alt Text](/results/moving-mnist/3/2-3-digits.gif) ![Alt Text](/results/moving-mnist/3/3-3-digits.gif) ![Alt Text](/results/moving-mnist/3/4-3-digits.gif) ![Alt Text](/results/moving-mnist/3/5-3-digits.gif) ![Alt Text](/results/moving-mnist/3/6-3-digits.gif) ![Alt Text](/results/moving-mnist/3/7-3-digits.gif) ![Alt Text](/results/moving-mnist/3/8-3-digits.gif) ![Alt Text](/results/moving-mnist/3/9-3-digits.gif) ![Alt Text](/results/moving-mnist/3/10-3-digits.gif) ![Alt Text](/results/moving-mnist/3/11-3-digits.gif) ![Alt Text](/results/moving-mnist/3/12-3-digits.gif) 

## Generation diversity

We test the VRNN's capability in generating novel sequences on 4 separate runs .  Each sequence is 200 frames long and both models received the ground truth as input for the first 20 frames. **Top: Ground Truth. Each row is a separate run.**

![Alt Text](/results/moving-shapes/diversity/0-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/1-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/2-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/3-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/4-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/5-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/6-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/7-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/8-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/9-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/10-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/11-2-shapes.gif) ![Alt Text](/results/moving-shapes/diversity/12-2-shapes.gif)

![Alt Text](/results/moving-mnist/diversity/6-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/7-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/8-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/9-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/10-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/11-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/12-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/13-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/14-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/15-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/16-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/17-2-digits.gif) ![Alt Text](/results/moving-mnist/diversity/18-2-digits.gif)
