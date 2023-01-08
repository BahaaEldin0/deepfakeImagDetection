# DeepFake Image Detection

This project is made to compare different AI Models in image classification detecting deepfaked images from real images, we used the 140kimages dataset from kaggle to train the models [DataSet](https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces)




## Training
We used 3 models from tensorflow keras library.
DenseNet121
ResNet101V2
InceptionV3

the training dataset was 100k images and 20k for validation
each one was trained twice once on the regular colored dataset, and another time on the grayscaled dataset to check for the best input shape for the data.

## Results
After Training we tested on a 20k images we saw the following ROC Scores


| DataSet  | DenseNet121 | ResNet101V2  | InceptionV3 |
| ------------- | ------------- | ------------- | ------------- |
| GrayScale  | 0.997279655  | 0.9922737850000001  | 0.998956665  |
| Colored  | 0.996271405  | 0.994448455  | 0.997279655  |

## Testing 

So we choose to go with ensembling to get the best results by choosing the most same answers and using tensorflow built in ensambling function too.