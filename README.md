# Facial-Keypoints-Detection_FastAI

### Overview
Detecing facial keypoints is a very challenging problem.  Facial features vary greatly from one individual to another, and even for a single individual, there is a large amount of variation due to 3D pose, size, position, viewing angle, and illumination conditions. Computer vision research has come a long way in addressing these difficulties, but there remain many opportunities for improvement.

### Notes
This dataset has missing values, will be nice to experiment how to handle the missing values.
#### Drop missing values

Dripping missing values will results in huge reduction in data, so it is not viable option

#### Fill missing data
1. Forward fill ```ffill``` works better
2. Fill with median values, results are similar to Forward fill
3. Fill with mean values, doesn't works for smaller faces

I have kept codes related to all the above options, for experimentation. Feel free to do so!

### Implementation details
| Feature | Brief Explanation |
| ------ | ------ |
| Base Model Architecture | Resnet152 from [ResNet](https://arxiv.org/abs/1512.03385) family, implemetation from [PyTorch](https://pytorch.org/)|
| Learning Rate Finder | [Learning rate finder](https://arxiv.org/abs/1506.01186) implemetation from [FastAI](https://www.fast.ai/) |
| Learning rate and  Momentum scheduler| [One cycle policy](https://arxiv.org/abs/1803.09820) implemetation from [FastAI](https://www.fast.ai/)  to achieve superconvergence |
| Dataset |  Dataset [Facial Keypoints Detection](https://www.kaggle.com/c/facial-keypoints-detection/overview) from [Dr. Yoshua Bengio](http://www.iro.umontreal.ca/~bengioy/yoshua_en/index.html) and James Petterson |


### Results
| Model | Metrics(Validation loss) | Epochs |
| ------ | ------ | ------ |
| Resnet152 | 0.002639 | 12 |


#### Inference
![Alt text](https://github.com/gurucharanmk/Facial-Keypoints-Detection_FastAI/blob/main/images/results.png  )

## License
This project is licensed under the [MIT License](https://github.com/gurucharanmk/Facial-Keypoints-Detection_FastAI/blob/main/LICENSE)
