# RNN - Text Sentiment Classification

## Description

This code is about RNN. Given 170000 sentences (**HW4_dataset/train**) on Twitter which we have known whether those sentenses are positive(1) or negative(0) , we have to classify whether the sentence in **HW4_dataset/test** are positive or negative.

## Files

* **HW4_dataset.zip** : The .zip file of the training dataset and testing dataset.
* **HW4_sample_code.ipynb** : The code I train, test, and evaluate
* **SampleCode-pred.csv** : my prediction to the training data
* **report.pdf** : My report

## Usage

Run **HW4_sample_code.ipynb** on Google Colab. It will automatically download **HW4_dataset** and unzip it to derive the training dataset **train.csv** and **train_nolabel.csv** and the testing dataset **test.csv** in it. After training, **model.pth** will be generated. This way, we can deal with the testing data and output our prediction in **SampleCode-pred.csv**.

## What I've done

### Preprocessing

First, I seperated all the words and punctuations in a sentence into a list.

Then, since there may be some uncommon words, such as names, websites, or even typos, appearing in the messages. I removed those words from message. This way, the size of the word bank of the training data can decrease by nearly 50%.

### Embedding

Then, I used Word2Vec to embed all the words in the dataset.

This way, the words with similar meanings (for example, "happy" and "glad") may be represented as similar vectors.

Since each word can be represented as an 1-D vector, so for each sentence, we can use RNN or other models for further training to predict the meanings of the sentences.

### RNN

I chose RNN for training. In fact, RNN, LSTM, and GRU has different structure but all of them can be used to train in cases such as time series or sentences interpretations.

## Performance

The accuracy is 0.73490, which is ranked 53-rd among 65 students, which is not as good as I expected.

In fact, the limitations of RNN is that gradient vanishing or gradient exploding may occur. Due to the different structures, if time permits, maybe trying LSTM or GRU may be a good way to improve my performance. 

