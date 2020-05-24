# SpeechRecognition-in-Python
#My very first python project I built with lessons from Brad(Traversy Media)

#first in the terminal, we need to import SpeechRecognition and Py Audio

python3 -m venv venv
source venv/bon/activate

import speech_recognition as sr

r = sr.Recognizer()

with sr.Microphone() as source:
    print("Say something")
    audio = r.listen(source)
    voice_data = r.recognize_google(audio)
    print(voice_data)
