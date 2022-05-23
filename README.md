
<p align="center">
  <img src="https://github.com/tmartinez88/RTLEARNER/blob/main/assets/RTLEARNER_PIC.png?raw=true" width="300" title="RTLEARNER APP">
</p>

## Abstract
Developed during an independent study with Professor Johanna Devaney in the Sonic Arts MFA at Brooklyn College, RTLEARNER (or Real-Time Learner) is a set of example applications for fast dataset creation, and real-time communication between MaxMSP and the Python machine learning library Sci-Kit Learn. MaxMSP has long been the programming environment of choice for new music practitioners, containing within it a wide variety of composable audio processing units. Sci-Kit Learn has emerged as the goto framework for machine learning tasks, and provides with it a number of popular ML (machine learning) algorithms for classification and prediction in a highly approachable yet optimized format.

RTLEARNER implements a bi-directional OSC client/server architecture to act as a go-between for MaxMSP and the Python environment, offering one method for exploiting the particular advantages of each environment. Python, is not well suited for musical, real-time digital signal processing, but provides a wide array of tools in the domain of perceptual data analysis. MaxMSP, in this paradigm, handles audio input and output buffers, the feature extraction for dataset creation, and passes with low latency, feature sets to the machine learning model hosted by the Python environment. The Sci-Kit Learn library then handles predictions on these feature sets which can then be sent to and processed further by MaxMSP to affect parameter changes in a real-time musical context.

Though it is intended to be used for audio classification processes, components of the patch could very well be altered to classify other data native to Max, such as visual or gestural information.

## Other tools
Machine Learning tools within Max such as FluCoMa, Magenta Studio, and ml.star offer classification, prediction, and even generation processes all within a singular software environment. The trade off for this this elegance is less composability in the underlying model parameters and less exposure to the core systems of  of machine learning. For many  

## Demonstration
https://www.youtube.com/watch?v=e7F6OkrapIU&t=5s

## use cases

## Dependencies
The RTLEARNER max patch uses a number of FluCoMa objects for feature extraction. The FluCoMa objects can be downloaded [here](https://www.flucoma.org/download/), and soon in the Max package manager. These objects may be swapped out for other analysis objects such as Zsa Descriptors which can be found in the Max package manager, though this repository does not depend on them.

## Setup

### 1. Installation
1. Both Windows and Mac are supported.
2. Python 3.9 is recommended. I used a virtual environment using anaconda. pip install sklearn, numpy, pandas, python-osc to
3. Install [ffmpeg](https://ffmpeg.org/download.html#get-packages). This is necessary for reading audio files.
4. Install [PyTorch](https://pytorch.org/get-started/locally/). Pick the latest stable version, your operating system, your package manager (pip by default) and finally pick any of the proposed CUDA versions if you have a GPU, otherwise pick CPU. Run the given command.
5. Install the remaining requirements with `pip install -r requirements.txt`
