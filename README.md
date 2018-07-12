# EpicyclicAnimator
This repo is an implementation of reconstructing 2-D sequential point clouds using Fourier series. This is based off [this](https://mathematica.stackexchange.com/a/171756) answer on stackexchange. The original code has been done is mathematica, and this is a python 2.7 implementation.

The notebook [Epicycles.ipynb](Epicycles.ipynb) is self-explanatory, with comments at relevant places.

For the interested user, play around with the value `m`-- no. of fourier components. If you have it more than the no. of points taken for the image, you can see some interesting effects!

-----------------------------------------
#### Testing

The following images in assets/ seem to work without a hitch: [Eli](assets/Eli.png) and [Groot](assets/Groot4.png). ~~The remaining need to be validated. I shall, tomorrow, if I am not snapped.~~

All of the images in [assets](assets/) have been validated. There are certain examples to how the image must be:

1. The image must **not** have mutiple loops. Images like [this version of Avengers logo](assets/A.png) is not preferred. Rather, [this version of Avengers logo](assets/A2.png) is preferred. 
2. Different images require different kinds of preprocessing. This is done using cv2 by performing morphological operations. Complex segemented masks could potentially be extracted.
-------------------------------------------

#### Potential work to be done
1. Replace the FT with `np.fft.fft` for faster, and more accurate computation.
2. Some instabilities occur for certain images. Need to fix this.
3. The 2-opt algorithm implementation is **very** slow. Need to optimize it.
4. Automate preprocessing.

Constructive criticism is welcome on the work done!
