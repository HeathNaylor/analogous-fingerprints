# Analogous Fingerprints (Research)

This is a research project to investigate and determine if a Convolutional Neural Network (CNN) can be used to associate never before seen fingerprints with known individuals that have only had a single fingerprint scanned before.

## Dataset
This project plans to use the [Sokoto Conventry Fingerprint Dataset](https://arxiv.org/abs/1807.10609) to train the model.


## Process

The dataset contains 6,000 fingerprints for 600 individuals

We will split the data as follows:
- `x_train` = 5,400 finger prints (One finger print omitted for each subject)
- `Y_train` = 5,400 labels (One finger print omitted for each subject)
  - These will be one-hot encoded for each of the 600 individuals
- `x_test` = 600 finger prints (the omitted one)
- `Y_test` = 600 labels (the omitted one)
  - These will be one-hot encoded for each of the 600 individuals

- The input layer will be the the raw image pixels passed through several convolutional, pooling, and dense layers
- The output layer will be a softmax layer with 600 outputs.
