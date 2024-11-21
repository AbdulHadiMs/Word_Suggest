
# Word suggest App
This is a simple Flask web application that suggests similar words based on a user's input. The suggestions are ranked according to their Jaccard similarity to the input keyword, as well as their probability of occurrence in a given text.



## Overview
The application reads a text file (text.txt), processes the words, calculates the frequency of each word, and computes the probability of each word appearing in the text. When a user enters a keyword, the app finds the most similar words based on the Jaccard distance, showing suggestions with their similarity score and probability.
## Features

- Word Frequency Calculation: Reads a text file and calculates the frequency of each word.
- Similarity Search: Uses Jaccard distance to find words similar to a given keyword.
- Web Interface: A simple web page where users can input a keyword and view suggestions.


## Technologies Used

- Python: Main programming language.
- Flask: Lightweight web framework.
- pandas: Used for handling and manipulating the word frequency data.
- textdistance: Library used for calculating the Jaccard distance between words.
- re: Regular expressions for text processing.
- HTML/CSS: Frontend to display the suggestions.
## Installation
To run this project, you will need to have Python and the required libraries installed. You can follow the steps below:

## 1. Clone the repository:
```bash
git clone https://github.com/yourusername/word-suggestion-app.git
cd word-suggestion-app
```
## 2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate
```
## 3. Install dependencies:
```bash
pip install -r requirements.txt
```
If you don’t have a requirements.txt file, install the necessary libraries manually:

```bash
pip install flask pandas textdistance
```
## 4. Prepare the ```text.txt``` file:
Ensure that you have a ```text.txt``` file in the project directory. This file should contain the text you want to analyze.
## 5. Run the Flask app:
```bash
python app.py
```
The application will be running at ```http://127.0.0.1:5000/.```

## How It Works
- The app loads the contents of ```text.txt```, processes the text, and creates a list of words.
- It computes the frequency of each word and stores it in a dictionary.
- The probability of each word appearing in the text is calculated by dividing the word frequency by the total number of words in the text.
- When a user submits a keyword via the form on the homepage, the app calculates the Jaccard similarity between the input keyword and each word in the text.
- The results are displayed on the webpage, showing the words most similar to the input keyword, sorted by similarity and probability.
## Usage

Navigate to ```http://127.0.0.1:5000/``` in your browser.
Enter a keyword in the input field and submit the form.
The app will display a list of similar words along with their similarity score and probability.
