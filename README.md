# 🛠️ Project Setup Guide

## 📖 Table of Contents

1. [✅ Prerequisites](#-prerequisites)
2. [🌐 Step 1: Create a Virtual Environment](#step-1-create-a-virtual-environment-)
3. [📦 Step 2: Install Dependencies](#step-2-install-dependencies-)
4. [🔑 Step 3: Configure the Environment Variables](#step-3-configure-the-environment-variables-)
5. [⚙️ Step 4: Connect the Virtual Environment to Jupyter Kernel](#step-4-connect-the-virtual-environment-to-jupyter-kernel-)
6. [▶️ Step 5: Run the Project](#step-5-run-the-project-)
7. [🛠️ Troubleshooting](#-troubleshooting)
8. [📌 Additional Notes](#-additional-notes)

This guide will help you set up and run the project contained in this repository. Follow the steps below to create a virtual environment 🐍, install dependencies 📦, and configure the environment variables 🔐.

## ✅ Prerequisites

Make sure you have the following installed on your system:

- 🐍 Python 3.8 or higher
- 📦 pip (Python package manager)
- 📓 Jupyter Notebook or JupyterLab

---
## Step 1. Clone the repo
**Windows**:
     ```bash
     git clone https://github.com/Esneide23/Transcrition_educative
     ```
   - **macOS/Linux**:
     ```bash
     source .venv/bin/activate
     ```



## Step 2: Create a Virtual Environment 🌐

1. Open a terminal 🖥️ or command prompt.
2. Navigate to the project directory 📂.
3. Run the following command to create a virtual environment:
   ```bash
   python -m venv .venv
   ```
4. Activate the virtual environment:
   - **Windows**:
     ```bash
     .\.venv\Scripts\activate
     ```
   - **macOS/Linux**:
     ```bash
     source .venv/bin/activate
     ```

---

## Step 2: Install Dependencies 📦

With the virtual environment activated, install the required Python libraries 📚:

```bash
pip install -r requirements.txt
```

> **ℹ️ Note:** If `requirements.txt` is not available, install the libraries manually using:
>
> ```bash
> pip install PyPDF2 python-dotenv google-generativeai
> ```

---

## Step 3: Configure the Environment Variables 🔑

1. Create a `.env` file in the project root directory 🗂️.
2. Use the provided `.env.example` file as a template. You can copy it with:
   ```bash
   cp .env.example .env
   ```
3. Update the `.env` file with the required credentials and settings. Example:

````env
API_KEY=your_api_key_here
DATABASE_URL=postgres://user:password@localhost:5432/mydatabase
OTHER_VARIABLE=default_value
``` Example:
   ```env
   API_KEY=your_api_key_here
   DATABASE_URL=your_database_url_here
   OTHER_VARIABLE=your_value_here
````

---

## Step 4: Connect the Virtual Environment to Jupyter Kernel ⚙️

1. Install the `ipykernel` package in the virtual environment:
   ```bash
   pip install ipykernel
   ```
2. Add the virtual environment to Jupyter:
   ```bash
   python -m ipykernel install --user --name=.venv --display-name "Python (.venv)"
   ```
3. Open the Jupyter Notebook or JupyterLab interface 📓.
4. Select the `Python (.venv)` kernel from the kernel options 🔽.

---

## Step 5: Run the Project ▶️

1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Open the `main.ipynb` file 📄.
3. Execute the cells step-by-step ✅.

---

## 🛠️ Troubleshooting

- If you encounter issues with missing dependencies, ensure the virtual environment is activated 🔄.
- Double-check your `.env` file for accuracy and completeness 🔍.

---

## 📌 Additional Notes

- Ensure your `.env` file is not shared publicly to protect sensitive information 🔒.
- For further customization or extensions, refer to the library documentation 📖:
  - [PyPDF2](https://pypi.org/project/PyPDF2/)
  - [python-dotenv](https://pypi.org/project/python-dotenv/)
  - [google-generativeai](https://pypi.org/project/google-generativeai/)

🎉 Happy coding!

