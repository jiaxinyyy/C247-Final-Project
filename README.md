# Final Project for W25 ECE C147/247

### Setup
1) Clone this repository to your local system
2) Copy ```/data```folder into main directory 
    - i.e. ```{local path}/C247-Final-Project/data```
3) Run notebook to train!

### Code in /emg2qwerty
- ```lightning.py```
    - TDSConvCTCModule(pl.LightningModule) - class to assemble baseline model architecture
    - WindowedEMGDataModule(pl.LightningDataModule) - Contains dataset loader (Do not touch)
- ```modules.py```
    - Defines layers assembled in lightning.py
    - TODO: Add new layer architecture here
- ```transforms.py```
    - contains data augmentations functions, loaded into WindowedEMGDataModule in lightning.py
    - TODO: Try different data augmentation methods
- ```config/*.yaml```
    - Adjust hyperparameters here for training

To train:
```
!python -m emg2qwerty.train \
  user="single_user" \
  trainer.accelerator=gpu trainer.devices=1 trainer.max_epochs=30
```