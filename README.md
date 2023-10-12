# Audio Processing with Python- Speech Recognition
An application is based  Mozilla DeepSpeech library to create an offline automatic speech recognition. Importing DeepSpeech allows the use of speech models to train and recognize speech patterns across various languages.
- JiWER is a python library that calculates the word error rate(WER) of the application
- The models folder is the **important** part as it contains the text-to-speech deepspeech model that has been trained over time by the community and is essential


### The application contains voice recordings of 3 diff languages ( English, Spanish and Italian)
The audio files are recorded in vaious noisy envionments and speeds making it difficult to understand what it is trying to say, even for native speakers
- The purpose of the application is to create a light-weight solution of speech recognition that is able achieve high accuracy constantly across various environments.
- It could Improve the current `text-to-speech` capabilities of many on the market applications
- It gets exponentially difficult for other languages except ENG since the speakers will speak much faster, this is great to train the model

### [Methods used]
The segments that are commented out below are the methods I used for various languages and compare the speech and the text it is supposed to mean.

**[ENG]**
-There is not much to change since the WER score is pretty high and the model is able to recognize most of the words spoken.

**[SPANISH]**
- Use noisereduce library to remove background noises
- Use low-pass filter to remove any high freq noises that are above the human speech range

**[ITA]**
- Add a 1 second buffer for each word spoken since the italian language is spoken too fast for the algorithm
- It gives the algorithm more time to recognize the words
