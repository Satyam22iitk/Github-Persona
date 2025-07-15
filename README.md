# 🧠 Reddit User Persona Generator

This project generates a text-based **user persona** from any public Reddit profile by analyzing their recent comments and posts.

It was developed as part of the assignment for the **AI/LLM Engineer Intern** role at **BeyondChats**.  
It uses only free, open-source tools — **no paid APIs or LLMs** were used.

---

## 📌 Features

- ✅ Takes a Reddit user profile URL as input
- 🔎 Scrapes up to 100 comments and 50 posts using Reddit API
- 🧠 Analyzes text to extract:
  - Personality traits
  - Interests and hobbies
  - Personal opinions
- 🔗 Cites original Reddit comment/post links
- 📁 Outputs a clean `.txt` file for each user

---

## 🛠 Technologies Used

| Tool         | Purpose                          |
|--------------|----------------------------------|
| Python 3     | Core programming language        |
| PRAW         | Reddit API wrapper (free)        |
| Regex / Logic | Keyword-based persona extraction |
| Colab Support | Also runs on Google Colab        |

---

## 🚀 Getting Started

### 1. Clone this repository
```bash
git clone https://github.com/satyam-civil-iitk/reddit-persona-generator.git
cd reddit-persona-generator
```

### 2. Install dependencies
```bash
pip install praw
```

### 3. Setup Reddit API credentials

Create a Reddit app here:  
🔗 https://www.reddit.com/prefs/apps

Choose:
- App type: `script`
- Name: anything (e.g., PersonaGen)
- Redirect URI: `http://localhost:8080`

Already done. Here's what's used in the script:

```python
reddit = praw.Reddit(
    client_id="8RNsm7uy-KzMuZtfwtwtMg",
    client_secret="w4nW6HYfrc3YsZQ0JXZr9WrSEE4wLA",
    user_agent="script:reddit.persona:v1.0 (by u/Satyam)"
)
```

---

## ▶️ How to Run

```bash
python user_persona_generator.py
```

When prompted, enter a Reddit profile URL like:
```
https://www.reddit.com/user/kojied/
```

✅ The script will:
- Scrape and analyze data
- Print the user persona in the terminal
- Save the result in `personas/kojied.txt`

---

## 📁 Folder Structure

```
reddit-persona/
├── user_persona_generator.py    # Main script
├── personas/                    # Output folder
│   ├── kojied.txt
│   └── Hungry-Move-6603.txt
├── README.md                    # You’re reading this
```

---

## 📄 Sample Output Format

Example: `kojied.txt`

```
USER: kojied

--- GENERATED PERSONA ---

👤 Personality Traits:
- Curious and skeptical [Source: https://reddit.com/r/someplace/comments/abc123]

📚 Interests:
- Loves statistics and gaming [Source: https://reddit.com/r/stats/comments/xyz789]

💬 Opinions:
- Believes AI should be regulated [Source: https://reddit.com/r/tech/comments/xyz001]

🔗 Source Citations:
- https://reddit.com/r/example/comments/abc123
- https://reddit.com/r/example/comments/xyz789
```

---

## ⚠️ Notes

- Only public Reddit profiles are supported
- No external LLMs or paid services used
- Script follows PEP-8 guidelines

---

## 💼 Assignment Compliance Checklist

| Requirement                             | Status |
|----------------------------------------|--------|
| Executable Python script                | ✅ Done |
| `.txt` output files for sample users   | ✅ Done |
| `README.md` with setup & usage         | ✅ Done |
| Free tools only, no paid APIs          | ✅ Done |
| Ready for GitHub submission            | ✅ Done |

---

## 👨‍💻 Author

**Satyam Srivastava**  
3rd Year Civil Engineering  
IIT Kanpur  

---

## ✅ Submission

This repository was created as part of the assignment round for the **AI/LLM Engineer Intern** role at **BeyondChats** via Internshala.

---
