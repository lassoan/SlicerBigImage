# SlicerScope

## Introduction

SlicerScope is an extension of 3D Slicer. It is used for large scale
microscopic image viewing and computing.

Computational histopathology is a fast emerging field which converts
the traditional glass slide based department to a new examination
platform. Such a paradigm shift also brings the in silico computation
to the field. Much research have been presented in the past decades on
the algorithm development for pathology image analysis. On the other
hand, a comprehensive software platform with advanced visualization
and computation capability, large developer community, flexible plugin
mechanism, and friendly transnational license, would be extremely
beneficial for the entire community.

SlicerScope is an open platform for whole slide histopathology image
computing based on the highly successful 3D Slicer.

In addition to viewing the giga-pixel whole slide image viewing,
currently, the extension also offers several specific analytical
modules for qualitative presentation, nucleus level analysis, tissue
scale computation, and 3D pathology. Thanks to the openess of Slicer,
the SlicerScope extension could also be further extended by you.

## Build
The module also needs the openslide library to be installed on your
computer. Under linux (apt system), this could be done by simply running:

sudo apt install libopenslide

The module in this extension will install the python wrapper of
openslide through pip. This is done automatically the first time the
module is run. But you may need to restart Slicer to use it.

## Usage

### Example data
Example large scale wholse slide image can be downloaded at, e.g., the
[OpenSlide
website](https://openslide.cs.cmu.edu/download/openslide-testdata/Aperio/CMU-1.svs
"Brightfield WSI")

### Large whole slide image viewing
Swith to the "SlicerScopeViewer" module in the SlicerScope category. As shown in the module panel, select the WSI file to view in the "Select WSI" box. Then click "Load WSI" below.

![image](https://user-images.githubusercontent.com/89077084/174545558-4dc2a490-ccb9-4de9-9237-6bc93de731ff.png)

One can then view different region/scale of the image, using mouse dragging and mosue wheeling, as shown below:

![image](https://user-images.githubusercontent.com/89077084/174545844-83a5f601-32ca-4d88-b328-b3a0cba0e922.png)
![image](https://user-images.githubusercontent.com/89077084/174545870-063ae0a8-2e3d-49bd-8d61-08ca19c5dbb6.png)

### Staining decomposition
Histopathology images are often stained using different dyes. When a WSI is stained using multiple dyes, the different stains can be computationally separated using the module "ColorDecomposition", whose panel is shown below.

![image](https://user-images.githubusercontent.com/920557/174555656-1e227e15-2110-4bf1-8b9d-74b1fdddc823.png)

There are various options for color decomposition. This particular WSI is stained with H-E. Its original appearance is:
![image](https://user-images.githubusercontent.com/920557/174556082-81738b77-87f5-4111-bf31-bbca18501501.png)

After decomposition, the hematoxylin content is shown in gray-scale as:
![image](https://user-images.githubusercontent.com/920557/174556323-eb064126-c40b-48a2-95bd-f4a0c77d60b3.png)
where the dark regions corresponding to the high hematoxylin content.

If the eosin chanel is wanted, one can switch the output chanel in the module panel to the 2nd chanel, and the result will be like:
![image](https://user-images.githubusercontent.com/920557/174556464-e4e1d6d0-f1c3-4222-ad68-f490a520ae98.png)


## Citation

If you find this extension helpful please cite this paper:

Xiaxia Yu, Bingshuai Zhao, Haofan Huang, Mu Tian, Sai Zhang, Hongping Song, Zengshan Li, Kun Huang, Yi Gao, "An Open Source Platform for Computational Histopathology," in IEEE Access, vol. 9, pp. 73651-73661, 2021, doi: 10.1109/ACCESS.2021.3080429.


