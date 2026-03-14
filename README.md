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
---

**🔹 HTTPS (Simple Method)**\
(HTTP stands for HyperText Transfer Protocol.)

When you push to GitHub using HTTPS:

``` bash 
https://github.com/username/repo.git 
``` 

You authenticate using:

- Username

- Personal Access Token (NOT password)

✅ Advantages

- Easy setup

- Works immediately

❌ Disadvantages

- Needs login/token

- Slightly annoying
---

**🔹 SSH (Professional Method)**\
(SSH stands for Secure Shell.)

When you use SSH:

```bash
git@github.com:username/repo.git
```

You authenticate using:

- SSH key pair

- No password every time

✅ Advantages

- Secure

- Professional

- Used in companies

- No repeated login

❌ Slightly more setup


### 🔐 In Short 
Git needs a way to talk to GitHub server.

There are 2 ways to connect:

**🌐 HTTPS**

Git talks to GitHub using web protocol.

Example:
```bash
https://github.com/username/repo.git
```
What it does:

- Connects using internet like a browser

- You authenticate using username + token

*In simple words:*

HTTPS = Login with password/token every time

**🔑 SSH**

Git talks to GitHub using secure key authentication.

Example:
```bash
git@github.com:username/repo.git
```
What it does:

- Uses a secret key stored on your computer

- GitHub verifies that key

- No password needed

*In simple words:*

SSH = Login using secret key (automatic, secure)

### Note: HTTPS and SSH are only for communication with GitHub (remote server).
✅ We will use HTTPS for this entire learning project.\
✅ After you fully master Git → Next we switch to SSH.

They are used when you:

```
git push
git pull
git fetch
git clone
```
They are NOT used for local Git operations like:
``` bash
git add 
git commit
git branch
git merge
git reset
```

## Learning Git

First, open any random project. You can also download the provided file and extract it.
**[Here is file](https://github.com/TiwariRahul16/git-learning-beginner-to-advanced)**

After extracting the project, check whether a **`.git` folder** is present inside the project directory. This folder contains the previous Git history of the project.

If you find the `.git` folder, delete it. This will remove the existing Git tracking so that we can **start the project from the beginning with a fresh Git repository**.

open project in any ide
Inside your project folder in VSCode terminal:
run this command:
git init

git status

after this command you will get output like
note i want to learn every things of git.


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
