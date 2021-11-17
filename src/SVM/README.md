## Support Vector(SVM)

Info about the algorithm

## Run

## Required arguments

- Navigate to `src/SVM` directory

  - `--females` number of images of females, maximum amount is 5407.
  - `--males` number of images of males, maximum amount is 4372.

sample command: `poetry run python classify.py --females 1500 --males 1500`

You may adjust the numbers as necessary to experiment with the algorithm.or example increase the number of input images for one group and observe how that affect the precision of the trained model. The input data
will be split into training and test data, where test data share is 0.3.

## Output

Please note that it may take a while to run the experiment. The output is a classification report, and labeled sample images, press enter key to get labels for more images.