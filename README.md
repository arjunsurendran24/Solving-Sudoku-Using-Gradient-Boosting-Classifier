<h2>Solving Sudoku using Gradient Boosting Classfier<h2>

<h3>Model Description</h3>

In this notebook I am attempting to formulate a semi-machine learning model that can predict the value of a particular cell of the puzzle.

The dataset for training is obtained from Kaggle : https://www.kaggle.com/bryanpark/sudoku

I am training a classifier whose input contains 26 features and output is a single value, the value of predicted cell. The 26 features consist of 8 values in same row, 8 values in same column, 8 values in same box, and 2 values which indicate position of the cell in the puzzle(row,column). For training, data is taken from 1000 puzzles and their solutions. It is split in a ratio 9:1, and 1 part is used as dev set. The data is further tested on 5000 examples. For improving accuracy, the output is fitted into puzzle and given as input again till further predictions make no change.

The classifier used is Gradient Boosting Classifier, and learning rate chosen is 0.1. Accuracy is defined as no. of correct predictions out of no. of blank spaces. The model gave an accuracy of 73% on dev set.(With output not fitted into input).

<h3>Acknowledgements</h3>

I am grateful to Bryan Park for sharing this dataset.
https://www.kaggle.com/bryanpark/sudoku
