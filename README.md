# Enhancing Handwritten Image Detection with GANs and Optical Feature Extraction Techniques

## Abstract
This paper presents a novel approach for the Handwritten Image Detection task that combines the deep-convolution GAN (DCGAN) model with optical feature-extraction techniques, including Oriented FAST with Rotated BRIEF (ORB) and Scale Invariant Feature Transform (SIFT) using the Bag-of-Features approach. Our model uses the image and its optical features (SIFT or ORB) as the inputs to a network trained to recognise the shape and orientation of characters from each class. This study examines the effect of both regular and dense optical features. We evaluate our algorithm on the MNIST, EMNIST, and MADBase datasets. The results indicate that GANs using optical feature approaches are superior to classical GANs, with an accuracy improvement of 4.88% in the MNSIT dataset, 6.89% in the EMNIST dataset, and 0.62% in the MADBase dataset. In addition, our approach surpasses the state-of-the-art methods on the MADBase dataset.

## About
These python notebooks implement the algorthims and experiments discussed by the authors in the mentioned paper: [Enhancing Handwritten Image Detection with GANs and Optical Feature Extraction Techniques](https://ieeexplore.ieee.org/document/10112139). The datasets have been mentioned along with all the pre-processing steps taken before mored generation.

**DOI: 10.1109/ISCON57294.2023.10112139**

## Usage
We have trained out model on three datasets: MNIST, EMNIST and MADBase.

The repository contains .ipynb file (python notebooks) with the following naming conventions:
1. GAN\_<dataset\_name>\_tf\_generation.ipynb: Training DCGAN to generate images from the given dataset.
2. GAN\_<dataset\_name>\_tf\_classification.ipynb: Generates Histogram for the given dataset and trains the model on BoF architecture as discussed in paper.

Run "GAN\_<dataset\_name>\_tf\_generation.ipynb" to pre-train the model and then run 'GAN\_<dataset_name>\_tf\_classification.ipynb' to get the results for the same dataset.

## Files and Uploads
1. GAN\_NET\_<dataset\_name>\_best\_weights.hdf5: Best weights trained DCGAN\_SIFT/ORB BoF model.
2. <dataset\_name>\_<SIFT/ORB>\_hitogram\_<train/test>.npy: Generated hitorgram for the dataset to be use for training/testing task.
3. [training\_checkpoints\_MNIST](https://drive.google.com/drive/folders/1669LBwHefgKl6UW8yVOTTDSwrztJl5qb?usp=share_link): Training checkpoint after generation phase for MNIST dataset.
4. [training\_checkpoints\_EMNIST](https://drive.google.com/drive/folders/1sBE9lHuJAQoCsLsJN1n7xkjV_YV5wgnC?usp=share_link): Training checkpoint after generation phase for EMNIST dataset.
5. [training\_checkpoints\_MADBase](https://drive.google.com/drive/folders/1mdAARbGvWNBCaPYBuVnBu96mSSPAC_ei?usp=share_link): Training checkpoint after generation phase for MADBase dataset.

## Citation
> R. Dubey and I. Das, "Handwritten Image Detection using DCGAN with SIFT and ORB Optical Features," 2023 6th International Conference on Information Systems and Computer Networks (ISCON), Mathura, India, 2023, pp. 1-6, doi: 10.1109/ISCON57294.2023.10112139.


