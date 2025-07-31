
# 📘 Lesson 3: Creating and Managing Repositories in Git & GitHub

## 🔹 1. What is a Repository?

A **repository (repo)** is like a **project folder** that contains:

* Your code and files

* The complete history of changes

* Configuration for collaboration

* **Local Repository** → stored on your computer

* **Remote Repository** → stored on GitHub (or GitLab/Bitbucket)

---

## 🔹 2. Creating a Local Repository

### Step 1: Create a New Project Folder

```bash
mkdir my-first-project
cd my-first-project
```

### Step 2: Initialize Git

```bash
git init
```

👉 This creates a hidden `.git` folder that tracks changes.

### Step 3: Add a File

```bash
echo "# My First Project" > README.md
```

### Step 4: Stage the File

```bash
git add README.md
```

### Step 5: Commit the File

```bash
git commit -m "✨ Initial commit with README.md"
```

✅ You now have a **local Git repository** 🎉

---

## 🔹 3. Creating a Remote Repository on GitHub

### Step 1: Login to GitHub

* Go to [https://github.com](https://github.com)
* Click **+ → New Repository**

### Step 2: Fill in the Details

* **Repository Name** → `my-first-project`
* **Description** → “My first Git & GitHub project”
* Choose **Public** (anyone can see) or **Private**
* Optionally, check **Add a README file**

### Step 3: Create Repository

👉 Click **Create Repository** button

---

## 🔹 4. Connecting Local Repository to GitHub

GitHub will give you a repository URL.

👉 Using **HTTPS**:

```bash
git remote add origin https://github.com/username/my-first-project.git
```

👉 Using **SSH**:

```bash
git remote add origin git@github.com:username/my-first-project.git
```

### First Push:

```bash
git branch -M main
git push -u origin main
```

---

## 🔹 5. Sending New Changes to GitHub

Whenever you make changes in your local files:

```bash
git add .
git commit -m "✅ Added new feature"
git push
```

---

## 🔹 6. Getting Updates from GitHub

If team members added new changes:

```bash
git pull
```

---

## ✅ Summary

* **Local Repository** → Work on your own computer
* **Remote Repository (GitHub)** → Backup & share code with team
* **Push** → Send code from local to GitHub
* **Pull** → Fetch updates from GitHub to local
