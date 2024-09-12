
# Deep learning with uncertainty quantification for predicting Dice coefficient of computational histopathology image segmentation




# Index:

1. Data can be obtained at: https://drive.google.com/drive/folders/1TJAd_aG9_8Hde06YnHmagnWrGh1xgxlJ?usp=drive_link

2. Trained Models can be obtained at: https://drive.google.com/drive/folders/1wu1U4jo_eD5FWyFNYqj2JNFq4jCOZcSe?usp=drive_link

3. The codes for training and evaluation of trained models can be obtained at: https://drive.google.com/drive/folders/1wu1U4jo_eD5FWyFNYqj2JNFq4jCOZcSe?usp=drive_link

 

# Gallery of model outputs: 
The segregated uncertainty maps for Train-from-scratch (TFS) Monte Carlo dropout deep learning models (MCD) augmented with backprop and dropout uncertainty explanations for prostate tumor segmentation are shown in the following figures. The uncertainty maps are represented as heatmaps, with deeper red indicating greater uncertainty and deeper blue indicating the bleast uncertainty. The maps include binary segmentation masks from the MCD model output and corresponding uncertainty estimates for tumor tissue regions, non-tumor tissue regions, and non-tissue regions.

* Proposed algorithm.
  
  * https://drive.google.com/drive/folders/18sdJE27fa6jS9yAGmGifPd798Qh7ZCo7?usp=drive_link
![fig1](https://github.com/Dr-Pratik-Shah-UCI/EMBC2024_prostate/assets/20062780/f01fc9ff-7fab-41ce-93fa-73faf0c26d0b)

* Segmentation and Uncertainty Maps for Backprop and Monte-Carlo Dropout augmented TFS models. “GT” – clinical ground-truth, “back-gr” – non-tissue regions.

   * https://drive.google.com/drive/folders/18sdJE27fa6jS9yAGmGifPd798Qh7ZCo7?usp=drive_link
![fig2](https://github.com/Dr-Pratik-Shah-UCI/EMBC2024_prostate/assets/20062780/69c20679-6ed8-42b2-beb2-3d45c649af47)

* Model output segmentation and region-based uncertainty maps. Visualization of model output and uncertainty explanations for prostate tumor segmentation by a Monte Carlo dropout deep learning model (MCD) trained using microscopic Hematoxylin and Eosin (H&E) dye stained prostate core biopsy images. Left to right columns: A, Input RGB image; B, Binary mask of clinical ground-truth label; C, Binary mask of segmentation from MCD output image; D, Uncertainty estimate maps of binary segmentation of MCD model; E, Uncertainty estimate maps of binary segmentation of MCD model for tumor tissue regions; F, Uncertainty estimate map of binary segmentation of MCD model for non-tumor tissue regions; G, Uncertainty estimate map of MCD model binary segmentation for non-tissue regions. Color bar shows the degree of model uncertainty with deeper red indicating greater uncertainty and deeper blue indicating the least uncertainty (with lowest value being 0). “GT” – clinical ground-truth, “back-gr” – non-tissue regions.
   * https://drive.google.com/drive/folders/18sdJE27fa6jS9yAGmGifPd798Qh7ZCo7?usp=drive_link

   ![Fig3](https://github.com/Dr-Pratik-Shah-UCI/EMBC2024_prostate/assets/20062780/ef0438ae-b7dd-4094-9ee9-56076628daf4)

# FYI:

1. Architecture used: VGG-16-UNet (i.e., UNet encoder represents VGG-16 arch.)

2. a. TL indicates transfer learning using ImageNet pre-training
2. b. TFS indicates training from scratch (no transfer learning involved)

3. The DATA folder contains pre-processed data with binary segmentation masks (labels) for the prostate data, split into TRAIN (80%) and TEST (20%)

4. Trained  weights for segmentation of prostate core biopsy images are provided in the 'weights' folder

5. To get model outputs for the test images, navigate to the individual folder for transfer learning (folder 'seg_TL') and training from scratch (folder 'seg_TFS') and run: python test.py

# Dependencies: Python 3.6.7, Tensorflow 1.12.0, Tensorflow-probability 0.5.0, OpenCV 4.1.1 

Create a conda environment and use conda installations (i.e., using the Anaconda distribution) within that environment on your machine for this and make sure these versions match. You can make a Python 3.6 environment using conda and install these within it.
