# Latexify-Handwriting

## Introduction
Handwritten Mathematical Expressions Recognition (HMER) is the field of converting handwritten mathematical expressions to their LaTeX representation –this is the goal of our project. This project is useful because scientific documents have been handwritten for centuries, but currently, the main source of communication is the Internet; it is therefore important to have a tool that can convert expressions into a compatible representation. Machine learning is an appropriate tool because we need to classify several characters, which can be done by training a deep network with a large dataset of labelled characters. 

Our model carries support for over 89 characters, including integrals, fractions, trigonometric equations, as well as subscripts and superscripts. 

## How It Works
![Optional text](../master/Images/model-picture.JPG?raw=true)

Full overview of model starting from handwritten image to final LaTeX representation.

## Model Architecture
We used ResNet34, one of the best models used for object classification. We fine-tuned ResNet34 and re-trained it on our dataset to update the parameters. ResNet34 has 34 layers in total, with 5 types of convolutional layers, followed by a DRF and a fully-connected layer. We added the linear fully-connected layer to account for the 89 output features that we have. Through rigorous hyperparameter tuning, we decided on selecting the following hyperparameters: batch size of 1000, number of epochs to 30, weight decay of 0, and learning rate of 0.001. We utilized the Adam Optimizer, and kept the original ReLU activation function.

## Results
The highest training accuracy achieved was 99%, validation accuracy is 97% and test accuracy of 95.7%.

![Optional text](../master/Images/Accuracy.JPG?raw=true)

The following are results from challenging equations.

![Optional text](../master/Images/Fractions.JPG?raw=true)

![Optional text](../master/Images/Special.JPG?raw=true)

![Optional text](../master/Images/Superscript.JPG?raw=true)

![Optional text](../master/Images/Trig.JPG?raw=true)
