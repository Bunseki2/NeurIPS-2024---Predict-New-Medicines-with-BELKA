# NeurIPS-2024---Predict-New-Medicines-with-BELKA 
Kaggle competition
    Predict small molecule-protein interactions using the Big Encoded Library for Chemical Assessment (BELKA)
https://www.kaggle.com/competitions/leash-BELKA

Leaderboard : https://www.kaggle.com/competitions/leash-BELKA/leaderboard

Dataset : https://www.kaggle.com/datasets/ahmedelfazouan/belka-enc-dataset

Base NoteBook : https://www.kaggle.com/code/ahmedelfazouan/belka-1dcnn-starter-with-all-data


Hello!

I would like to thank Kaggle for organizing such an interesting competition. We also appreciate @ahmedelfazouan for sharing notebooks and dataset that influenced my solution.

Below you can find a outline of how to reproduce my 4th_place solution for the NeurIPS 2024 - Predict New Medicines with BELKA competition.



#ARCHIVE CONTENTS  
solution_4thplace.ipynb	: code to rebuild models from scratch and generate predictions 
my.model-0.keras	: model archived 
model-0.h5 : model_weight
requirements.txt
Model_summary.txt


#HARDWARE: (The following specs were used to create the original solution)
Kaggle NoteBook 
Its default CPU(s) (Intel(R) Xeon(R) CPU @ 2.00GHz) and TPU VM v3 

#SOFTWARE (python packages are detailed separately in `requirements.txt`):

#DATA SETUP 
down load pre-processed data from https://www.kaggle.com/datasets/ahmedelfazouan/belka-enc-dataset


#DATA PROCESSING-MODEL BUILD-PREDICTION
run solution_4thplace.ipynb
    a) expect this to run for 3 hrs or so
    b) train all model 


# Key Points
The model is a very basic experiment and far from the optimal. You can improve and optimize it. 
- used whole data with TPU
- did PCA and projected data to 3d space 
- appended these to the dataset and trained with 1DCNN + original parameters.

The keys that set my solution apart from others in the competition might come from simple feature engineering, including reduced dimension chemical space information along with detailed chemical structure information, simple 1D-CNN, and all data.

# Background
Small molecule drugs work by interacting with proteins in cells to change their function. Traditionally, finding these drugs is a slow process of making and testing them one by one. While there's a vast chemical space with potential treatments, the current method is too time-consuming to explore it fully. To address this, Leash Biosciences created a large dataset (BELKA) of 133M small molecule interactions with protein targets. This dataset aims to promote the use of machine learning to predict drug-target interactions, potentially revolutionizing drug discovery by enabling computational screening of the chemical space instead of relying solely on lab experiments.

# DNA-encoded chemical libraries (DELs)
DELs are collections of small molecules, each tagged with a unique DNA barcode. This barcoding system offers a scalable alternative to traditional high-throughput screening, which requires handling individual small molecules in separate tubes. DELs allow for many molecules to be mixed in a single tube and screened simultaneously against a protein target. Molecules that bind to the target are identified through DNA sequencing of their barcodes. DELs are created by chemically combining different building blocks, analogous to building a Mickey Mouse head with different attachments.   

!(/assets/images/DEL_Kaggle.png)
