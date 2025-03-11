# Git Stash Command - Solution Guide

## **What is Git Stash?**
Git stash allows you to temporarily save uncommitted changes and restore them later. It helps when you need to switch branches or work on something else without committing unfinished work.

---

## **Common Git Stash Commands & Fixes**

### **1️⃣ Stash Uncommitted Changes**
```bash
git stash
```
This will save your modified and staged files while cleaning the working directory.

### **2️⃣ List Stashed Changes**
```bash
git stash list
```
Displays all stored stashes in a stack-like structure.

### **3️⃣ Apply the Most Recent Stash**
```bash
git stash pop
```
Restores the most recent stash and removes it from the stash list.

### **4️⃣ Apply a Stash Without Removing It**
```bash
git stash apply
```
Restores changes but keeps the stash in the list.

### **5️⃣ Stash with a Custom Message**
```bash
git stash push -m "WIP: Fixing login issue"
```
Saves the stash with a meaningful description.

### **6️⃣ Apply a Specific Stash**
```bash
git stash apply stash@{1}
```
Applies the second stash from the list.

### **7️⃣ Delete a Specific Stash**
```bash
git stash drop stash@{0}
```
Removes the most recent stash.

### **8️⃣ Clear All Stashes**
```bash
git stash clear
```
Deletes all saved stashes permanently.

---

## **Example Scenario**
1. You modify files `index.html` and `style.css`.
2. You need to switch branches but don't want to commit incomplete work.
3. Run `git stash` to save the changes.
4. Switch branches, fix the issue, and return to the original branch.
5. Restore changes with `git stash pop`.

---

## **Key Benefits**
✅ Helps in switching branches without committing incomplete work.  
✅ Acts as a temporary clipboard for code changes.  
✅ Prevents unnecessary commits in the repository.  

Use `git stash` effectively to manage your workflow! 🚀

