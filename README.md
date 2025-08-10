# 📝 To-Do List App

A simple and efficient **To-Do List** application to help you manage your daily tasks.  
Built with **Python Flask** (can be adapted to any stack) and integrated with **GitHub Actions** for Continuous Integration.

---

## 📌 Features
- Add, edit, and delete tasks
- Mark tasks as completed
- Persistent storage of tasks
- Clean and user-friendly interface
- Automated testing with GitHub Actions

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/username/todo-list.git
cd todo-list
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 💻 Usage

Run the app locally:
```bash
python app.py
```

Open your browser and go to:
```
http://localhost:5000
```

---

## 🔄 Git Workflow

### Create a New Branch
```bash
git checkout -b feature-name
```

### Stage, Commit, and Push Changes
```bash
git add .
git commit -m "Your commit message"
git push origin feature-name
```

---

## 🤖 Continuous Integration (CI) with GitHub Actions

This project uses a **GitHub Actions workflow** to automatically:
1. Install dependencies
2. Run tests
3. Ensure the app is stable before merging changes

Workflow file: `.github/workflows/ci.yml`

Example for Python:
```yaml
name: Python CI

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v3
    - name: Set up Python
      uses: actions/setup-python@v4
      with:
        python-version: "3.10"
    - name: Install dependencies
      run: |
        pip install -r requirements.txt
    - name: Run tests
      run: |
        pytest
```

---

## 📂 Project Structure
```
todo-list/
│
├── app.py               # Main application file
├── templates/           # HTML templates
├── static/              # CSS/JS files
├── requirements.txt     # Python dependencies
├── tests/               # Unit tests
└── .github/
    └── workflows/
        └── ci.yml       # GitHub Actions workflow
```

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
