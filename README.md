# Assignment-0
Step-by-step Guide to MNIST Image Classification with Keras


# Assignment Zero: MNIST Classification

In this assignment, you will implement Python code to perform classification on the MNIST dataset
using the deep learning framework Keras. There are two parts to this assignment. InPart I,your
main goal will be to simply get the code running. Hopefully this will build your confidence to move
on to the next part. InPart II, you will “tease” apart the code fromPart I, section by section,
with the objective being to better understand how the code works.

# Part I: Create and Run a Python Notebook

1. Navigate tohttps://colab.research.google.com/and select ”New Notebook” as in the
    following figures.
2. Navigate to https://keras.io/examples/mnist_cnn/. Copy and paste the code into the
    first ”cell” of the Colab Notebook.
3. On the first line, add in the statement
    import numpy as np
4. Immediately following the line containingepochs = 12, add the line
    np.random.seed(0)
    Keras gets its source of randomness from numpy’s random number generator. To ensure
    reproducible results, this starts random computation off at the same place every run.


5. Immediatelyfollowingthe line containing
    model.add(Dense(num classes, activation=’softmax’))andbeforethe line containing
    model.compile..., add the line
       print(model.summary())
    This will print a summary of your model’s architecture and parameters.
6. Change the line that hasmodel.fit(...to

```
history = model.fit(...
```
7. Delete the last three lines of code, i.e. score = ...,print(’Test..., andprint(’Test... and
    replace them with
       print([(key, round(value[0], 4)) for key, value in history.history.items()])
8. To run the code, press the PlayIbutton as shown inFigure 3.

```
Figure 3. Run Colab Notebook Code
```
9. If your code runs, congratulations!! Your output should look like the Output.txt file that is
    with this document. If your code doesn’t work or your output doesn’t match, try re-tracing
    your steps and making sure you did everything correctly. If that doesn’t work, try Googling
    the error message(s) you are receiving.


# Part II: Understanding Part I

InPart Iyou successfully ran Python code which uses a Convolutional Neural Network to classify
the images in the MNIST dataset. For many of you, that probably doesn’t make a lot of sense. So
our goal in this part of the assignment will be to take a closer look at what’s happening in the code
fromPart I. I have added some additional lines to the code you will be examining. These serve
only as aides to better illustrate the concepts therein.

To get started, you will need to be signed in to your Google account. Once signed in, navigate
to the Colab Notebook athttps://bit.ly/2Yqiqjnand select the “Save a copy in Drive” op-
tion under the “File” Menu. Once you have done that, the file name should now be “Copy of
KerasMNIST.ipynb” and you can run the first cell, as shown inFigure 4below.

```
Figure 4: Save a Copy and Run First Cell
```
Once you’ve run this cell, the empty square brackets at the left of the cell should now read [1] (see
Figure 5), as opposed to [ ] before we ran the cell (e.g. look at cell 2 inFigure 5, it’s [ ] because
it hasn’t been run yet).

From here, you will simply go cell by cell, running each and observing the output. I have included
some notes and code block titles to try and help with the break down. I would suggest reading each
line in an individual cell and try to make sense of what it is doing. The shortcut to run a cell is
Shift + Enter, which should make it a little smoother to work your way through.


Lastly, don’t forget, you made a copy of this Notebook, so feel free to make asmany changesas
you want. If it helps, you can add print statements after every single line! Good luck and have fun!


![Alt text](Misc/after_run.png?raw=true "Title")


