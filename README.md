### This is my first Git learning project.

Project: Fitness Dashboard built with Vite and React.
Feature: Working on UI improvements branch.
Hotfix: Updated documentation formatting.
Feature: Authentication module in progress.

Hotfix: Minor formatting cleanup.

Work in progress line for stash testing.

Edited from GitHub UI.

Local change before conflict simulation.

Remote change before conflict simulation.

Remote change for rebase demo.

Local change for rebase demo.

Profile feature - initial structure.

Add profile validation logic.

Fix typo in profile logic.

Improve profile UI layout.



# Hello


### SSH vs HTTPS

| Feature | HTTPS (Simple Method) | SSH (Professional Method) |
|-------|-------|-------|
| **Meaning** | HTTP stands for **HyperText Transfer Protocol** | SSH stands for **Secure Shell** |
| **Repository URL Format** | ```https://github.com/username/repo.git``` | ```git@github.com:username/repo.git``` |
| **Authentication Method** | • Username  <br> • Personal Access Token (not password) | • SSH Key Pair |
| **Login Requirement** | Requires login/token when pushing | No password required after setup |
| **Advantages** | ✅ Easy setup <br> ✅ Works immediately | ✅ More secure <br> ✅ Professional method <br> ✅ Used in companies <br> ✅ No repeated login |
| **Disadvantages** | ❌ Requires token/login <br> ❌ Slightly annoying for frequent pushes | ❌ Slightly more setup required |


## 🔐 In Short — How Git Connects to GitHub

Git needs a way to communicate with the **GitHub server (remote repository)** when sending or receiving code.

There are **two connection methods**:

* 🌐 **HTTPS**
* 🔑 **SSH**

---

## 🌐 HTTPS (Simple Method)

With **HTTPS**, Git communicates with GitHub using the **web protocol** (the same protocol used by browsers).

**Repository URL Example**

```bash
https://github.com/username/repository.git
```

### How it works

* Git connects to GitHub through the internet.
* You authenticate using:

  * **GitHub username**
  * **Personal Access Token (PAT)**

> GitHub no longer allows password authentication for Git operations.

**In simple words**

HTTPS = Login using **username + token**

---

## 🔑 SSH (Professional Method)

With **SSH**, Git communicates with GitHub using **secure key-based authentication**.

**Repository URL Example**

```bash
git@github.com:username/repository.git
```

### How it works

* Your computer generates an **SSH key pair**

  * **Private key** → stored on your computer
  * **Public key** → added to GitHub
* GitHub verifies your key when you connect.
* No password or token is required each time.

**In simple words**

SSH = Login using a **secure key (automatic authentication)**

---

## 📌 Important Note

HTTPS and SSH are used **only for communication with remote repositories (GitHub).**

They are used when running commands like:

```bash
git push
git pull
git fetch
git clone
```

They are **NOT used for local Git operations**, such as:

```bash
git add
git commit
git branch
git merge
git reset
```

These commands work **only on your local repository**.

---

## 📚 Learning Plan

For this learning project:

* ✅ We will use **HTTPS** because it is easier to start with.
* 🚀 After mastering Git basics, we will switch to **SSH**, which is commonly used in professional development environments.

## 🚀 Step 1 — Initialize a New Git Repository

### 1️⃣ Download or Open a Project

First, open any random project.

You can also download the sample project from here:

**Project Repository**

```
https://github.com/sohan/git-learning-beginner-to-advanced
```

After downloading, **extract the project folder** on your computer.

---

### 2️⃣ Remove Existing Git History

After extracting the project, check whether a **`.git` folder** exists inside the project directory.

The `.git` folder stores:

* commit history
* branches
* configuration
* repository metadata

If the `.git` folder already exists, **delete it**.

This removes the previous Git tracking so we can **start from scratch with a fresh Git repository**.

---

### 3️⃣ Open the Project in an IDE

Open the project folder in any IDE.

Example:

* **VS Code**
* WebStorm
* IntelliJ
* Atom

Then open the **terminal inside the project folder**.

In **VS Code** you can open the terminal using:

