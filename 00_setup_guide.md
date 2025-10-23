# Large Language Models for Research - QCIF
Author: Moji Ghadimi https://www.linkedin.com/in/moji-ghadimi/

<br>
<br>
<br>


# Setup Guide for Python and JupyterLab

This guide explains how to install **Python**, **essential packages**, and **JupyterLab** for running the LLM workshop notebooks on your computer or HPC environment.

---

## 🐍 1. Install Python (Recommended: Version 3.10 or newer)

### **Windows**

1. Go to the official Python website: [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Download the latest **Python 3.x installer**.
3. Run the installer and **check the box** that says:

   * ✅ *Add Python to PATH*
4. Choose *Install Now* and follow the prompts.

To verify installation, open **Command Prompt (cmd)** and type:

```bash
python --version
```

You should see something like:

```
Python 3.11.6
```

---

### **macOS / Linux**

Most systems come with Python preinstalled. You can check your version:

```bash
python3 --version
```

If Python is not installed, install it using your system package manager:

**macOS (Homebrew):**

```bash
brew install python
```

**Ubuntu / Debian:**

```bash
sudo apt update && sudo apt install python3 python3-pip -y
```

---

## 📦 2. Install jupyterlab

Once Python is installed, you can install packages using `pip` (Python’s package manager).

Run this command in your terminal or command prompt:

```bash
pip install jupyterlab
```

---

## 🧠 3. Launch JupyterLab

Open terminal or command prompt and navigate to the folder containing your workshop notebooks (or navigate then open), then run:

```bash
jupyter lab
```

This will open a new tab in your default web browser with the JupyterLab interface.

You can then click on any notebook to open it.

---

## ⚙️ 4. Running on HPC

If you’re using a hosted JupyterLab instance on HPC infrastructure, Python and most dependencies are already installed. You typically only need to:

1. Open the web-based JupyterLab interface.
2. Load the correct Python environment (via module or dropdown).
3. Start a notebook directly.

## 📦 5. Install Required Python Packages

Open a notebook and in a cell run the command below to install packages:

```Python
!pip install pandas matplotlib openai rank-bm25 requests 
```

This will install:


* `numpy` – for handling arrays.
* `pandas` – for handling data.
* `matplotlib` – for plotting.
* `openai` – to connect to Groq or OpenAI-compatible APIs.
* `rank-bm25` – for retrieval-based tasks.
* `requests` – for fetching data from APIs.
* `jupyterlab` – for running notebooks interactively.

To verify installation:

```bash
pip list | findstr "numpy pandas matplotlib openai rank-bm25 requests"
```

You should see all packages listed.

---

## ✅ Summary

* Install Python ≥ 3.10
* Use `pip` to install required packages
* Run `jupyter lab`
* Verify everything by opening the example notebooks


