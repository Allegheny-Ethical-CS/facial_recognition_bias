
## Run

## Required arguments

- Navigate to `src/CNN` directory.

  - `--females` number of images of females, maximum amount is 5407.
  - `--males` number of images of males, maximum amount is 4372.

sample command: `poetry run python CNN.py --females 1500 --males 1500`

You may adjust the numbers as necessary to experiment with the algorithm or increase the number of input images for one group and observe how that affect the precision of the trained model. The input data
will be split into training and test data, where test data share is 0.3.

NOTE: it might take a little while to get the output

## Output

The output is a classification report.

(https://www.tensorflow.org/tutorials/images/cnn)