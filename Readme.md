# Data Engineering Project Setup

This guide walks you through setting up a data engineering project from scratch using **GitHub**, **WSL**, a **Python virtual environment**, and installing dependencies.

---

## 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository (e.g., `data-engineering-projects`).
2. Clone the repository to your local machine using WSL:

```bash
# Navigate to your desired folder
cd ~/Documents

# Clone the repository (replace URL with your repo URL)
git clone https://github.com/your-username/data-engineering-projects.git

# Enter the project folder
cd data-engineering-projects

# Activate WSL and open vs code
wsl
code .
```

## 2. Install venv Module in WSL

```bash
# Update package lists
sudo apt update

# Install the venv module for Python
sudo apt install python3-venv -y

# You may be prompted for your WSL password.
```

## 3. Create and Activate a Virtual Environment
```bash
# Create a virtual environment named .venv
python3 -m venv .venv

# Activate the virtual environment
source .venv/bin/activate

# Your terminal prompt should now show (.venv) indicating the virtual environment is active.
```

4. Create requirements.txt and Install Dependencies

```bash
# Create a requirements file with the requests module
echo "requests" > requirements.txt

# Append pandas module
echo "pandas" >> requirements.txt

# Install all dependencies from the requirements file
pip install -r requirements.txt
```

## 5. Verify installations:

```bash
pip show requests
pip show pandas
```

## 5. Deactivate Virtual Environment (Optional)

```bash
deactivate

# This returns your terminal to the system Python environment.
```

## 6. Notes & Best Practices

```bash
# Adding more packages later:

echo "package-name" >> requirements.txt
pip install -r requirements.txt

# Always activate your virtual environment before working on the project to ensure dependencies are isolated.
# Keep requirements.txt up to date to make your project portable and reproducible across machines.
```