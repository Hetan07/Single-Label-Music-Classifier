A single-label music genre classifier system based on
the training dataset provided by the [GTZAN](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification) 
Dataset on Kaggle.

This is my initial project and decided to work with traditional machine-learning
algorithms namely:

- K-Nearest Neighbours
- Logistic Regression
- Support Vector Machines

Along with

- A simple Neural Network
- XGB

The source code is provided here for the deployment present on 
Hugging Face.

The deployment is divided into 3 files

- *app.py*: Which has all the code written using streamlit library for the front-end deployment
- *feature_extraction.py* - Which has all the feature extraction code written using librosa library. Any uploaded music sample is processed using this module 
- *audio_splitting.py* - To optimize performance once deployed on the HuggingFace platform I found that feature extraction on the whole music sample runs slowly and instead now this works on using 3 seconds sample (Also the approach used in GTZAN)

The genres classified and predicted are:
- Blues 
- Classical 
- Country 
- Disco 
- HipHop 
- Jazz
- Metal 
- Pop 
- Reggae 
- Rock