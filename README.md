# Module_13_Challenge
## Alphabet Soup, Analysis using a Neural Network Model
![Screenshot_header](Screenshots/Screenshot_header.png)

## Background
Working as a risk management associate at Alphabet Soup, and the business team receives many funding applications from startups every day. I have been asked to help them create a model that predicts whether applicants will become successful if funded by Alphabet Soup.

The team has forwarded a CSV file containing more than 34,000 organisations that have received funding from Alphabet Soup over the years. This file contains various types of information about the organisations, including whether they ultimately became successful. Using machine learning and neural networks, I used the features in the provided dataset to create a binary classifier model that will predict whether an applicant will become successful.

### What I have created
To predict whether Alphabet Soup funding applicants will be successful, I created a binary classification model using a deep neural network. To do this I;

- Preprocessed data for a neural network model.

- Used the model-fit-predict pattern to compile and evaluate a binary classification model.

- Optimised the model.

I dropped the “EIN” (Employer Identification Number) and “NAME” columns from the DataFrame, because they’re irrelevant for the binary classification model. Encoded the categorical variables of the dataset by using OneHotEncoder, and then placed the encoded variables in a new DataFrame.

Using the preprocessed data, I created the features (X) and target (y) datasets. The “IS_SUCCESSFUL” column in the preprocessed DataFrame should define the target dataset. The remaining columns defined the features dataset. I then split the features and target datasets into training and testing datasets.

I used knowledge of TensorFlow to design a binary classification deep neural network model. This model uses the features of the dataset to predict whether a startup that’s funded by Alphabet Soup will become successful. I considered the number of inputs before determining both the number of layers that the model  contains and the number of neurons on each layer. Then I compiled and fitted the model. Finally, evaluated the binary classification model to calculate the model’s loss and accuracy.

I saved and exported the model to an HDF5 file, and name the file AlphabetSoup.h5.

### Optimising the Neural Network Model
Using knowledge of TensorFlow and Keras, I was able to optimise model however it only slightly improve its accuracy.

## The process

### Preparing the data to be used on a neural network model.

![Screenshot_1](screenshots/Screenshot_1.png)

I then reveiwed the types associated with the columns.

![Screenshot_2](screenshots/Screenshot_2.png)

I dropped the “EIN” (Employer Identification Number) and “NAME” columns from the DataFrame. and reviewed the DataFrame.

![Screenshot_3](screenshots/Screenshot_3.png)

I used `OneHotEncoder` to encode the datasets catergorical variables, and then placed the encoded variables into a new DataFrame.

![Screenshot_4](screenshots/Screenshot_4.png)

I then added the original DataFrames numerical variables to the DataFrame.

![Screenshot_5](screenshots/Screenshot_5.png)

Using the preprocessed data, I created the features (`X`) and target (`y`) datasets. The target dataset was defined by the preprocessed DataFrame column “IS_SUCCESSFUL”. The remaining columns were defined the features dataset.  I then split and processed the data using train_test_split(X, y, random_state=1) and scikit-learn's StandardScaler. I compiled and evaluated a Binary Classification model using a Neural Network. I compiled and fitted the model using binary_crossentropy loss fuinction, the adam optimizer and the accuracy evaluation metric before saving and exporting the model.

I then made two more alternative models;
1. by adding a hidden layer
2. by running 200 epocks

### Original Model Results

![Screenshot_6](screenshots/Screenshot_6.png)

### Alternative Model 1 Results

![Screenshot_7](screenshots/Screenshot_7.png)

### Alternative Model 2 Results

![Screenshot_8](screenshots/Screenshot_8.png)

Results were saved to the AlphabetSoup.h5 file.

As can be seen from the above results, there was only minor amendments to the loss and accuracy results on these alternative models. Further work could be undertaken to amend the original data set and understand its affect on the loss and accuracy of the models.


