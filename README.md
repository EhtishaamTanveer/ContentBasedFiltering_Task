# Content-Based Movie Rating Prediction with Deep Learning

### Description

This repository implements a content-based movie rating prediction system using deep learning. It aims to predict user ratings for new movies based on their titles, descriptions, and genre information. A deep learning model is developed using tensorflow that will learn the patterns using prior movie data to predict ratings of new movies in the test dataset.

I started working on this project all by myself while completing my Coursera specialization called "[Machine Learning Specialization](https://www.coursera.org/account/accomplishments/specialization/NG3GPTVN7M8E?utm_source=link&utm_medium=certificate&utm_content=cert_image&utm_campaign=sharing_cta&utm_product=s12n)"

### How Content-Based Filtering works?

Similar to Collaborative Filering, Content-based filtering also generates a user and movie feature vector but recognizes there may be other information available about the user and/or movie that may improve the prediction. The additional information is provided to a neural network which then generates the user and movie vector.

### Benefits

- Recommends New Movies: Accurately suggest movies to users based on their genre and description preferences.
- Cold Start Problem Mitigation: Predicts ratings for new movies even when user ratings are unavailable.

### Insight on the Dataset

The dataset I derived for the sake of this project was derived from [MovieLens "ml_dataset_small" dataset ](https://grouplens.org/datasets/movielens/latest/) 

Although the original dataset has **9000 movies** and **600 users**, I have roughly halved it to reduce computation. Now, my dataset has **694 movies** and **395 users**

- The movie content provided to the network is a combination of the original data and some 'engineered features'.

- The original features are the year the movie was released and the movie's genre presented as a one-hot vector. There are 14 genres. 

- The engineered feature is an average rating derived from the user ratings. Movies with multiple genre have a training vector per genre. 

**NOTE: The user content is composed of only engineered features.**
