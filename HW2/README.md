\# CNN - Face Expression Recognition

## Description

This code is about CNN. The training data is 25000 labeled pictures of human faces, and we need to use them to predict the expressions (anger, disgust, fear, happy, sad, neutral, and shocked) in the testing data.

## Files

* **best_model.ipynb** : The code I train, test, and evaluate
* **early_stop.ipynb** : The code I train, test, and evaluate with early-stopping.
* **predict.csv** : the file of my model's prediction to the testing data
* **report.pdf** : My report

## Usage

Run **best_model.ipynb** on Google Colab. It will automatically download the dataset **HW2.zip** and unzip it into **data**. After training, **model.pth** will be generated, and we can use it to generate  **predict.csv**.

## What I've done    

### Preprocessing

First, for all pictures, I enlarge the contrast of the colors of all pictures to make them more trainable for the machine.

Then, since the pictures may be somewhat tilted, and the sizes of the faces in those pictures are also distinct. Thus, adjusting them is also necessary.

### Training
I used CNN to train. I used nn.Conv2d -> nn.BatchNorm2d -> nn.LeakyReLU ->.nn.MaxPool2d for several layers and then finally nn.Linear. 

I also implemented early-stopping in **early_stop.ipynb** to save time.

## Performance

The training accuracy is 0.6976.
The validating accuracy is 0.6182.
The testing accuracy is 0.63266, which is ranked 42-nd among all 77 students.
