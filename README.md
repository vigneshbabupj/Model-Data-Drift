# Model-Data-Drift
Sample Code for Monitoring Data Drift using [Alibi Detect](https://github.com/SeldonIO/alibi-detect)

Refer the notebook : [Drift_monitoring](https://github.com/vigneshbabupj/Model-Data-Drift/blob/main/S11_Drift.ipynb)

- Load a pretrained torch scipted resnet18 model trained on Cifar10 data - [model](https://github.com/vigneshbabupj/lightning-hydra-timm-template/blob/main/Docker/demo/model.script.pt)
- Apply preturbation in the test images using Albumentaions (RandomBrightnessContrast, AdvancedBlur, MultiplicativeNoise)
- Check for Data Drift
- Train model using the same preturbation as Image augmentation
- Saved metrics and 25 sample images in Tensorboard

## Augmented Images during Training
![img](https://github.com/vigneshbabupj/Model-Data-Drift/blob/main/images/tensorboard_albu_img1.png)
![img2](https://github.com/vigneshbabupj/Model-Data-Drift/blob/main/images/tensorboard_albu_img2.png)

- Train log with data drift monitoring after every epoch [Logs](https://github.com/vigneshbabupj/Model-Data-Drift/blob/main/train_log.md)

- Notebook with different kinds of drift monitoring [Link](https://colab.research.google.com/drive/1uNKdtVyZEIz508bQTCq3EMLoXLzxZvWQ?usp=sharing#scrollTo=bdCenhBmip_n)
