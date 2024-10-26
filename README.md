# Traffic Light Sight

Traffic light detection from images using a small YOLOv8 model.

The model was fine-tuned and evaluated on the [LISA Traffic Light Dataset](https://www.kaggle.com/datasets/mbornoe/lisa-traffic-light-dataset/data). The main goal is to detect and classify traffic lights into green, yellow and red classes.

## Features
- **Acceptable performance** for a small model, it achieves >0.7 for precision, recall and mAP50 on testing data with <1h training.
- **Reduced training data size by 83%** by removing highly similar images using CLIP for image similarity and employing relevant augmentations for better generalization.
- **Inference speed <170ms** on Apple M2. 

## Testing

The model demonstrates good daytime detection. However, nighttime detection remains challenging due to different lighting conditions, as illustrated in the following examples:

<img src="./output/output_daySequence1_1.gif" loop=infinite>
<img src="./output/output_daySequence1_2.gif" loop=infinite>
<img src="./output/output_nightSequence1_2.gif" loop=infinite>

## Future

- Increase training set with relevant data to improve detection.
- Optimize the model for better performance and inference speed.
