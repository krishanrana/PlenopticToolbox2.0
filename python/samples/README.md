## Python Samples

The samples given here are intended to give some hints about how to use the available code:

Up to now four scripts are provided, more can be added in case of request (just write me at lpa@informatik.uni-kiel.de)

#### Read the image (read_image.py)

Super simple file to test that everything is working. It just reads a file (real or synthetic) by giving as input the path to the configuration file (the .xml, (name of image and configuration file should be the same!) or the .json) and shows the image.

#### Read the image and change between micro-images and subaperture images (subapertureimages.py).

Input Image                |  Subaperture Views
:-------------------------:|:-------------------------:
![Input Image](https://github.com/PlenopticToolbox/PlenopticToolbox2.0/blob/master/python/samples/Dragon_Processed%20copy.jpg)  |  ![](https://github.com/PlenopticToolbox/PlenopticToolbox2.0/blob/master/python/samples/Dragon_Processed_subarpertureimages%20copy.jpg)

Since many people are used to the Lytro (Plenoptic 1.0 Cameras) this script allows you to exchange the way the data is shown. Plenoptic 2.0 Cameras have different physical properties, thus the subaperture views are quite small and low-quality. The script is mostly thought as an example of what you would get treating these kind of images as if they were Lytro images.
The images shown here are downscaled for visualization purposes.

#### Change the format of the synthetic images (from_synth_to_xml.py)

It reads all micro-images contained in the given folder (where the scene.json file is) and save the image as .png file with his relative .xml configuration file, so that it looks like a real image and can be easier accessed.

#### Estimate the disparity (disparity_sample.py)

Input Image                |  Disparity Map
:-------------------------:|:-------------------------:
![Input Image](https://github.com/PlenopticToolbox/PlenopticToolbox2.0/blob/master/python/samples/Dragon_Processed%20copy.jpg)  |  ![](https://github.com/PlenopticToolbox/PlenopticToolbox2.0/blob/master/python/samples/Dragon_Disparity.jpg)

A short example of how to read an image and calculate its disparity map. Several parameters can be tuned, starting from different similarity measures (SAD, SSD, CENSUS) and other algorithm parameters (minimum and maximum disparity, disparity step, penalty function, threshold for circle of confusion, minimum coverage).

For a further insight about the disparity estimation process, please refer to the papers
- [_Fleischmann O. and Koch R, Lens-Based Depth Estimation for Multi-focus Plenoptic Cameras, GCPR, 2014_](https://link.springer.com/content/pdf/10.1007/978-3-319-11752-2_33.pdf)
- [_Palmieri L. and Koch R, Optimizing the Lens Selection Process for Multi-Focus Plenoptic Cameras and Numerical Evaluation, LF4CV @ CVPR, 2017_](http://openaccess.thecvf.com/content_cvpr_2017_workshops/w27/papers/Palmieri_Optimizing_the_Lens_CVPR_2017_paper.pdf)


