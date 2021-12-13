import pyttsx3
from decouple import config
import os
import webbrowser
USERNAME = config('USER')
BOTNAME = config('BOTNAME')
engine = pyttsx3.init('sapi5')
# Set Rate
engine.setProperty('rate', 190)
# Set Volume
engine.setProperty('volume', 1.0)
# Set Voice (Female)
voices = engine.getProperty('voices')
engine.setProperty('voice', voices[0].id)
# Text to Speech Conversion
def speak(text):
    #Used to speak whatever text is passed to it    
    engine.say(text)
    engine.runAndWait()
from datetime import datetime
def greet_user():
    #Greets the user according to the time
    hour = datetime.now().hour
    if (hour >= 6) and (hour < 12):
        speak(f"Good Morning {USERNAME}")
    elif (hour >= 12) and (hour < 16):
        speak(f"Good afternoon {USERNAME}")
    elif (hour >= 16) and (hour < 19):
        speak(f"Good Evening {USERNAME}")
    speak(f"My name is {BOTNAME}. Please choose from the following options.")
def options():
    speak(f"1 for the Command Prompt, 2 for Google Chrome, 3 for the Made Tech website, 4 to exit.")
if __name__ == '__main__':
    greet_user()
    print("Please choose from the following options: 1 for the Command Prompt, 2 for Google Chrome, 3 for the Made Tech website, 4 to exit.")
    options()
    while True:
        choice = int(input("Enter your number here-->"))
        if choice == 1:
            os.system('start cmd')
        elif choice == 2:
            webbrowser.open("www.google.com", new=1)
        elif choice == 3:
            webbrowser.open("www.madetech.com/", new=1)
        elif choice == 4:
            speak(f"Thank you for using the Jarvis system. Goodbye.")
            print("Thank you for using the Jarvis system. Goodbye.")
            break