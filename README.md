# 🧠 Flashcard Quiz App

An interactive web-based flashcard quiz application built with **Flask** (Python) and **jQuery**. Users can create decks, modify them, and test their knowledge through a dynamic, one-question-at-a-time quiz interface.

---

## 🚀 Features

- ✅ Deck creation and storage in JSON format
- ✅ Deck selection via dropdown menu
- ✅ One-question-at-a-time quiz flow
- ✅ Real-time answer checking and scoring
- ✅ Clean, responsive UI with custom styling

---

## 🧩 How It Works

1. Flask serves the available decks and their flashcards as JSON via API routes.
2. The user selects a deck and starts a quiz via the frontend.
3. Questions are displayed one at a time. After each answer, the next question is shown.
4. At the end of the quiz, the user is shown their total score.

---

## 🗂️ Project Structure

flashcard-quiz-app/
│
├── app.py                  # Flask app with API endpoints
├── decks/
│   └── decks.json         # List of available deck names
│
├── templates/
│   ├── index.html          # Home page with deck selector
│   └── quiz.html           # Quiz interface
│
├── static/
│   ├── css/
│   │   └── styles.css      # Custom styles for dropdowns, inputs, etc.
│   ├── js/
│   │   └── main.js         # jQuery-powered quiz logic
│   └── assets/
│       └── logo.png        # App logo in navbar
│
└── README.md               # Project documentation

---

## 🧪 Flask Endpoints

python
# Returns a list of available decks
GET /decks

# Returns the cards in a selected deck
GET /decks/<int:deck_id>/cards

---

## 🛠️ Technologies Used

* **Backend:** Python 3, Flask
* **Frontend:** HTML5, CSS3, JavaScript (jQuery)
* **Data Storage:** JSON files (for decks and flashcards)

---

## 🧰 Setup Instructions

### 1. Copy the source files 						// ([compress everything into a .zip file])

- Extract [.zip file name]
- Copy extracted files into target directory

### 2. Install dependencies

bash
pip install flask


### 3. Run the Flask server

bash
python app.py


By default, the app will run at:
👉 'http://localhost:5000'

### 4. Access the app

Open your browser and go to:

text
http://localhost:5000

---

## 📁 Example Deck Format

Each flashcard deck is a JSON file containing a list of question-answer pairs:

json
[
  {
    "prompt": "Are the prompts created by the user?",
    "answer": "Yes, they are. The user provides the prompts when creating their own decks."
  },
  {
    "question": "What about the answers?",
    "answer": "The answers are also provided by the user together with the prompts/questions."
  }
]


'decks.json' should list all available deck names:

json
[
  { "name": "Cardiovascular System", "filename": "anatomychapter1.json" },
  { "name": "Digestive System", "filename": "anatomychapter2.json" }
]


---

## 🧱 Customization

* **Add more decks:** Drop new deck files into the 'decks/' folder and update 'decks.json'.
* **Style the UI:** Edit 'static/css/styles.css' to change the look and feel.
* **Add user features:** Add login, progress tracking, or spaced repetition logic.

---

## 📜 License

This project is personal and intended for my own private use only.

---

## 🙌 Credits

Created by Khattab Salim.