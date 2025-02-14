# Rat Detector

Susana Luna -
Computer Vision -
Individual Assignment

Objective: Build a Rat Detector model using YOLOv10 model. 

Methodology: 
The provided dataset is automatically annotated using groundingDINO. Check notebook: auto_anotation_goundingDINO.ipynb (link: https://github.com/slunara/ratDetectorComputerVision/blob/main/auto_anotation_groundingDINO.ipynb) 
The annotated images were uploaded to Roboflow to check and correct the image annotation
6 models were created using different sizes, number of batches and learning rate for the YOLOv10 and YOLOv11 Check notebook: train_yolov10.ipynb (link: [train_yolov10.ipynb](https://github.com/slunara/ratDetectorComputerVision/blob/main/train_yolov10.ipynb)) 

Conclusions: 
- GroundingDINO is a powerful tool for automatic annotation; however, manual review and adjustment of incorrect annotations are essential to prevent training and validation errors.
- Roboflow provides an intuitive interface for manual annotation and includes additional preprocessing features. While these capabilities were not utilized in this project, they could be valuable for future improvements.
- It was demonstrated that using more advanced models and increasing the number of epochs significantly enhances model performance.
- The Nano version is more lightweight and efficient for training. While training 100 epochs on the Medium model took 33 minutes, the Nano model completed 200 epochs in the same 33-minute timeframe.
- The best-performing model was YOLOv11-nano trained for 200 epochs. With a precision of 94% and a recall of 88%.
- The model performed well during training and validation but struggled on the test dataset, showing signs of overfitting. To improve generalization, techniques like regularization, data augmentation, or balancing the dataset could help.
