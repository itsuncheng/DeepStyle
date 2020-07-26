# DeepStyle: Using State-of-the-Art Deep Learning to Generate Realistic High Fashion Clothing and Styles

This is the official repository for the Medium Article that contains all the relevant source code, jupyter notebooks, and configuration files for the paper. The paper is also included in the repository and can be found [here](https://github.com/itsuncheng/DeepStyle/blob/master/full_paper.pdf).

## Brief Description of the Files

The `.yaml` files contain the configuration details of the object detection models trained in this research as described in the paper.

The `DeepFashion2Coco.ipynb` shows the steps to convert the [DeepFashion Dataset](http://mmlab.ie.cuhk.edu.hk/projects/DeepFashion.html) to [COCO format](http://cocodataset.org/#format-data) to ease the training and validation of the models implemented by the [Detectron framework](https://github.com/facebookresearch/Detectron).

The `vis.py` file is under the `detectron/utils/` folder in the [Detectron github repository](https://github.com/facebookresearch/Detectron). Replace the `vis.py` file in the repository with the updated one to reproduce the cropping of the test images based on the predicted bounding boxes, as described in the paper. This `vis.py` adds the code for detecting full-body fashion items in images, cropping them based on the bounding boxes, and saving the results to a local directory.

Finally, the rest of the jupyter notebooks provide the implementation details of the DCGANs as described in paper. The hyperparameters for training and the architectures for the generator and discriminator are provided for each model tested. Code are written in Pytorch. 

