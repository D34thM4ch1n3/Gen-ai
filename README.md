# AI Code Explainer (Offline, Local LLM)

This tool allows you to explain code using a **locally hosted LLM** (e.g., Mistral 7B via LM Studio). You can upload a code file and ask questions in plain English.

---

## Features
- Works completely offline using a local LLM
- Supports Python, JavaScript, and other code formats
- Asks and answers questions about any code snippet
- No API key or OpenAI access required

---

## Requirements
- Windows 10/11 or Linux
- Python 3.8+
- [LM Studio](https://lmstudio.ai/) (for running local LLM server)
- Mistral 7B or any GGUF model compatible with LM Studio

---

## 1. Setup Python Environment

### Step 1: Install Python (if not already)
Download from: https://www.python.org/downloads/

Make sure to check "Add Python to PATH" during installation.

### Step 2: Install dependencies
Open a terminal or command prompt:

```bash
pip install -r requirements.txt
```

---

## 2. Setup LM Studio (for Local LLM)

### Step 1: Download & Install LM Studio
Download from: [https://lmstudio.ai](https://lmstudio.ai)

### Step 2: Download a GGUF Model (e.g., Mistral 7B)
Inside LM Studio:
1. Go to the **"Models"** tab
2. Search for: `Mistral 7B Instruct GGUF`
3. Click **Download**

### Step 3: Run the Model as a Server
1. Go to **"Local Server"** tab (bottom left of LM Studio)
2. Select the model you downloaded
3. Click **Start Server**
4. Ensure it's running on `http://localhost:1234`

---

## 3. Using the Code Explainer

### Step 1: Prepare your code file
Place your code file in the same folder or in `sample_code/`

Example: `example.py`
```python
def greet(name):
    return f"Hello, {name}!"
```

### Step 2: Run the Script
```bash
python code_explainer.py sample_code/example.py
```

### Step 3: Ask your question
You'll be prompted to ask something about the code. Example:
```
Ask something about the code: What does this function do?
```

You’ll get a detailed explanation from the local LLM.

---

## 4. Customize

You can edit the script to:
- Add voice support (e.g., using `speech_recognition`)
- Add a GUI (e.g., using `tkinter` or `PyQt`)
- Extend to multi-file projects

---

## Troubleshooting

- If the LLM doesn’t respond:
  - Check LM Studio is running
  - Make sure `http://localhost:1234` is correct
- If you see errors about dependencies:
  - Ensure `requests` library is installed via `pip install requests`

---

## License

This project is free to use and modify. No attribution needed.

