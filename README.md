# Image-classification-In-Pyspark-and-Elephas

## Technologies Used

**PySpark** is a Python API (Application Programming Interface) for Apache Spark, which is a fast and general-purpose distributed computing system for Big Data processing. It provides an interface for programming Spark with Python instead of Scala or Java, which makes it easier for data scientists and developers to use Spark for large-scale data processing and machine learning.

PySpark allows users to leverage the power of Spark's distributed computing framework using Python syntax, which is a popular language among data scientists and developers for its simplicity and ease of use. With PySpark, users can easily manipulate large datasets, perform complex data transformations, and build scalable machine learning models.

**Elephas** is a distributed deep learning library built on top of Spark, which is a popular big data processing engine. Elephas enables distributed training of Keras deep learning models on Spark clusters, making it ideal for large-scale machine learning applications. It allows users to scale their deep learning models to big data and take advantage of distributed computing resources.
Detection of diseases a plant may have based on the images of the leaves.

**Streamlit** is an open-source Python library used for building interactive data science and machine learning web applications. It allows data scientists and developers to quickly and easily create web applications that can display data, models, and visualizations in a user-friendly way.

## Details of the problem statement

• The leaves on a plant are like a barometer. They can tell you what is happening to the plant.So given labeled images of plant leaves,we use Machine learning to detect if a plant is healthy or not.

• The dataset contains RGB images of leaves from different plants facing from different diseases. There are a total of 38 classes in this dataset. But for our task, we have used 33 classes which span over 9 plant species. The training set contains total of 58579 images, out of which 80 percent are used while training and 20 percent as validation set. The testing set contains total of 15231 images.

• The images are resized into size of 24x24 and flattened to store in pyspark dataframe which gives us total of 1728 features.Next,A neural network model that:

- Reshape the data from flat list to original shape
- Has Convolutional neural network model for feature extraction.
- Fully connected layers for classification
  

## Results


Various metrics are used to evaluate the model on test set, these are: False positive Rate, Recall, Precision and f1 score.
These metrics are calculated for each class, and has the average of following: 

- False positive Rate:0.002319 
- Recall:0.925906
- Precision:0.926199
- F1 score: 0.925523
- Accuracy: 0.925313

Than We use streamlit to create a web app to take the images from user and give predictions with score
