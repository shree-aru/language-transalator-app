# Language Translator App

## 1. Introduction

### 1.1 Problem Statement
In our increasingly connected world, communication across different languages is essential. However, real-time, accurate translation remains a challenge for many users, especially when they lack access to premium online services or need a lightweight, offline solution. Traditional machine translation often relies on heavy cloud infrastructure or word-level translation, which can miss contextual nuances in short, informal sentences.

### 1.2 Project Objective
This project aims to develop a desktop-based, GUI-enabled English-to-French Language Translator App using Python. Leveraging character-level sequence-to-sequence learning via LSTM neural networks, the tool provides users with simple, efficient, and offline translation capabilities. The application is built with a user-friendly interface using Tkinter and is intended for educational, demonstrative, and lightweight practical use.

### 1.3 Expected Outcome
The final product is an interactive desktop application that accepts English input and returns French translations. It includes a trained model, a character-level encoding mechanism, and real-time decoding. The project comes with full source code, training logic, data preparation, and GUI integration, along with documentation for academic, GitHub, or portfolio use.

---

## 2. Features

### 2.1 Offline English-to-French Translation
The app works offline and uses a pre-trained LSTM-based sequence-to-sequence model to generate accurate French sentences from English input.

### 2.2 Character-level Neural Translation
Unlike word-based models, this implementation handles each sentence at the character level. This increases flexibility and helps in learning sentence structure, punctuation, and short inputs.

### 2.3 Real-Time GUI Interaction
The Tkinter-based GUI provides:
- A simple text input for English sentences.
- A live response in French.
- Scrollable text output for longer translations.

### 2.4 Model Trained on 10,000+ Sentence Pairs
The app uses a subset of the **eng-french.txt** dataset consisting of over 10,000 English–French sentence pairs for training.

### 2.5 Modular Architecture
- `langTraining.py`: Handles training and model creation.
- `LangTransGui.py`: Manages the user interface and inference logic.
- `training_data.pkl`: Pickled dictionary of metadata (character sets, max lengths).
- `s2s_model.h5`: Saved trained Keras model.

---

## 3. Installation

### 3.1 Prerequisites
Ensure the following are installed:
- Python 3.x
- pip

### 3.2 Clone the Repository

git clone https://github.com/YOUR_USERNAME/language-translator-app.git
cd language-translator-app

3.3 Install Required Libraries
bash
Copy
Edit
pip install tensorflow scikit-learn numpy
Note: Tkinter comes pre-installed with most Python versions. If missing, install via your system’s package manager.

4. Usage
4.1 Training the Model (Optional)
 -python langTraining.py
This will:

Load and preprocess data from eng-french.txt

Train the encoder-decoder model using LSTM layers

Save the model as s2s_model.h5

Export metadata as training_data.pkl

4.2 Running the GUI App
python LangTransGui.py

4.3 Interacting with the App
Type an English sentence into the input field.

Press Enter or click Send.

View the translated French sentence in the output pane.

5. Technologies Used
Python 3.x – Core programming language.

TensorFlow/Keras – Model training and inference.

Tkinter – GUI framework.

Scikit-learn – Used for character-level encoding via CountVectorizer.

NumPy – Data handling for model input.

6. Project Structure
   
language-translator-app/
├── LangTransGui.py         # GUI and decoder logic
├── langTraining.py         # Model training logic
├── training_data.pkl       # Character metadata
├── s2s_model.h5            # Trained model
├── eng-french.txt          # Dataset
├── README.md               # Documentation
└── model_plot.png          # (Optional) Model architecture visualization

7. Example
Input: How are you?
Output: comment allez-vous ?

8. Contributing
Contributions are welcome! To contribute:

Fork the repo

Create a feature branch: git checkout -b feature/new-feature

Commit changes: git commit -m "Added new feature"

Push and submit a Pull Request

9. Contact
Shreearu Bisoi
📧 shreearubisoi100@gmail.com
🌐 GitHub: https://github.com/shree-aru


