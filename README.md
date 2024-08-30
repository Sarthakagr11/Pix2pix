# Pix2pix

This demonstrates how to build and train a conditional generative adversarial network (cGAN) called pix2pix that learns a mapping from input images to output images, as described in Image-to-image translation with conditional adversarial networks by Isola et al. (2017). pix2pix is not application specific—it can be applied to a wide range of tasks, including synthesizing photos from label maps, generating colorized photos from black and white images, turning Google Maps photos into aerial images, and even transforming sketches into photos.

In this example, this network will generate images of building facades using the CMP Facade Database provided by the Center for Machine Perception at the Czech Technical University in Prague. To keep it short, this will use a preprocessed copy of this dataset created by the pix2pix authors.

In the pix2pix cGAN, you condition on input images and generate corresponding output images. cGANs were first proposed in Conditional Generative Adversarial Nets (Mirza and Osindero, 2014)

The architecture of your network will contain:

- A generator with a U-Net-based architecture.
- A discriminator represented by a convolutional PatchGAN classifier (proposed in the pix2pix paper).
- Note that each epoch can take around 15 seconds on a single V100 GPU.
