Here is a clean, professional, GitHub-ready **README.md** for your Python-based AI commit summarizer.

---

# 🧠 AI Git Commit Summarizer

A lightweight Python utility that automatically generates concise, meaningful commit summaries based on your Git changes — powered by the OpenAI API.

This tool analyzes your staged diff (or your last commit if nothing is staged) and produces a **~20-word semantic summary**, perfect for writing clean commit messages or changelogs.

---

## 🚀 Features

* ✨ Automatically summarizes your Git changes
* 📝 ~20-word semantic commit message
* 🧩 Reads **staged changes** (git add) for precise control
* 🔄 Falls back to `HEAD~1..HEAD` if nothing is staged
* ⚡ Uses OpenAI’s `gpt-4o-mini` model
* 💻 Works on Windows, macOS, and Linux
* 🧙‍♂️ Zero configuration required after setup

---

## 📦 Installation

### 1. Install Python dependencies

```bash
pip install openai python-dotenv
```

### 2. Add your OpenAI API key

Create a `.env` file in the same directory:

```
OPENAI_API_KEY=your_key_here
```

### 3. Save the script

Place the `generate_commit.py` file in your project root or anywhere in your PATH.

---

## ▶️ Usage

Inside any Git repo, run:

```bash
python generate_commit.py
```

### Option A: Summarize **staged changes**

```bash
git add .
python generate_commit.py
```

### Option B: Summarize **your last commit**

If nothing is staged, the script automatically uses:

```
git diff HEAD~1..HEAD
```

---

## 📄 Example Output

```
===== Commit Summary =====
Refactored session handler logic, cleaned schema fields, and improved JSON parsing for more stable game state management.
==========================
```

---

## 🧰 How It Works

1. Collects Git diff using:

   * `git diff --cached`
   * Falls back to `git diff HEAD~1..HEAD`
2. Sends the diff to OpenAI
3. Retrieves a clear, concise, semantic summary
4. Prints the result to your terminal

---

## 🧪 Requirements

* Python 3.9+
* Git installed
* OpenAI API key

---

## 🛠 Future Enhancements (optional)

I can add any of these on request:

* 🔧 Auto-commit with generated message
* 🏷 Conventional Commit style output (`feat:`, `fix:`, etc.)
* 🗂 Create `CHANGELOG.md` automatically
* 🖥 Windows `.bat` launcher (click-to-run)
* 🚦 Token usage limiter
* 🎚 Switch between short and long summaries
* 🧪 Detect file types (PHP, JSON, schema, config, etc.)

---

## 🤝 Contributing

Feel free to submit improvements, suggestions, or pull requests.

---

## 📜 License

MIT License — free to use, modify, and distribute.



Just tell me!
