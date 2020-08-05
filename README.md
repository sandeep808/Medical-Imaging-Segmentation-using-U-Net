# Medical-Imaging-Segmentation-using-U-Net

Sample Images, Objective and our approach :
● Objective - Automate the
generation of the image masks
● Approach – Use U-Net, a
special CNN designed for
segmentation tasks to
generate these masks


The goal of segmentation is to
separate different parts of image, into
sensible coherent parts. Where we are
basically predicting the class for each
pixel in an image.


● There are two types of Segmentation.
1. Semantic Segmentation
2. Instance Segmentation

Type 1 – Semantic Segmentation
● Pixel classifications
based on defined
classes e.g. roads,
persons, cars, trees
etc.

Type 2 – Instance Segmentation
● Pixel classifications
combined with
classifying object
entities e.g. separate
persons, cars etc.

Applications in Medical Imaging
● Many medical applications necessitates finding and
accurately labeling things found in medial scans.
● This is often done using advanced software to assist
medical technicians and doctors. However, this task still
requires human intervention and as such, can be tedious,
slow, expensive and prone to human error.
● There’s a huge initiative for use Computer Vision and Deep
Learning to automate many of these tasks

U-Net
458
● Created in 2015, U-Net was a unique CNN developed for
Biomedical Image Segmentation.
● U-Net has now become a very popular end-to-end encoderdecoder
network for semantic segmentation
● It has a unique Up-Down architecture which has a Contracting path
and an Expansive path.


U-Net’s Structure
460
1. The downsampling path in U-Net consists of 4 blocks with the following layers:
○ 3x3 CONV (ReLU + Batch Normalization and Dropout used)
○ 3x3 CONV (ReLU + Batch Normalization and Dropout used)
○ 2x2 Max Pooling
○ Feature maps double as we go down the blocks, starting at 64, then 128, 256
and 512.
2. Bottleneck consists of 2 CONV layers with Batch Normalization & Dropout
3. The up sampling path consists of 4 blocks with the following layers:
○ Deconvolution layer
○ Concatenation with the feature map from the corresponding contracting path
○ 3x3 CONV (ReLU + Batch Normalization and Dropout used)
○ 3x3 CONV (ReLU + Batch Normalization and Dropout used)
