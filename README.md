# 🚀 Project Rules for Cursor

🎯 This will help you set up automated task tracking in your project using **Cursor's Project Rules** and a `prd.md` file. 

## 📌 Why Use This?
Without proper tracking, **AI-based code assistants** tend to forget approved changes and might unintentionally modify or remove them. ❌  
By automating updates to a `prd.md` file, you can:
✅ Prevent unnecessary code modifications  
✅ Keep track of completed and pending tasks  
✅ Speed up your development process  

---

## 🛠️ Setup Guide

### 1️⃣ Create a `prd.md` file
Inside your project, create a file named `prd.md` and structure it like this:

```md
## Done
- UI customization
- Storing projects with localStorage

## To Do
- Advanced statistics & reporting features
- Code improvements (DRY, refactoring)
```

---

### 2️⃣ Add the `prd-accept` Rule in Cursor

Go to **Cursor's Project Rules** and add the following rule:

```md
Rule: prd-accept

Trigger:
- When the user approves a piece of code and writes a command starting with "all good", this rule is triggered.

Action:
1. Open the prd.md file.
2. Find the "## Done" section in the file.
3. Search for the latest approved output (the one the user confirmed with "all good") in this section.
4. If this output is not in the "## Done" list, append it to the bottom.
5. If it already exists, do nothing.

Context:
- This rule only executes when the user starts their command with "all good".
- This rule ensures that newly developed features are updated in the @prd.md file.
```

---

### 3️⃣ How It Works? 🤔
When you complete a task and type:
```md
all good. Now let's work on feature X.
```
✅ The task **automatically** gets added to the **"Done"** list in `prd.md`.  
✅ You can move on to the next task with a **clear track of progress**.  

---

## 🎯 Benefits
⚡ **Faster development** – No more second-guessing what was completed.  
📝 **Better documentation** – Keep an up-to-date progress log effortlessly.  
💡 **Fewer errors** – Prevent unwanted code modifications.  

---

## 🚀 Try It Out!
Implement this in your Cursor environment and feel the difference! Happy coding! 🎉

### 👋 🍉
[x](https://x.com/mergencdev) | [medium](https://mergenc.medium.com) | [linkedin](https://www.linkedin.com/in/mehmet-ergenc)
