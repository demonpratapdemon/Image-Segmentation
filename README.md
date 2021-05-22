# Image-Segmentation
Extracting the Interactive Foreground from the image

# ForeGround Extraction using Object Detection and Grabcut OpenCV
Using transfer learning with Mask RCNN as Object detector, we get the probable bounding box of the objects in the image. These bounding boxes are then selected having maximum probability and the rectangle tus obtained is fed into the Grabcut algorithm and initialised with the Rect.

# ForeGround Extraction using Superpixels method and Grabcut OpenCV
Superpixels are nothing but a cluster of pixels which we obtain locally situated pixels in the pixel grid of the image which carries the same semantic meaning.
Superpixels works best when it is converted to LAB color space. The slic method in addition to the image, it also takes the number of segments or the number of segments defined as
n_segments which defines how many superpixel segments we want to generate.
After the slic method runs, it provides the segments. With those segments, we can create a mask which will be the input to the Grabcut algorithm and initialise it with the MSK instead of RECT