```
Ctrl + `
```

---

### 4️⃣ Initialize Git

Run the following command inside the project folder:

```bash
git init
```

This command creates a new **`.git` directory** and starts tracking the project with Git.

---

### 5️⃣ Check Repository Status

Now run:

```bash
git status
```

This command shows:

* current branch
* tracked files
* untracked files
* staged files
* changes waiting to be committed

---

### 📌 Example Output

After running the commands, you might see an output like this:

```bash
PS C:\Users\sohan\Desktop\git_and_github> git init
Initialized empty Git repository in C:/Users/sohan/Desktop/git_and_github/.git/

PS C:\Users\sohan\Desktop\git_and_github> git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.md
        index.html
        logo.png
        node_modules/
        package-lock.json
        package.json
        postcss.config.cjs
        public/
        src/
        tailwind.config.cjs
        vite.config.mjs

nothing added to commit but untracked files present (use "git add" to track)
```

---

### 📖 What This Output Means

* **On branch main** → Your repository is currently on the `main` branch.
* **No commits yet** → No commits have been created yet.
* **Untracked files** → Git sees files but is **not tracking them yet**.
* **nothing added to commit** → You haven't staged any files for commit.

Next step will be **adding files to Git tracking using `git add`**.


## 📦 Understanding Untracked Files and `.gitignore`

After initializing Git and running:

```bash
git status
```

Git shows the following output:

```bash
PS C:\Users\sohan\Desktop\git_and_github> git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.md
        index.html
        logo.png
        node_modules/
        package-lock.json
        package.json
        postcss.config.cjs
        public/
        src/
        tailwind.config.cjs
        vite.config.mjs

nothing added to commit but untracked files present (use "git add" to track)
```

### ❓ Why is `node_modules/` appearing?

Git lists **every file and folder that is not being tracked yet**.

The `node_modules/` folder appears because:

* It exists inside the project directory.
* Git sees it as a new folder that could be tracked.

However, **`node_modules` does not contain your actual project code**.

It contains:

* downloaded dependencies
* packages installed by `npm` or `yarn`

These files can always be **reinstalled using `package.json`**.

Because of this, **committing `node_modules` is considered bad practice**.

---

## ❌ Should We Commit `node_modules`?

No.

Reasons:

* The folder can be **extremely large**
* It contains **generated dependencies**
* It makes the repository unnecessarily heavy
* It can always be recreated using:

```bash
npm install
```

---

## 📄 Creating `.gitignore`

Since we don't want Git to track `node_modules`, we create a **`.gitignore` file**.

A `.gitignore` file tells Git:

> "Ignore these files or folders. Do not track them."

Currently the file is created but **empty**.

Example:

```bash
.gitignore
```

Right now Git shows:

```bash
Untracked files:

.gitignore
README.md
index.html
logo.png
package-lock.json
package.json
postcss.config.cjs
public/
src/
tailwind.config.cjs
vite.config.mjs
```

---

## 🧠 Learning Strategy

Before adding files to Git, we may **temporarily remove or delay adding some files**.

This helps us learn important Git concepts step by step such as:

* staging files
* tracking vs untracked files
* partial commits
* ignoring files
* commit history
* reverting changes
* branching
* merging
* remote repositories

This approach allows us to **understand Git deeply instead of just memorizing commands**.

---

## 📌 Current Repository State

* Git repository initialized
* No commits yet
* All files are **untracked**
* `.gitignore` file created but empty

Next step will be learning how Git **tracks files using `git add`** and understanding the **staging area**.






# 🚀 Git Learning — Step by Step

This guide explains the **initial Git workflow** from setting up a project to understanding **staging and file states in Git**.

---

# 1️⃣ Download or Open a Project

First, open any random project.

You can also download the sample project from:

```
https://github.com/sohan/git-learning-beginner-to-advanced
```

After downloading, **extract the project folder** on your computer.

---

# 2️⃣ Remove Existing Git History

Check whether the project contains a **`.git` folder**.

The `.git` folder stores:

* commit history
* branches
* configuration
* repository metadata

If the `.git` folder exists, **delete it**.

This allows us to **start the project from scratch with a fresh Git repository**.

---

# 3️⃣ Open the Project in an IDE

Open the project folder in any IDE such as:

* VS Code
* WebStorm
* IntelliJ

Then open the **terminal inside the project folder**.

---

# 4️⃣ Initialize a Git Repository

Run the following command inside the project folder:

```bash
git init
```

Example output:

```bash
Initialized empty Git repository in C:/Users/sohan/Desktop/git_and_github/.git/
```

This command:

* creates a `.git` folder
* turns the directory into a **Git repository**

---

# 5️⃣ Check Repository Status

Run:

```bash
git status
```

Example output:

```bash
On branch main

