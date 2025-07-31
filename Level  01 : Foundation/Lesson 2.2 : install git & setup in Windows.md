
# 📌 How to Download and Setup Git in Windows (PC)

## 🔹 Step 1: Download Git

1. Go to the official Git website:
   👉 [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Download will usually start automatically.
3. You’ll get a `.exe` file (e.g., `Git-2.x.x-64-bit.exe`).

---

## 🔹 Step 2: Install Git

1. Double‑click the `.exe` file to start the installer.

2. Follow the installation wizard:

   **Important Settings to Choose:**

   * **Default editor** → Choose *Visual Studio Code* (recommended) or Notepad++.
   * **Path environment** → Select **Git from the command line and also from 3rd‑party software**.
   * **HTTPS transport backend** → Choose *Use HTTPS*.
   * **Line endings** → Choose *Checkout Windows-style, commit Unix-style line endings* (recommended).
   * **Terminal emulator** → Choose *Use MinTTY* (default) for Git Bash.
   * Keep other settings as default unless you know you need customization.

3. Finish installation.

4. After installation, you’ll get:

   * **Git Bash** → a terminal for Git commands.
   * **Git CMD** → Windows Command Prompt with Git.
   * **Integration with VS Code** (if selected).

---

## 🔹 Step 3: Verify Installation

Open **Git Bash** (from Start menu) and run:

```bash
git --version
```

👉 Example output:

```
git version 2.44.0.windows.1
```

---

## 🔹 Step 4: Setup Your Git Identity

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

✅ Check if it saved:

```bash
git config --list
```

---

## 🔹 Step 5: Set Default Branch Name

```bash
git config --global init.defaultBranch main
```

---

## 🔹 Step 6: Enable Colors in Output (Optional)

```bash
git config --global color.ui auto
```

---

## 🔹 Step 7: Setup SSH Key for GitHub / GitLab (Optional but Recommended)

If you want to use SSH (instead of HTTPS):

1. Generate a key:

```bash
ssh-keygen -t ed25519 -C "youremail@example.com"
```

👉 Press Enter for all prompts.

2. Show your public key:

```bash
cat ~/.ssh/id_ed25519.pub
```

3. Copy the output and add it to GitHub/GitLab →
   **Settings > SSH and GPG Keys > New SSH Key**.

4. Test GitHub connection:

```bash
ssh -T git@github.com
```

---

## ✅ Quick Setup Cheat Sheet

```bash
# Verify Git
git --version  

# Set username & email
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"

# Set default branch
git config --global init.defaultBranch main

# (Optional) Generate SSH key
ssh-keygen -t ed25519 -C "youremail@example.com"
```

---

## 🔹 Bonus: Git Integration with VS Code

If you use **Visual Studio Code**:

1. Install [VS Code](https://code.visualstudio.com/).
2. Open VS Code → Extensions → install **GitLens** (for Git super‑powers).
3. VS Code will auto-detect Git if installed correctly.