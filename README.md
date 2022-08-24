# Image Reconstruction Using StyleGAN2
In this project you'll get familiar with the power of Generative Adversarial Networks (GAN for short).
Specifically, I used the Nvidia's StyleGAN2 Architecture for this project.

## Short background

### GANs?
Generative adversarial networks (GANs) have been shown to generate images of remarkable quality and photo-realism. A line of work called StyleGAN took the generation capabilities to new levels of realism. The website ”This Person Does not Exists” demonstrates these capabilities by sampling new images from StyleGAN2 at each page refresh. While we will be using StyleGAN2, it is worth noting that the recent StyleGAN3 improves on top of StyleGAN2 by using classical image processing and signal processing concepts such as anti-aliasing.
As you have seen, a GAN takes as an input random noise and is trained to generate an image. Here as well, StyleGAN2 takes in a random noise vector z and generates an output image which we will denote with Igen. We call the noise vector z a ”latent vector”and the space it is sampled from the ”latent space”.
The StyleGAN2 you will be using has been pre-trained on the FFHQ dataset, which consists of 70, 000 images of human faces at 1024×1024 resolution and contains variation in terms of age, ethnicity and image background. It also has good coverage of accessories such as eyeglasses, sunglasses, hats, etc. All the images are preprocessed and aligned so that facial parts locations are consistent across the dataset, as you will see later in the exercise, using this preprocessing pipeline is crucial for good results in this exercise.

### Latent Optimization
In IMPR course, we have seen the standard process in which neural networks are usually trained. The network weights are optimized by running some variant of Gradient Decent and Back Propagation (i.e the differ- entiation is done with respect to the weights of the network). 
In this project we use a slightly different setup, rather than optimizing the network weights, in Latent Optimization the latent vector itself (i.e the input of the GAN) is optimized while the weights of the generator remain unchanged.
That is, at each step the differentiation is done with respect to the latent code itself. This could be interpreted as finding the best latent code that minimizes the objective loss. In this exercise we will use Latent Optimization to perform GAN Inversion which we will cover next.

## Quick overview

This project can be divided into 3 different reconstructive parts:
#### 1. Image De-blurring
![Alt text](Deblur.png?raw=true "Title")

#### 2. Image Colorization
![Alt text](Colorize.png?raw=true "Title")

#### 3. Image In-painting 
![Alt text](Inpaint.png?raw=true "Title")


## Executing program
Assuming you are already familiar with Jupyter/Colab, as usual, you run all cells in their natural order and wait for the results.
Notice that inside the code itself, you have specific instructions for customize the code for your personal use. 


## Authors
This project was developed as a final exercise in Image Processing Course @ Hebrew University of Jerusalem, Israel. Lectured by Prof. Shmuel Peleg.
