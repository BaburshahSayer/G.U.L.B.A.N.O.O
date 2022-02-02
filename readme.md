# G.U.L.B.A.N.O.O - Just A Rather Very Intelligent System

#### Created and Tested on Linux with Python 2.7

An attempt to make a very simple, Personal Assistant that understands speech as well as text input and is capable of performing tasks other than conversing.
This project is based on AIML 1.0 and uses pyaiml for using the AIML interpreter in python. AIML, is based on pattern matching and this project does not implement any sort of machine learning or language processing.
Combined with a few python scripts, J.A.R.V.I.S now performs quite a few tasks:

- ### Converses, barely.

    **Talk to G.U.L.B.A.N.O.O :** hello<br>
    **G.U.L.B.A.N.O.O :** Well, hello

    G.U.L.B.A.N.O.O WHO Is iron man?<br>
    **G.U.L.B.A.N.O.O :** Iron man is the one who created me.

    **Talk to G.U.L.B.A.N.O.O :** What does JARVIS stand for?<br>
    **G.U.L.B.A.N.O.O :** JARVIS stands for Just A Rather Very Intelligent System

    All conversation is only for the hardcoded patterns, which are quite few. Can be easily extended to add AIML scripts of ALICE and other existing AIs.

- ### Rhythmbox: Play, Pause, Open.

    Uses shell commands to play and pause rhythmbox music.

    **Talk to G.U.L.B.A.N.O.O :** play music<br>
    **G.U.L.B.A.N.O.O :** On it!<br>
    **Talk to G.U.L.B.A.N.O.O :** play music<br>
    **G.U.L.B.A.N.O.O :** On it!<br>
    **Talk to G.U.L.B.A.N.O.O :** please open rhythmbox jarvis<br>
    **G.U.L.B.A.N.O.O :** Right away, sir!

- ### Tells time.
    
    **Talk to G.U.L.B.A.N.O.O :** what time is it?<br>
    **G.U.L.B.A.N.O.O :** The time is 4 43 am

- ### Gives a brief system status.

    **Talk to G.U.L.B.A.N.O.O :** how are you? / System report / System Status<br>
    **G.U.L.B.A.N.O.O :** I am fine, sir. All systems are at 100 percent. Battery percentage: 100%. Battery state: discharging. 265 processes are currently running. Current volume is 30 percent

- ### Suggests Googling for all unrecognized interrogative questions

    **Talk to G.U.L.B.A.N.O.O :** What is IIT, Bombay?<br>
    **G.U.L.B.A.N.O.O :** Do you want me to google that for you?<br>
    **Talk to G.U.L.B.A.N.O.O :** yes<br>
    **G.U.L.B.A.N.O.O :** Right away, sir!  Created new window in existing browser session.

- ### Plays any song, first search result in youtube

    **Talk to G.U.L.B.A.N.O.O :** play me a song<br>
    **G.U.L.B.A.N.O.O :** What song, sir?<br>
    **Talk to G.U.L.B.A.N.O.O :** Alter Bridge Isolation<br>
    **G.U.L.B.A.N.O.O :** On it!  Created new window in existing browser session.

    Uses youtube.py script to find the first search result for the last user input in above case, and opens it in chromium browser.

- ### Searches internet.

    **Talk to G.U.L.B.A.N.O.O :** Google what is the answer to life?<br>
    **G.U.L.B.A.N.O.O :** Right away, sir!  Created new window in existing browser session.<br>
    **Talk to G.U.L.B.A.N.O.O :** Search youtube for Call of Duty<br>
    **G.U.L.B.A.N.O.O :** On it!  Created new window in existing browser session.<br>
    **Talk to G.U.L.B.A.N.O.O :** Search for Navi Mumbai on google maps<br>
    **G.U.L.B.A.N.O.O :** On it!  Created new window in existing browser session.

- ### Changes Wallpaper.

    Keep a set of wallpapers (and nothing else) in G.U.L.B.A.N.O.O/wallpapers directory. wallpaper.py randomly selects one and sets it as the desktop wallpaper by changing the key value using dconf-editor.

    **Talk to G.U.L.B.A.N.O.O :** change wallpaper<br>
    **G.U.L.B.A.N.O.O :** On it!

- ### Launches Programs.
    
    **Talk to G.U.L.B.A.N.O.O :** open nautilus<br>
    **G.U.L.B.A.N.O.O :** Right away, sir!<br>
    **Talk to G.U.L.B.A.N.O.O :** take me to /etc<br>
    **G.U.L.B.A.N.O.O :** Sure thing! (Opens /etc in nautilus)<br>
    **Talk to G.U.L.B.A.N.O.O :** take me home<br>
    **G.U.L.B.A.N.O.O :** Sure thing! (Opens ~ in nautilus)<br>
    **Talk to G.U.L.B.A.N.O.O :** open chromium / open firefox / open calculator / open vlc<br>
    **G.U.L.B.A.N.O.O :** Sure thing!


- ### Other:
    
    Standard replies for unrecognized/unmatched inputs

   **Talk to G.U.L.B.A.N.O.O :** you are dumb<br>
    **G.U.L.B.A.N.O.O :** I don't understand that yet. Maybe you could teach me.<br>
    **Talk to G.U.L.B.A.N.O.O :** no I won't<br>
    **G.U.L.B.A.N.O.O :** I don't know how to answer that. Maybe I could interest you in something else.<br>

    **Talk to G.U.L.B.A.N.O.O :** go to sleep / exit / quit / bye / goodbye

    closes the python script.

## Requirements:

Make sure you install these packages before moving forward to other python libraries-

`sudo apt install libasound-dev portaudio19-dev libportaudio2 libportaudiocpp0 ffmpeg libav-tools`

You can run `pip install -r requirements.txt` to install them all.

Individual packages listed as follows-

- ### AIML (For Pattern Recognition)
    `pip install aiml`

- ### Speech Recognition
    `pip install SpeechRecognition`

- ### PyAudio is required for microphone input
    `pip install pyaudio`

- ### alsaaudio: (For Volume Control, Linux only)
    `pip install pyalsaaudio`

- ### ttsx: (Offline Text to Speech Service)
    `pip install pyttsx`

- ### Optional for Google Text to Speech :
   + #### gTTS: (Google Text to Speech service)
      `pip install gTTS`

   + #### PyGame: (For audio playback with gTTS)
       `pip install pygame`

- ### argparse (For parsing arguments)
    `pip install argparse`

## Installation:

Clone this repository. Change directories to go to that directory. Run the script "script.py" **from the directory containing it**.
Run script as:

`python script.py` : for text mode (default) of input

`python script.py --voice` : for voice mode of input

`python script.py --voice --gtts` : for voice mode of input, with Google Text to Speech enabled

Voice mode may give a series of warnings for numerous reasons, but still might fuction properly.

## Contribution:

A lot can be done with this project. Core AI chatbot like functionality can be added. More python scripts can be associated. Pull requests for any such changes are accepted. Feel free to fork this project and make your own changes too.
