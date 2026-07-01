# Emotion Detector

Emotion Detector is a web application built with Flask and the Watson NLP
library. It analyzes a given piece of text and returns the intensity scores
for five emotions — anger, disgust, fear, joy, and sadness — along with the
dominant (strongest) emotion detected in the text.

## Project Overview

This project was built as the final assignment for the "Developing AI
Applications with Python and Flask" course. It demonstrates:

- Consuming the Watson NLP Emotion Predict service from Python
- Formatting and returning structured JSON output
- Packaging the application as an importable Python module (`EmotionDetection`)
- Unit testing with `unittest`
- Deploying the application as a web service using Flask
- Handling errors gracefully for blank/invalid input
- Passing static code analysis with `pylint`

## Project Structure

```
emotion_detector/
├── EmotionDetection/
│   ├── __init__.py
│   └── emotion_detection.py
├── static/
│   ├── mystyle.css
│   └── mywebscript.js
├── templates/
│   └── index.html
├── server.py
├── test_emotion_detection.py
├── requirements.txt
└── README.md
```

## How to Run

1. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
2. Start the Flask server:
   ```
   python server.py
   ```
3. Open the app in a browser at `http://localhost:5000` and enter text to
   analyze.

## Running Tests

```
python test_emotion_detection.py
```

## Running Static Code Analysis

```
pylint server.py
```
#######Agar tumhe ye project kabhi bhi apne local machine ya kisi bhi environment mein run karna ho (submission ke baad practice ke liye, ya interview demo ke liye), to steps yeh hain:
1. Prerequisites Install Karo

Python (3.8 ya usse upar) — https://python.org se download karo
Git (agar GitHub se clone karna hai) — https://git-scm.com se download karo

2. Project Lao
GitHub se clone karo:
bashgit clone https://github.com/RAVIRANJANKUSH7/emotion-detector.git
cd emotion-detector
3. Dependencies Install Karo
bashpip install -r requirements.txt
4. Server Chalao
bashpython server.py
Terminal mein dikhega:
* Running on http://127.0.0.1:5000
5. Browser Mein Kholo
Browser mein jaao:
http://127.0.0.1:5000
Text daalo, "Analyze" dabao — result mil jayega.

⚠️ Important Cheez Jo Tumhe Pata Honi Chahiye:
Ye app Watson NLP API (sn-watson-emotion.labs.skills.network) use karta hai, jo sirf IBM Skills Network ke Cloud IDE/lab environment ke andar hi accessible hai. Agar tum ise apne normal laptop pe ya kisi aur server pe chalaoge (bina IBM lab ke), to:

Server to chal jayega
Lekin jab tum text analyze karoge, request Watson API tak jaake fail ho jayegi (connection error ya timeout), kyunki wo endpoint sirf IBM ke internal network se accessible hai

Matlab: Ye project sirf IBM Skills Network Cloud IDE ke andar hi poori tarah kaam karega jaisa tumne abhi dekha. Apne laptop pe agar chalana ho sirf dekhne ke liye ki server start ho raha hai ya code sahi hai, wo kar sakte ho, lekin actual emotion detection result nahi milega bina Watson access ke.
Agar future mein isi tarah ka project apni khud ki service ke saath (bina IBM dependency ke) banana ho, batana — hum koi free/open emotion detection library (jaise transformers ya nltk) use karke wahi kaam kar sakte hain jo kahin bhi chalega.####
