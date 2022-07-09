# Image-classification-In-Pyspark-and-Elephas

Detection of diseases a plant may have based on the images of the leaves.

• The leaves on a plant are like a barometer. They can tell you what is happening to the plant.So given labeled images of plant leaves,we use Machine learning to detect if a plant is healthy or not.

• The dataset contains RGB images of leaves from different plants facing from different diseases. There are a total of 38 classes in this dataset. But for our task, we have used 33 classes which span over 9 plant species. The training set contains total of 58579 images, out of which 80 percent are used while training and 20 percent as validation set. The testing set contains total of 15231 images.

• The images are resized into size of 24x24 and flattened to store in pyspark dataframe which gives us total of 1728 features.Next,A neural network model that:

- Reshape the data from flat list to original shape
- Has Convolutional neural network model for feature extraction.
- Fully connected layers for classification
  
• Elephas is used to enable distributed computing.It is an extension of Keras, which allows you to run distributed deep learning models at scale with Spark.

# Results


Various metrics are used to evaluate the model on test set, these are: False positive Rate, Recall, Precision and f1 score.
These metrics are calculated for each class, and has the average of following: 
- FalsepositiveRate:0.002319 
- Recall:0.925906
- Precision:0.926199
- F1 score: 0.925523
- Accuracy: 0.925313

Than We use streamlit to create a web app to take the images from user and give predictions with score
