# Git Reset Practice Lab

## **Prerequisites**
- A Linux server or local machine with Git installed.
- A GitHub repository (optional for remote practice).
- A sample project (or create one).

---

## **Step 1: Initialize a Git Repository**
```bash
mkdir git-reset-lab && cd git-reset-lab
git init
```

---

## **Step 2: Create and Commit Some Files**
```bash
echo "First Line" > file.txt
git add file.txt
git commit -m "Commit 1: Added file.txt"

echo "Second Line" >> file.txt
git add file.txt
git commit -m "Commit 2: Added second line"

echo "Third Line" >> file.txt
git add file.txt
git commit -m "Commit 3: Added third line"

echo "Fourth Line" >> file.txt
git add file.txt
git commit -m "Commit 4: Added fourth line"

git log --oneline  # Check commits history
```

---

## **Step 3: Practice `git reset` Commands**

### **1. `git reset --soft` (Keep changes staged)**
```bash
git reset --soft HEAD~1  # Moves HEAD back by one commit
git status  # File changes remain staged
```
💡 **Use Case:** Undo last commit but keep changes staged for a new commit.

---

### **2. `git reset --mixed` (Keep changes unstaged)**
```bash
git reset --mixed HEAD~1  # Moves HEAD back but unstages changes
git status  # Changes are present but unstaged
```
💡 **Use Case:** Undo a commit and unstage changes for modifications.

---

### **3. `git reset --hard` (Remove all changes)**
```bash
git reset --hard HEAD~1  # Moves HEAD back and removes changes
git status  # No changes left
```
💡 **Use Case:** Completely remove changes and revert to a previous commit.

---

## **Step 4: Experiment with Remote Repository**
### **Push changes and reset to check behavior with `origin/main`**
```bash
git remote add origin <your-repo-url>
git push origin main
```
Then, test resetting commits and force-pushing:
```bash
git reset --hard HEAD~1
git push origin main --force  # Force push after reset
```

---

## **Step 5: Restore After `git reset --hard`**

### **1️⃣ Check Git Reflog (Find Lost Commits)**
```bash
git reflog
```
Example output:
```
abc1234 (HEAD -> main) HEAD@{0}: reset: moving to HEAD~1
def5678 HEAD@{1}: commit: Added new feature
ghi9101 HEAD@{2}: commit: Fixed a bug
jkl3456 HEAD@{3}: commit: Initial commit
```
💡 **Look for the commit hash before the reset (e.g., `def5678`).**

---

### **2️⃣ Restore the Lost Commit**
Once you find the commit hash from `git reflog`, reset back to it:
```bash
git reset --hard <commit-hash>
```
Example:
```bash
git reset --hard def5678
```
✅ This brings back the lost commit.

---

### **3️⃣ If You Reset After Pushing to Remote**
If the hard reset removed commits that were already pushed, and you want to restore them:
```bash
git push origin main --force
```
⚠️ **Warning:** Force push can rewrite history on the remote repository.

---

### **4️⃣ If Reset Deleted Uncommitted Changes**
If your hard reset removed uncommitted work, try recovering it from your IDE’s local history (if available). Otherwise, it is permanently lost.

---

## **Summary of Recovery Steps**
| Situation | Solution |
|-----------|----------|
| Lost committed changes | Use `git reflog` and `git reset --hard <commit-hash>` |
| Lost pushed commits | Use `git push origin main --force` |
| Lost uncommitted changes | Cannot be recovered (unless using IDE backups) |

---

Try this lab setup and let me know if you need further modifications! 🚀


