# VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE  RECOGNITION

## Overview:
This README file provides an overview of the files present in the folder, their functionalities, instructions to use the dataset, and guidance on running the scripts for model training, evaluation, and visualization.

## Files:

1. ### **single-multi-scale-experiments**:
   
    The files within this directory encompass models designed for both single and multi-scale experiments. 
  For the single-scale evaluation, the test image size (Q) is configured as Q=S for a constant S, and Q=0.5(Smin+Smax) for S values within the range [256, 512]. 
  In the multiscale experiments, scale jittering is applied to the test images. Here, the test image size is specified as Q={S-32, S, S+32} for fixed S values of 256 pixels and 384 pixels.
  The following files are available within this directory:

   1. **model_A.py**: VGG-11 model
   2. **model_B.py**: VGG-13 model
   3. **model_C.py**: VGG-16 model with kernel size of 1*1
   4. **model_D.py**: VGG-16 model with kernel size of 5*5
   5. **model_E.py**: VGG-19 model



2. **vgg16_vgg19_with_different_kernel.py**:

   This particular script conducts experiments involving varying kernel sizes in the final layers. During testing, the three fully connected layers were transformed into convolutional layers, using filter sizes of 7, 1, and 1, respectively.
   Our experimentation involved replacing the initial layer, originally set at a filter size of 7, with two alternative models: one employing a filter size of 5 and the other using a filter size of 3. This comparative analysis was carried out for both the VGG-16(D) and VGG-19(E) models.


3. **multi_Crop_vgg19_&_vgg16.py**:
   - Here we used VGG-19 and VGG-16 models to perform multi crop evaluation. To run the experiments, run every cell in the notebook to replicate the results


4. **Ensemble_of_VGG_19_and_VGG_16.py**:
   - In this experiment, we performed ensemble of VGG-16 and VGG-19 through which we obtained better results compared to vanilla algorithm. To replicate the results, run each and every cell in order

## Dataset:

The project uses the **[Imagenette](https://github.com/fastai/imagenette#imagenette-1)** dataset for image classification. The dataset contains 10k samples classified into 10 classes. It is subset of original ImageNet dataset.
   
