# Chest Xray Segmenation and Classifcation

This project contains the code for the ML model to segment chest xrays using U-nets and uses a CNN to classify the chest xrays and diagnose diseases.

## Segmenation using U-nets

This project uses a U-net model to segment the images which has an encoder and decoder semgments. The encoder unit down-samples the image to look at low level features and the decoder block upsamples the image and localizes high level features.
![unet_arch](https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/u-net-architecture.png)

## Results
The results for the segmentation of one image are shown below. We predicted with an accuracy of 94%.

We have also included the loss and accuracy graphs plotted against the epochs.

## Classificaiton using CNNs
 
We use a very simple structure of 2 convolution layer and a max pooling followed by the same to predict the disease shown in any given image. The inference is shown within the notebook. The input size for the image is chosen to be 176 x 176. 

We tried to tweak the hyperparameters for better classification accuracy but to no avail.

The confusion matrix for the validation images using the model is shown:

## Future work

1. The classificaiton accuracy is not great. To overcome this we would like to augment the data. 
2. We would also like to add other models using transfer learning for classificaiton. The models of choice are:
  - Resnet 50
  - VGG 16