No commits yet

Untracked files:
        README.md
        index.html
        logo.png
        node_modules/
        package-lock.json
        package.json
        postcss.config.cjs
        public/
        src/
        tailwind.config.cjs
        vite.config.mjs

nothing added to commit but untracked files present (use "git add" to track)
```

### What This Means

* **On branch main** → current branch is `main`
* **No commits yet** → repository has no commits
* **Untracked files** → Git sees files but is **not tracking them**

---

# 6️⃣ Why `node_modules` Appears

Git lists **every file and folder** inside the project.

The folder `node_modules/` appears because:

* it exists in the project directory
* Git has not been told to ignore it

However, `node_modules`:

* contains downloaded dependencies
* does not contain your actual project code
* can be recreated using `npm install`

Because of this, **committing `node_modules` is not recommended**.

---

# 7️⃣ Create `.gitignore`

To prevent Git from tracking unnecessary files, create a **`.gitignore` file**.

Example `.gitignore`:

```
node_modules/
```

The `.gitignore` file tells Git:

> Ignore these files or folders when tracking the project.

---

# 8️⃣ Current Repository State

Running:

```bash
git status
```

Shows:

```bash
Untracked files:
        .gitignore
        README.md
        index.html
        logo.png
        package-lock.json
        package.json
        postcss.config.cjs
        public/
        src/
        tailwind.config.cjs
        vite.config.mjs
```

This means **none of the files are tracked yet**.

---

# 9️⃣ Add a File to the Staging Area

Add a file to Git tracking:

```bash
git add README.md
```

Check status again:

```bash
git status
```

Output:

```bash
Changes to be committed:
        new file: README.md
```

### What Happened

* `README.md` is now **tracked**
* It is placed in the **staging area**
* It will be included in the **next commit**

---

# 🔟 Modify the File After Staging

After staging `README.md`, if you edit the file again and run:

```bash
git status
```

Git shows:

```bash
Changes to be committed:
        new file: README.md

Changes not staged for commit:
        modified: README.md
```

This happens because Git tracks **two versions of the file**.

---

# 🧠 Git's Three Main Areas

Git internally works with three areas:

| Area              | Description               |
| ----------------- | ------------------------- |
| Working Directory | Where you edit files      |
| Staging Area      | Files prepared for commit |
| Repository        | Saved commit history      |

Current situation:

```
Working Directory
        ↓
README.md (modified again)

Staging Area
        ↓
README.md (previous version)

Repository
        ↓
No commits yet
```

So Git shows:

* **Changes to be committed** → staged version
* **Changes not staged for commit** → new modifications

---

# Updating the Staged Version

To stage the new changes:

```bash
git add README.md
```

---

# Unstaging a File

To remove a file from the staging area:

```bash
git rm --cached README.md
```

---

# Discard Changes in Working Directory

To discard new changes:

```bash
git restore README.md
```

⚠️ This deletes the latest modifications.

---

# 📌 Key Concept Learned

One file can exist in **multiple Git states simultaneously**.

```
Working Directory → modified file
Staging Area → version prepared for commit
Repository → saved history
```

Understanding this concept is **fundamental to mastering Git**.

---

# 📚 Next Concepts to Learn

Next we will learn:

* `git add .`
* committing changes (`git commit`)
* commit history (`git log`)
* `.gitignore` best practices
* Git file lifecycle
* Git diff
* undoing commits
* branching
* merging
* rebasing
* remote repositories
* GitHub workflow
