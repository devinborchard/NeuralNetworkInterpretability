Check out Interpretability paper pdf for project results and comprehensive explanation

## Dataset and directories

This project was run through google colab, and as such, the associated project file directories are structured as google drive directories.

The Movies dataset can be found here: https://www.eraserbenchmark.com/
The downloaded 'movies' folder should be put in a google drive directory 'drive/MyDrive/google_colab_data/movies'.

## data_processing

The data_processing.ipynb file is responsible for reading the data from the movies folder, reorganizing and processing it into dataLoaders, and then resaving the data into new files to be accessed later on by the models.

The processed data is saved to the directory 'drive/MyDrive/google_colab_data/'. Three files are saved, one for each of the test set, training set, and validation set. The data_processing.ipynb file can be run top to bottom to achieve this.

## Standard Transformer

The standard tranformer model is made and trained in the std_transformer.ipynb file. The file reads in the saved dataloaders from the data processing file and uses them for training and validation. There is a section in the file 'LOAD PARAMS'. This section will load any pretrained parameters for the model before continuing training. If it is the first time training the model, and no parameters have been saved yet, this section should be skipped. 

After training the models parameters are saved to the google drive directory 'drive/MyDrive/google_colab_data/params_std.txt'.

## Custom Transformer

The customer transformer in the custom_transformer.ipynb file follows the save steps and pattern as the standard transformer

The custom model parameters are saved to the file 'drive/MyDrive/google_colab_data/params_custom.txt'

## Evaluation

After all data is pre-processed, and the models are trained and there parameters are saved, the evaluation.ipynb file can be run. This file will rebuild the models with their trained saved parameters, and use lime and the validation data to calculate the results found in the project report. 

This file can be run all the way through to get results but does take many hours to finish.
