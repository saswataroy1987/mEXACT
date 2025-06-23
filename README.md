# Beyond Just Saying It's False: Explainable AI for Multimodal Misinformation Detection 
## Authors : __Saswata Roy*, Manish Bhanu*, Shalini Priya, Joydeep Chandra, Sourav Dandapat__
\* these authors contributed equally to this wok.
###### Paper DOI is found at https://doi.org/10.1007/s10489-025-06656-2

## Introduction
mEXACT finds a variable-size bucket of check-worthy MS information whose removal from a false input sample can invert model prediction. Consequently, the proposed model is capable of distinguishing contributing and non-contributing misinformation elements for better explainability along with outperforming the existing models over classification performance.


## If you use the code, we appreciate it if you cite our paper
~~~~
@article{roy2025beyond,
  title={Beyond just saying it’s false: explainable AI for multimodal misinformation detection},
  author={Roy, Saswata and Bhanu, Manish and Priya, Shalini and Chandra, Joydeep and Dandapat, Sourav Kumar},
  journal={Applied Intelligence},
  volume={55},
  number={11},
  pages={1--18},
  year={2025},
  publisher={Springer}
}

~~~~

## Installation

### Prerequisite
----------------------
Python >= 3.6.
Anaconda 3

### Create Environment
Type the following command to create the environment "mexact" which contains all the required packages. <br />
~~~~
conda env create -f mexact.yml
~~~~
-----------------------

## Details

### Details of getData.py
 * This python script first prepare the data for news text, user comments and news images.
 * Next, it invokes build_NeuralNet() function of another script getModel.py to compile our neural network model.
 * Execute "getData.py" file to initite the training process.
 * After model training is done, save the trained model.
 * Required files will be saved under "repo_Fast" folder.
   
### Details of getModel.py
 * This file contains the main DNN model mEXACT.
 * mEXACT first extracts encodede representation of news text, user comments and news image.
 * Next, mEXACT invokes artificialThresholding() function to retain the LS features in the encodede representation of news text, user comments and news image.
   
### Details of getData_Explainability.py
 * This python script also prepares the data for news text, user comments and news images.
 * Next, it loads the already saved trained mEXACT model.
 * Finally, this script stores the explainable and non-explainable components of news text, user comments and news image by analyzing the MS and LS information. 



## mEXACT Framework

![](mEXACT_final.png)


## Some correctly predicted reconstructed news images and their corresponding MS and LS information
![](mexact_predicted.png)


