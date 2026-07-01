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
