
# 🔹 Git Branch

## ✅ Branch কী?

Git-এ **Branch** মানে হলো একই প্রজেক্টের ভেতরে আলাদা একটি ট্র্যাক/লাইনের মতো, যেখানে আপনি নতুন ফিচার, বাগ ফিক্স বা এক্সপেরিমেন্টাল কাজ করতে পারেন মূল কোড (যেমন `main` বা `master`) নষ্ট না করেই।

👉 সহজভাবে:

* `main` → আপনার প্রোডাকশন বা স্থিতিশীল কোড
* `feature-login` → নতুন লগইন ফিচারের জন্য আলাদা Branch

---

## ✅ কেন ব্যবহার করবেন?

* নতুন ফিচার ডেভেলপমেন্ট আলাদাভাবে করতে পারবেন
* টিমে একাধিক ডেভেলপার একই সময়ে আলাদা Branch-এ কাজ করতে পারবেন
* মূল কোড নষ্ট হওয়ার ভয় কম থাকবে
* প্রয়োজনে এক্সপেরিমেন্টাল কাজ করে পরে বাদ দিতে পারবেন

---

## ✅ কিভাবে ব্যবহার করবেন?

### 1️⃣ Branch তৈরি

```bash
git branch branch_name
```

### 2️⃣ Branch তৈরি ও সাথে সাথে Switch করা

```bash
git checkout -b branch_name
```

অথবা (নতুন ভার্সনে):

```bash
git switch -c branch_name
```

### 3️⃣ Branch লিস্ট দেখা

```bash
git branch
```

### 4️⃣ Branch পরিবর্তন

```bash
git switch branch_name
```

---

# 🔹 Git Merge

## ✅ Merge কী?

**Merge** মানে হলো দুটি Branch-এর কোডকে একত্রিত করা।
সাধারণত, কোনো ফিচার বা বাগ ফিক্স করার পর সেটি `main` বা `develop` Branch-এ ফিরিয়ে আনার জন্য Merge ব্যবহার করা হয়।

---

## ✅ কেন ব্যবহার করবেন?

* একাধিক Branch-এ করা পরিবর্তন একসাথে যুক্ত করতে
* নতুন ফিচার শেষ হলে তা মূল প্রজেক্টে যুক্ত করতে
* টিমের বিভিন্ন মেম্বারের কাজ একত্রিত করতে

---

## ✅ কিভাবে ব্যবহার করবেন?

### 1️⃣ প্রথমে মূল Branch-এ যান (যেখানে Merge করবেন)

```bash
git switch main
```

### 2️⃣ অন্য Branch Merge করুন

```bash
git merge branch_name
```

উদাহরণ:

```bash
git merge feature-login
```

👉 এখানে `feature-login` এর কোড `main` এ Merge হবে।

---

## 🔹 Merge-এর ফলাফল

* **Fast-forward merge**
  👉 যদি `main` এর পর থেকে কোনো নতুন কমিট না থাকে, তাহলে Git সরাসরি Branch যুক্ত করে দেয়।

* **Three-way merge**
  👉 যদি উভয় Branch-এ আলাদা কমিট থাকে, Git একটি নতুন Merge commit তৈরি করে।

* **Conflict**
  👉 যদি একই ফাইলের একই অংশে দুই Branch-এ আলাদা পরিবর্তন থাকে, তাহলে Git conflict দেখাবে।
  আপনাকে ম্যানুয়ালি ফাইল এডিট করে সমস্যা সমাধান করতে হবে।

---

# 📌 একটি ছোট Workflow উদাহরণ

```bash
# main থেকে নতুন Branch তৈরি
git switch -c feature-login

# কিছু কোড এডিট ও কমিট করা
git add .
git commit -m "Added login feature"

# main এ ফিরে আসা
git switch main

# feature-login এর কোড main এ Merge করা
git merge feature-login
```

---

# 🖼️ ভিজ্যুয়াল রিপ্রেজেন্টেশন

```
(main) ----●----●
              \
               ●----● (feature-login)
                        \
                         Merge ➝ ● (main)
```

---

👉 সংক্ষেপে:

* **`git branch`** = Branch তৈরি ও ম্যানেজ করার জন্য
* **`git merge`** = এক Branch-এর কাজ অন্য Branch-এ আনার জন্য

