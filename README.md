# Biomedical Text Document Classification

## Dataset

This dataset includes long research papers on cancer, which are classified into 3 categories: 'Thyroid_Cancer', 'Colon_Cancer', and 'Lung_Cancer'.

For the purposes of this project, the data was limited to Thyroid Cancer and Colon Cancer. The dataset has a total of 4911 publications, distributed as:
- Colon cancer: 2322
- Thyroid cancer: 2589

## Preprocessing the Text

The dataset was preprocessed to remove special characters and digits, tokenize the text into words, remove stop words, and lemmatize the words using WordNetLemmatizer. The data was then split into train and test sets, and the labels were converted into numbers. The tokenizer was used to convert the text into a numeric representation, and the sentences were padded to a maximum length of 2830.

## Model Building

The model was built using LSTM layers. The input layer takes the preprocessed text as input, which is then passed through an LSTM layer with 32 units. Batch normalization is applied to the output of the LSTM layer, followed by flattening and dense layers. The output layer uses the sigmoid activation function to produce a binary output.

The model was compiled using the Adam optimizer, binary cross-entropy loss function, and accuracy as the evaluation metric.

## Model Performance

The model achieved an accuracy of 72% on the test set. This could have been improved with larger epochs.

## Prediction

The model was used to make predictions on the test set, and the predictions were rounded to the nearest integer. The final predictions were based on a threshold of 0.5. Confusion matrix was used to evaluate the performance of the model on the test set.

