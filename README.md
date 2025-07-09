## DeepLabV3 and U-Net Turtle Segmentation

### Description
This project aims to use the DeepLabV3 and U-Net architectures for semantic segmentation of turtle images, 
distinguishing between background and different parts of the turtles. DeepLabV3 model is trained using ResNet50 
and ResNet101 backbones to enhance segmentation performance.

### Available architectures 

| Model                   | Backbone          | Dataset             |
| ----------------------- | ----------------- |---------------------|
| deeplabv3_resnet50      | resnet50          |100% dataset         |
| deeplabv3               | resnet101         |100% dataset         |
| Unet                    | -                 |100% dataset         |
| Unet_50_dataset         | -                 |50% dataset          |

### Dataset

Download the dataset from https://www.kaggle.com/datasets/wildlifedatasets/seaturtleid2022?resource=download. Prepare the data in the required format.
```
├── archive 
  ├── turtles-data
    ├──instances_train2014.json
      ├──data
        ├──data
          ├──images
          ├──annotations.json
          ├──metadata_splits.csv
          ├──metadata.csv
    ├── license.txt
```

### Pre-trained Models
Download the pre-trained models for training and test by downloading the trained model: https://drive.google.com/drive/folders/10jmnQ5l_aRit56m2Go8w-FZYw1htS2Jj?usp=sharing

### File Structure
```
├── README.md
├── deeplabv3.ipynb 
├── deeplabv3_50.ipynb
├── Unet.ipynb
├── Unet_50_dataset
  ├── Unet_50_dataset.ipynb
  ├── Processing_of_datasets.ipynb
  ├── trained_model.h5
```

### Citation
**DeepLabV3:**
Chen, Liang-Chieh, et al. "Rethinking Atrous Convolution for Semantic Image Segmentation." In arXiv preprint arXiv:1706.05587, 2017.
https://github.com/tensorflow/models/tree/master/research/deeplab

**Unet:**
Ronneberger, Olaf, Philipp Fischer, and Thomas Brox. "U-Net: Convolutional Networks for Biomedical Image Segmentation." In Proceedings of the International Conference on Medical Image Computing and Computer-Assisted Intervention (MICCAI), 2015.
https://github.com/milesial/Pytorch-UNet