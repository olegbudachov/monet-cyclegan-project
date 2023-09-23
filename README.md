# monet-cyclegan-project

## ipynb file is big, that is why in order to see it, you need to upload zip file `monet-cyclegan-project.zip` and extract it all

### Table of Contents
1. Project overview
2. Data description
3. Model
4. Loss
5. Training Loop
6. Hyperparameter Tuning
7. Training and validation of CycleGAN
8. Conclusion
9. References

### 1. Project overview
The challenge problem in this project revolves around the task of unpaired image-to-image translation. Specifically, it entails transforming landscape images into a style resembling the renowned artist Monet's paintings. To achieve this, a generative deep learning model known as CycleGAN is employed. The core objective is to train the model to perform this transformation seamlessly.

The primary target of this project is to attain a Kaggle Score with an FID (Fréchet Inception Distance) metric of less than 120. This metric serves as an essential measure of the quality and similarity between the generated images and Monet's artistic style.

Additionally, there are several ancillary objectives to be achieved.

Firstly, the generated images should convincingly resemble Monet's paintings, aligning with the artistic aesthetics.
Secondly, minimizing cycle loss is crucial, ensuring that the images maintain their original characteristics when translated back and forth between the two domains (landscape and Monet-style).
Lastly, it's vital to prevent the collapse of landscape images when processed through the generator and vice versa, which is addressed through minimizing identity loss.
Successfully meeting these objectives showcases the effectiveness of the CycleGAN model in achieving the desired image transformation and artistic style replication.

### 2. Data description
add Codeadd Markdown
The dataset comprises four main directories: "monet_tfrec," "photo_tfrec," "monet_jpg," and "photo_jpg." Each set of directories contains images in different formats and represents two distinct categories: Monet paintings and photos.

#### Monet Paintings:
"monet_tfrec": This directory contains 300 Monet paintings, each sized 256x256, stored in the TFRecord format. TFRecords are a binary format commonly used with TensorFlow for efficient data storage and retrieval. "monet_jpg": Similarly, this directory includes the same 300 Monet paintings but in JPEG format. JPEG is a standard image format widely supported by various image processing tools.

#### Photos:
"photo_tfrec": In this directory, you will find 7,038 photos, each sized 256x256, stored in TFRecord format. These photos serve as the base images for the Monet-style transformation task. "photo_jpg": Similar to the TFRecord version, this directory contains the same set of 7,038 photos but in JPEG format.

#### Data source
The original data is available in kaggle competition website.

https://www.kaggle.com/competitions/gan-getting-started/data
