# Git Tagging Lab Solution

## **🔧 Lab Setup for Git Tagging Practice**
This guide covers **lightweight tags**, **annotated tags**, **pushing tags**, **deleting tags**, and **checking out tags**.

## **🛠 Prerequisites**
- A **Linux machine** or **local machine** with Git installed.
- A **GitHub repository** (optional, for remote operations).
- Basic understanding of Git commands.

---

## **Step 1: Install Git (If Not Installed)**
```bash
sudo apt update
sudo apt install git -y
```
Verify installation:
```bash
git --version
```

---

## **Step 2: Configure Git (If Not Configured)**
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

## **Step 3: Create a Sample Git Repository**
```bash
mkdir git-tagging-lab && cd git-tagging-lab
git init
```
Create a sample file and commit:
```bash
echo "Version 1.0" > version.txt
git add version.txt
git commit -m "Initial commit with version 1.0"
```

---

## **Step 4: Create and Manage Git Tags**
### **🔹 4.1 Create an Annotated Tag**
```bash
git tag -a v1.0 -m "Release version 1.0"
```
Verify:
```bash
git show v1.0
```

### **🔹 4.2 Create a Lightweight Tag**
```bash
git tag v1.0-light
```
Verify:
```bash
git show v1.0-light
```

---

## **Step 5: Push Tags to Remote Repository**
### **🔹 5.1 Add a Remote Repository (Optional)**
```bash
git remote add origin https://github.com/yourusername/git-tagging-lab.git
```
### **🔹 5.2 Push Tags to GitHub**
```bash
git push origin v1.0  # Push specific tag
git push origin --tags  # Push all tags
```

---

## **Step 6: Delete Tags**
### **🔹 6.1 Delete a Local Tag**
```bash
git tag -d v1.0
```
Verify:
```bash
git tag  # List remaining tags
```

### **🔹 6.2 Delete a Remote Tag**
```bash
git push origin --delete v1.0
```

---

## **Step 7: Checkout a Tag**
To switch to a tag:
```bash
git checkout v1.0
```
To create a new branch from a tag:
```bash
git checkout -b release-1.0 v1.0
```

---

## **Next Steps**
- Try **signing a tag** using GPG keys.
- Learn about **semantic versioning** (v1.0.1, v1.1.0, etc.).
- Automate tagging in **CI/CD pipelines**.

---

This guide provides a complete **Git tagging lab** solution. Upload this `solution.md` to your GitHub repository for reference! 🚀
