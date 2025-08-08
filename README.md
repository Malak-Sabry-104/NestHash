# NestHash - 🔖 Tag it. Find it.

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)
[![Made with Click](https://img.shields.io/badge/made%20with-Click-orange)](https://click.palletsprojects.com/)

---

Have you ever searched for a file but couldn’t remember its name?
but remembered its contents perfectly?
Or knew the name but had no clue where it was saved? 🗂️🤷‍♀️

- Yeah... same here.

And when things disappear, I’m left wondering: 
- was it deleted, or just hiding somewhere? 🫥🗑️
  
That’s what inspired me to build NestHash — a CLI project born from that everyday struggle. 💡🛠️

---

## 📌 Overview

**NestHash** is a command-line interface (CLI) application built with Python that helps you organize and search your files using hashtags (tags) instead of traditional folders.

The application allows you to **add, update, remove, and search** tags associated with files, making file organization and retrieval faster and more intuitive.

All data is stored locally in a JSON database for quick access and easy portability.

---

## ✨ Features

- **Tag-based organization** – Associate one or more tags with any file.
- **Quick search** – Find files instantly by searching for tags.
- **Non-destructive** – Files are never deleted from your system, only from the local tag database if requested.
- **Cross-platform** – Works on Windows, macOS, and Linux.
- **Simple storage** – Uses a human-readable JSON file as the database.
- **Extensible CLI** – Powered by the Click library for clean, easy-to-use commands.

---

## ✍️ Basic Usage

**Add tags to a file:**

```bash
python tagnest.py tag "C:/Users/Example/file.txt" #urgent #work
```

**Remove a specific tag from a file:**

```bash
pyhton tagnest.py remove "c:Users/Example/file.txt" #urgent
```

**Update all tags for a file:**

```bash
python tagnest.py update "C:/Users/Example/file.txt" #personal #archive
```

**Show all tags for a file:**

```bash
python tagnest.py show "C:/Users/Example/file.txt"
```

**Search for files by tags:**

```bash
python tagnest.py search #work
```

---

## 🗂️ Project Structure

Nothing complicated here — just a clean, easy-to-follow layout:

```
tagnest/
├── tagnest.py           # CLI entry point
├── tags_db.json         # Local JSON tag database
│
├── core/                # Core application logic
│   ├── storage.py       # Read/write JSON database
│   ├── tag_manager.py   # Tagging operations (add/remove/update/delete/search/show)
│
├── utils/               # Helper utilities
│   └── validators.py    # File checks, tag validation
│
├── tests/               # Unit tests for commands
│
├── README.md            # Project documentation
├── requirements.txt     # Dependencies (Click, Colorama, etc.)
└── .gitignore           # Ignore unnecessary files
```

---

## 🛠️ Future Plans

- **Database Upgrade** – Move from local JSON storage to SQLite for better scalability and performance.
- **Tag Suggestions** – Automatically suggest relevant tags using AI/NLP based on file content.
- **Web Dashboard** – Build a browser-based interface to manage and search files visually.
- **Cloud Sync** – Optional sync with Google Drive, Dropbox, or S3 for multi-device access.

---

## 🚀 Getting Started

### 🔧 Installation

Clone this repository (if you haven’t already):

```bash
git clone https://github.com/YourUsername/nesthash.git
cd nesthash
```

Set up a virtual environment (highly recommended):

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

Install requirements:

```bash
pip install -r requirements.txt
```

(Optional) Install development dependencies:

```bash
pip install -r dev-requirements.txt
```

---

## 📜 License

This project is licensed under the **MIT License**.
Permission is granted to use, modify, and distribute this software for personal or commercial purposes, provided that all copies or substantial portions include the original copyright
notice and license.
