
# 📘 Lesson 4: Basic Git Commands

In this lesson, we’ll cover the most commonly used Git commands to manage repositories, track changes, and collaborate effectively.

---

## 🔹 1. Checking Git Installation

```bash
git --version
```

👉 Shows the installed Git version.

---

## 🔹 2. Configuring Git (First-Time Setup)

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
git config --list
```

👉 Sets your identity for commits.

---

## 🔹 3. Initializing a Repository

```bash
git init
```

👉 Creates a new Git repository in the current folder.

---

## 🔹 4. Cloning a Repository

```bash
git clone <repository_url>
```

👉 Creates a local copy of a remote repository.
Example:

```bash
git clone https://github.com/username/myproject.git
```

---

## 🔹 5. Checking Repository Status

```bash
git status
```

👉 Shows which files are new, modified, or staged.

---

## 🔹 6. Adding Files to Staging Area

```bash
git add <filename>     # Add a specific file
git add .              # Add all changes
```

👉 Prepares files for commit.

---

## 🔹 7. Committing Changes

```bash
git commit -m "Your commit message"
```

👉 Saves the changes permanently in the repository history.

---

## 🔹 8. Viewing Commit History

```bash
git log
```

👉 Shows the list of commits.
For a short view:

```bash
git log --oneline
```

---

## 🔹 9. Branching

```bash
git branch              # Show all branches
git branch <branchname> # Create a new branch
git checkout <branchname>  # Switch to a branch
git checkout -b <branchname> # Create & switch
```

---

## 🔹 10. Merging Branches

First switch to the branch you want to merge **into**:

```bash
git checkout main
git merge feature-branch
```

---

## 🔹 11. Connecting to Remote Repository

```bash
git remote add origin <repository_url>
git remote -v
```

👉 Links your local repo with GitHub.

---

## 🔹 12. Pushing Changes to GitHub

```bash
git push -u origin main   # First time
git push                  # Next times
```

---

## 🔹 13. Pulling Updates from GitHub

```bash
git pull
```

👉 Fetches and merges changes from the remote repository.

---

## 🔹 14. Undoing Changes

### Remove file from staging:

```bash
git reset <filename>
```

### Discard changes in a file:

```bash
git checkout -- <filename>
```

### Go back to last commit:

```bash
git reset --hard HEAD
```

---

## ✅ Quick Reference Table

| Command                  | Description                |
| ------------------------ | -------------------------- |
| `git init`               | Initialize a repository    |
| `git clone <url>`        | Copy a remote repo locally |
| `git status`             | Check file status          |
| `git add <file>`         | Stage changes              |
| `git commit -m "msg"`    | Save changes               |
| `git log`                | View commit history        |
| `git branch`             | List branches              |
| `git checkout <branch>`  | Switch branch              |
| `git merge <branch>`     | Merge branch               |
| `git push`               | Send changes to GitHub     |
| `git pull`               | Get latest changes         |
| `git reset`              | Unstage changes            |
| `git checkout -- <file>` | Discard local changes      |

---

⚡ **Pro Tip:**
Always use `git status` frequently to know what’s happening in your repo.

## **Git Workflow: From Local To GitHub ** : 
<img width="1589" height="1010" alt="Image" src="https://github.com/user-attachments/assets/04e02312-9038-4efe-827f-debc91fbaaf1" />