## Dependencies

You can install all dependencies by running one of the following commands

You need a [anaconda](https://www.continuum.io/downloads) or [miniconda](https://conda.io/miniconda.html) to use the environment setting.

```python
# Use TensorFlow without GPU
conda env create -f environments.yml 

# Use TensorFlow with GPU
conda env create -f environment-gpu.yml
```

Or you can manually install the required libraries (see the contents of the environemnt*.yml files) using pip.


## Usage


### Run the pretrained model

Start up [the Udacity self-driving simulator](https://github.com/udacity/self-driving-car-sim), choose a scene and press the "Autonomous Mode" button.  Then, run the model as follows:

```python
python drive.py model.h5
```

### To train the model

First you'll need to generate the training data from simulator to train the model.

To record the training data choose a scene and press "Training Mode"button.

Press "R" to select the folder location to save training images. Now again press "R" to start recording.

Drive the car around the track. Press "R" to stop recording and start generating training data from captured images.

Copy/Paste the folder into project directory.

Now run following command to start training on Neural Network.

```python
python model.py
```

This will generate a file `model-<epoch>.h5` whenever the performance in the epoch is better than the previous best.  For example, the first epoch will generate a file called `model-000.h5`.

## Credits

The credits for this code go to [naokishibuya](https://github.com/naokishibuya).



