# AI-Voice-Assistant
Interactive voice assistant that can take limited voice commands and perform actions automatically.

# Functionality

* It is an interactive utility which can take voice commands and even has functionality to train your model to recognize commands from specific users only (voice recognition).
* Once voice recognition is done, it has functionality to recognize specific key words in sentences and perform automatic actions accordingly.
* It can play music from your local directory, it can play music from web.
* You can command it to tell weather, search something from wikipedia and speak the output (limited sentences).
* It has a functionality to detect your expression, age using trained Neural Networks and play songs accordingly.

# Packages Used

* pyttsx3
* datetime
* speech_recognition
* sounddevice
* scipy
* Numpy
* librosa
* Pandas
* sklearn
* keras
* wikipedia
* webbrowser
* multiprocessing
* playsound
* selenium
* mutagen
* time
* random
* os

# Steps Involved

* The code makes use of **pyttsx3** for text to speech functionality.
* Method **speak()** takes in text and converts that text to speech.
* Method **greet()** captures the current time and greets accordingly.
* **takeCommand()** uses speech_recognition library to recognize what user is saying.
* **take_voice_sample()** this method is used to record the input voice of the user and store it as a .wav file. This method is used only for the purpose of training voice recognition model.
* Method **parser()** is used to parse the .wav voice samples to tabular data which can be used to train voice recognition model. **data_processing_for_model()** method returns the final processed data.
* **train_voice_model()** creates and saves the model as .h5 and returns the Neural Network model for training voice samples.
* Then we have **authenticate()** method, which is optional. It is simply used to authenticate the user with their voice from the model trained in steps above.
* **detect_expression_and_age()** method takes input from default webcam and detects face, determines expression and age and displays the text accordingly.
* I have a separate repository which explains how to train a model for human facial expression detection (Please refer it, if required).
* Finally, the driver code uses the above methods depending on the keywords in the user's sentence.



