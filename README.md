# gspeech-rec

### A demonstration of Google's Speech Recognition API v2.

**speech-rec.sh** is a bash script that sends a flac audio file to Google for speech recognition and prints the N-best returned hypotheses.

More interestingly, if you have **parecord** and **timeout** installed on your machine, you can use the script interactively to record and utterance and get its transcription.

# Some examples

### Recognize speech in audio file
    ./speech-rec.sh -i record.flac --rate 16000

### Try other languages (default=en-US):
**French**

    ./speech-rec.sh -i record.flac --rate 16000 --language fr-FR

**Spanish**

    ./speech-rec.sh -i record.flac -r 16000 -l es-ES

### Simply say something and get (hopefully) what you've said
    ./speech-rec.sh
   
### Talk for 7 seconds (default=3)
    ./speech-rec.sh -d 7
   
The script writes audio data into an audio file named **record.flac** and doesn't delete it afterwards so you can listen to what you said.
To play the audio file, type:

    paplay record.flac
   
# Requirements
### Google API Key
The included key is only to be used for test purposes. It may be disabled by Google anytime. You should generate and use your own API key (follow this link for key generation instructions: http://www.chromium.org/developers/how-tos/api-keys)

#### parecord
To record and play audio data

#### timeout
To stop **parecord** after the required duration

#### wget
To send data to server


# Python API
https://github.com/Uberi/speech_recognition/

# Author
amsehili <amine.sehili@gmail.com> ([Mohamed El] Amine Sehili)

# License
Copyright (C) Amine Sehili 2015.

This program is available under the GNU GENERAL PUBLIC LICENSE Version 2.

Source code on GitHub: https://github.com/amsehili/gspeech-rec


