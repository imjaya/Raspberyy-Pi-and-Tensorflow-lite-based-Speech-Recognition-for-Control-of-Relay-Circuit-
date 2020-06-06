Raspberyy Pi and Tensorflow lite based Speech Recognition for Control of Relay Circuit 
======================================================================================

This project is a demonstration on how to use TensorFlow and Keras to train a Convolutional Neural Network (CNN) to recognize the wake word "stop" among other words. In addition, it contains another Python example that uses TensorFlow Lite to run inference on the trained model to recognize the spoken word "stop" on a Raspberry Pi.


Software Prerequisites
--------------
--------------

Install the following dependencies 

TensorFlow

Keras

Jupyter Notebook or (Google Colab) 

TensorFlow Lite inference engine on Raspberry Pi 

Hardware Prerequisites
----------------------
----------------------
Raspberry Pi

Microphone

Led

Relay

Breadboard  

Getting Started
---------------
---------------
Download and unzip the [Google Speech Commands dataset](https://storage.cloud.google.com/download.tensorflow.org/data/speech_commands_v0.02.tar.gz).

**google_speech_commands_to_mfcc.ipynb**  
Convert all speech samples (excluding the _background_noise_ set) to their [Mel Frequency Cepstral Coefficients]  and save them as tensors in a file named `all_targets_mfcc_sets.npz`

**google_speech_commands_mfcc_classifier.ipynb** 
Read the MFCCs from the file made in the first script, build a CNN Model, and train it using the training features (MFCCs) and save the model in the `wake_word_stop_model.h5` file.

**tensorflowflite_model_converter.ipynb** 
to produce a tensorflow lite model

Run the **main.py** script. to see the output (confidence level) of CNN.

Run the **relay.py** script. After connecting the realy and the circuit to the Raspberry pi.


