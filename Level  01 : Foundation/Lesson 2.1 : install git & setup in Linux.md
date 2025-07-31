
# 📌 How to Download and Setup Git in Linux (PC)

## 🔹 Step 1: Check if Git is Already Installed

```bash
git --version
```

👉 যদি version number দেখায়, তাহলে Git already installed আছে।
👉 না থাকলে নিচের steps follow করুন।

---

## 🔹 Step 2: Install Git

### ✅ For Ubuntu / Debian based Linux

```bash
sudo apt update
sudo apt install git -y
```

### ✅ For Fedora

```bash
sudo dnf install git -y
```

### ✅ For CentOS / RHEL

```bash
sudo yum install git -y
```

### ✅ For Arch Linux / Manjaro

```bash
sudo pacman -S git
```

---

## 🔹 Step 3: Verify Installation

```bash
git --version
```

👉 Example output:

```
git version 2.39.2
```

---

## 🔹 Step 4: Setup Your Git Identity

Git commits কে কে করছে তা জানার জন্য আপনার নাম আর ইমেইল দিতে হবে।

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

👉 Check if they are saved:

```bash
git config --list
```

---

## 🔹 Step 5: Setup Default Branch Name (Optional but Recommended)

```bash
git config --global init.defaultBranch main
```

---

## 🔹 Step 6: Enable Colored Output (Optional)

```bash
git config --global color.ui auto
```

---

## 🔹 Step 7: (Optional) Setup SSH Key for GitHub / GitLab

যদি remote repo (GitHub/GitLab) এ কাজ করতে চান:

```bash
ssh-keygen -t ed25519 -C "youremail@example.com"
```

👉 Press Enter কয়েকবার দিন → Key তৈরি হবে।
👉 তারপর key দেখতে:

```bash
cat ~/.ssh/id_ed25519.pub
```

👉 Output copy করে GitHub / GitLab → **SSH Keys** এ add করুন।

---

## 🔹 Step 8: Test GitHub Connection (if SSH used)

```bash
ssh -T git@github.com
```

👉 Output:

```
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

---

## ✅ Summary (Cheat Sheet)

```bash
# Install Git (Ubuntu)
sudo apt update && sudo apt install git -y  

# Configure Git
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
git config --list  

# Setup SSH key
ssh-keygen -t ed25519 -C "youremail@example.com"
cat ~/.ssh/id_ed25519.pub
```

---

⚡ Bonus Tip: আপনি চাইলে আমি একটা **চিত্র সহ workflow** বানাতে পারি যেখানে দেখানো হবে → Git install → config → first commit → push GitHub।

আপনি কি চান আমি সেই ভিজ্যুয়াল গাইড বানিয়ে দিই?
