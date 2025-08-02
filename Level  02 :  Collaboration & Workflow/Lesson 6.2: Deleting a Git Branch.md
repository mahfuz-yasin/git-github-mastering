
# 🗑️ Git Branch ডিলিট করার নিয়ম

## 📌 ১. লোকাল (Local) Branch ডিলিট করা

### (ক) নিরাপদভাবে ডিলিট (শুধু যদি merge হয়ে থাকে)

```bash
git branch -d branch_name
```

👉 এই কমান্ডটি কেবলমাত্র Branch মুছবে যদি সেটি ইতিমধ্যে মূল Branch (যেমন `main`) এ merge হয়ে যায়।

**উদাহরণ:**

```bash
git branch -d feature-login
```

---

### (খ) জোর করে ডিলিট (merge না হলেও)

```bash
git branch -D branch_name
```

👉 সতর্ক থাকুন ⚠️ — এই কমান্ডটি Branch মুছে দেবে, এমনকি পরিবর্তন merge না হলেও।

**উদাহরণ:**

```bash
git branch -D feature-login
```

---

## 📌 ২. রিমোট (Remote / GitHub) Branch ডিলিট করা

```bash
git push origin --delete branch_name
```

**উদাহরণ:**

```bash
git push origin --delete feature-login
```

👉 এটি GitHub বা অন্য কোনো রিমোট রিপোজিটরি থেকে ওই Branch মুছে দেবে।

---

## 📌 ৩. ডিলিট হওয়া Branch চেক করা

* **লোকাল Branch গুলো দেখতে**

```bash
git branch
```

* **রিমোট Branch গুলো দেখতে**

```bash
git branch -r
```

---

# ✅ টিপস

* মুছে ফেলার আগে দেখে নিন আপনার পরিবর্তনগুলো দরকারি কিনা।
* বড় টিমে কাজ করলে Branch ডিলিট করার আগে টিমের সাথে কনফার্ম করুন।
