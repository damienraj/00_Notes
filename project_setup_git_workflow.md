# Python Project Setup and Git Workflow

---

## 1. Starting a New Project

### Typical Folder Structure

```
~/projects/
├── project_a/
│   ├── venv/             ← Project-specific virtual environment
│   ├── main.py
│   ├── utils.py
│   ├── requirements.txt  ← List of packages for this project
│   ├── README.md         ← Project description
│   ├── data/             ← Store raw or processed data
│   ├── tests/            ← If you write test scripts
│   └── results/          ← Output files, charts, etc.
│
├── project_b/
├── project_c/
├── ....
```

---

### Steps to set up

1. **Create your project folder and navigate into it:**

```bash
mkdir my_project
cd my_project
```

2. **Create a Python virtual environment:**

```bash
python -m venv venv
```

3. **Activate the virtual environment:**

- On Windows (PowerShell):

```powershell
.\venv\Scripts\Activate.ps1
```

- On macOS/Linux:

```bash
source venv/bin/activate
```

4. **Create essential files:**

```bash
echo "# My Project" > README.md
echo "venv/" > .gitignore
```

5. **Initialize a Git repository:**

```bash
git init
```

6. **Create initial commit:**

```bash
git add .
git commit -m "Initial commit - project structure and venv setup"
```

7. **List committed files:**

```bash
git ls-files
```

---

## 2. Pulling an Existing GitHub Repo

1. **Clone the repo:**

```bash
git clone https://github.com/yourusername/yourrepo.git
cd yourrepo
```

2. **Create and activate a virtual environment (if not included):**

```bash
python -m venv venv
# activate venv as above
```

3. **Install dependencies from requirements.txt:**

```bash
pip install -r requirements.txt
```

4. **Start coding!**

---

## 3. Starting from Scratch: Installing Libraries and Pushing to GitHub

1. **Install libraries as needed:**

```bash
pip install numpy matplotlib pandas  # example libraries
```

2. **Generate `requirements.txt` file to record dependencies:**

```bash
pip freeze > requirements.txt
```

3. **Stage and commit your files:**

```bash
git add .
git commit -m "Add requirements and initial code"
```

4. **Add remote GitHub repo (if not done):**

```bash
git remote add origin https://github.com/yourusername/yourrepo.git
```

5. Name main branch as "main":

```bash
git branch -m main
```

6. **Push your commits:**

```bash
git push -u origin main
```

---

### Notes:

- Always activate your virtual environment before installing packages or running Python code.
- Keep `.gitignore` updated to exclude files/folders like `venv/`, `__pycache__/`, and results/output folders.
- Use descriptive commit messages to track changes effectively.

---

*Happy coding!* 🚀
