# Building Damage Assessment from High-resolutoin Remote Sensing Images

## Project Data:
The original annotations are from XView dataset (https://xview2.org/) and the NAIP remote sensing data was acquired through GEE API.
Annotations converted and extracted from XView dataset in shapefile format can be found in the /Data folder
### Registration for the GEE API:
https://developers.google.com/earth-engine/python_install-conda
https://developers.google.com/earth-engine/python_install

## Jupyter Notebook
Please refer to the /Notebook folder, three notebooks were included:
1. Setup_Feature_Classification.ipynb
Based on preprocessed annotations, get data from GEE API, calculated features and unsupervised clusters, use decision tree, SVM, and Random Forest to classify building damage types on GEE server, and extract NAIP images from GEE to test some other machine learning method at local client end.

2. BuildingProj_XGBoost.ipynb
Based on NAIP images extracted from 1, use XGBoost to classify building damage types and analyze effects of different features on predictions.

3.BuildingProj_NN.ipynb
Based on NAIP images extracted from 1, use 5-layer simple neural network to classify building types

## Other Scripts
Please refer to the /Script folder. Scripts for preprocessing of original XView annotations (xview_preprocessing.py).

