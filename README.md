# Cassava-Disease-Classification
 
The cassave plant is the third largets source of carbohydrates in the world. Unfortunately due to diseases, there has not been a harvest yield increase globaly in 25 years. 

Using machine learning I built an image classifier to detect whether a cassava plant has a disease and which of the top 4 most common diseases it is. 

While the main priority is to identify whether or not a plant has a disease, it is also very important to identify which disease it is so that the farmers know how to properly handle the situation. For some diseases, the plant can be recovered by simply removing any infected parts before it spreads. With others, the plant needs to be fully removed, dried and burned.


The data used for this is about 21,000 images gathered by Uganda's National Crops Resources Research Institute. This data is near for my objective as it is vast, as well as being sourced directly from farmers who took pictures of their crops. The Institute then went through and labeled each image.

The one downside of this dataset was the massive imbalance in its data. Among the 5 classes there was a ratio of 1:2:2:2:13

Data is stored in TTVS (train, test, and validation split) directory. 21,000 images split amount 5 classes. After a 60, 20, 20 split, the training data was massivley imbalanced with the following quantities

CBB 652; CBSD 1313; CGM 1431; CMD 7894; Healthy 1546

Useing random selection the CMD class was reduced to 5000 images and using data augmentation methods the other classes were increased to 5000 images.

This was done to deal with the datasets inherent class imbalance, which would skew the training and lead to overfitting of the class with a greater quantity of data.

While other meds do exist to deal with the class imbalance, this method was chosen due to it affecting the dataset and not the model, thus making the various models run faster.


