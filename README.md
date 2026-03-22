<!-- ### This is my first Git learning project.

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

Improve profile UI layout. -->



# Git & GitHub Complete Practical Guide (Beginner → Advanced)

### Quick Navigation

- [Skip Introduction](#table-of-contents)
- [Go to Table of Contents](#table-of-contents)


## Introduction

Welcome to the **Git & GitHub Complete Practical Guide**.

This repository is designed as a **hands-on learning resource** that teaches Git step-by-step from **beginner to advanced level** using real commands, explanations, terminal outputs, and practical examples.

Unlike typical tutorials that only explain theory, this guide follows a **real learning journey**, where every concept is practiced directly in the terminal. You will see the exact commands executed, the outputs they produce, and the reasoning behind each step.

The goal of this repository is to help anyone — even someone with **zero Git experience** — understand how Git works internally and how it is used in real development workflows.

---

## Why This Repository Exists

Many Git tutorials explain commands but do not explain **how Git actually behaves** when you run them.

This guide focuses on:

* Understanding **how Git tracks changes**
* Learning the **Git file lifecycle**
* Practicing **branching and merging**
* Understanding **commit history**
* Learning how to **undo mistakes safely**
* Working with **remote repositories**
* Using **professional Git workflows**

By the end of this guide, you will understand not just **how to use Git**, but also **why Git behaves the way it does**.

---

## How to Use This Guide

This guide is organized in a **progressive learning structure**.

Each section builds on the previous one and introduces new concepts step by step.

Every topic includes:

* Explanations of the concept
* Real terminal commands
* Actual command outputs
* Diagrams to visualize Git behavior
* Practical examples
* Troubleshooting tips

To get the best learning experience:

1. Follow the sections in order.
2. Run the commands yourself in your terminal.
3. Observe the outputs and compare them with the examples.

---

## What You Will Learn

This repository covers the **complete Git workflow**, including:

* Version control fundamentals
* Git installation and configuration
* Repository initialization
* Git file lifecycle
* Staging and committing changes
* Viewing commit history
* Branching and switching branches
* Merging branches
* Handling Git safety mechanisms
* Undoing changes
* Stashing temporary work
* Recovering lost commits
* Working with remote repositories
* Fetch vs Pull
* Advanced Git history rewriting
* SSH authentication with GitHub
* Real-world Git workflows

---

## Who This Guide Is For

This guide is suitable for:

* Beginners learning Git for the first time
* Developers who want a **deep understanding of Git**
* Students preparing for **professional development workflows**
* Anyone who wants to understand **how Git works internally**

No prior Git knowledge is required.

---

## Repository Goal

By the time you finish this README, you will be able to:

* Use Git confidently in real projects
* Understand Git’s internal model
* Work with branches and merges
* Fix mistakes without fear
* Collaborate using Git and GitHub
* Follow professional Git workflows

This guide aims to transform Git from something that feels confusing into a **powerful tool you fully understand and control**.

---

## Badges

![Git](https://img.shields.io/badge/Git-Version%20Control-orange)
![GitHub](https://img.shields.io/badge/GitHub-Repository-black)
![Beginner Friendly](https://img.shields.io/badge/Beginner-Friendly-green)
![Learning](https://img.shields.io/badge/Learning-Practical-blue)

---

## Git Workflow Overview

Understanding Git becomes much easier when you visualize how code moves through the Git system.

```
Working Directory
       │
       │ git add
       ▼
Staging Area
       │
       │ git commit
       ▼
Local Repository
       │
       │ git push
       ▼
Remote Repository (GitHub)
```

This workflow represents the **core lifecycle of changes in Git**.

---

Continue to the next section to explore the **complete navigation of this guide**.


# Table of Contents

This guide is organized as a **step-by-step practical learning path**.
Each section builds on the previous one, helping you move from **basic Git concepts to advanced workflows**.

Use the links below to quickly navigate to any section.

---


## Navigation

1. [Introduction](#git--github-complete-practical-guide-beginner--advanced)

2. [Table of Contents](#table-of-contents)

3. [What is Version Control](#what-is-version-control)

4. [What is Git](#what-is-git)

5. [Git vs GitHub](#git-vs-github)

6. [Local vs Remote Repositories](#local-vs-remote-repositories)

7. [Environment Setup](#environment-setup)

8. [HTTPS vs SSH Authentication](#https-vs-ssh-authentication)

9. [Initializing a Repository](#initializing-a-repository)

10. [Understanding Git Status](#understanding-git-status)

11. [.gitignore](#gitignore)

12. [Git File Lifecycle](#git-file-lifecycle)

13. [Staging Files](#staging-files)

14. [Inspecting Changes](#inspecting-changes)

15. [Commits and History](#commits-and-history)

16. [Understanding HEAD](#understanding-head)

17. [Branching](#branching)

18. [Switching Branches](#switching-branches)

19. [Merging Branches](#merging-branches)

20. [Fast-Forward Merge](#fast-forward-merge)

21. [Three-Way Merge](#three-way-merge)

22. [Git Safety Mechanisms](#git-safety-mechanisms)

23. [Undoing Changes](#undoing-changes)

24. [Git Stash](#git-stash)

25. [Git Reflog](#git-reflog)

26. [Remote Repositories](#remote-repositories)

27. [Fetch vs Pull](#fetch-vs-pull)

28. [Advanced Git History](#advanced-git-history)

29. [Git Command Cheat Sheet](#git-command-cheat-sheet)

30. [Git Workflow Diagram](#git-workflow-diagram)

31. [Common Git Mistakes](#common-git-mistakes)

32. [Learning Questions & Answers](#learning-questions--answers)

33. [SSH Authentication with Git (Using SSH Instead of HTTPS)](#ssh-authentication-with-git-using-ssh-instead-of-https)

---

## How This Guide Progresses

The guide follows the same flow used by professional developers when learning Git:

```
Git Basics
   ↓
Understanding Git Internals
   ↓
Branching & Merging
   ↓
Undoing Mistakes
   ↓
Working With Remote Repositories
   ↓
Advanced Git History
   ↓
Professional Git Workflow
```

If you are **new to Git**, start from the beginning and move sequentially through each section.

If you already know some Git concepts, you can jump directly to the relevant section using the navigation links above.

---

In the next section, we begin with the **core problem Git solves — Version Control**.

---

🔝 [Back to Table of Contents](#table-of-contents)

--- 

# What is Version Control

Before learning Git, it is important to understand the **problem Git solves**.

That problem is called **Version Control**.

---

# The Problem Without Version Control

Imagine you are working on a project and you keep saving files like this:

```
project_final.js
project_final_v2.js
project_final_v3.js
project_really_final.js
project_final_last.js
```

This approach quickly becomes confusing because:

* You lose track of which file is the latest.
* You cannot easily see what changed between versions.
* If you accidentally delete something, recovery is difficult.
* Multiple developers working on the same project will overwrite each other's work.

This is exactly the problem **Version Control Systems (VCS)** solve.

---

# What is Version Control?

Version Control is a system that **tracks changes to files over time**.

It allows developers to:

* Save snapshots of their code
* See what changed between versions
* Restore previous versions
* Collaborate safely with other developers

Instead of creating multiple copies of files manually, a version control system keeps a **structured history of changes**.

---

# Example Scenario

Suppose you are building a web application.

Without version control:

```
App.js
App_backup.js
App_backup_final.js
App_final_fixed.js
```

With version control:

```
Commit 1 → Initial project
Commit 2 → Added login page
Commit 3 → Fixed authentication bug
Commit 4 → Improved UI
```

Every change becomes part of a **clear and organized history**.

---

# Benefits of Version Control

Version control systems provide several important advantages.

## 1. Track Changes

You can see exactly **what changed in the code**.

Example:

```
Added authentication feature
Fixed login validation bug
Updated UI styles
```

---

## 2. Restore Previous Versions

If something breaks, you can return to an earlier version of the project.

Example:

```
Current version → Buggy
Previous version → Stable
```

You can instantly go back to the stable version.

---

## 3. Safe Experimentation

Developers can experiment with new ideas without affecting the stable version of the project.

Example:

```
Main version → Stable application
Experiment version → New feature under development
```

---

## 4. Collaboration

Multiple developers can work on the same project without overwriting each other's changes.

Each developer can:

* Work on their own changes
* Combine work later safely

---

# Types of Version Control Systems

There are two main types of version control systems.

## 1. Centralized Version Control

In centralized systems:

```
Developers
     ↓
Central Server
```

All developers depend on a **single central server**.

Example tools:

* SVN (Subversion)
* CVS

Problem:

If the server fails, the project history may be lost.

---

## 2. Distributed Version Control

Distributed systems solve this problem.

Each developer has a **complete copy of the repository**, including the full history.

```
Developer A → Full repository
Developer B → Full repository
Developer C → Full repository
```

This means:

* Work can continue even without internet
* History is safe on multiple machines
* Collaboration becomes easier

---

# Git is a Distributed Version Control System

Git is a **Distributed Version Control System (DVCS)**.

This means:

* Every developer has a complete repository
* Full history exists locally
* Work can be done offline
* Changes can later be shared with others

Git became the **most widely used version control system** in software development.

---

# Why Version Control is Essential for Developers

Modern software development is impossible without version control.

Version control enables:

* Professional team collaboration
* Safe code experimentation
* Complete project history
* Reliable recovery from mistakes

Git provides all of these capabilities and has become the **industry standard tool for version control**.

---

In the next section, we will explore **Git itself — what it is and how it works internally**.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# What is Git

Now that we understand **Version Control**, we can understand **Git**.

Git is the **tool that implements version control** for modern software development.

---

# Definition of Git

**Git is a distributed version control system used to track changes in files and coordinate work among multiple developers.**

It allows developers to:

* Track changes in source code
* Maintain complete project history
* Collaborate with other developers
* Safely experiment with new features
* Restore previous versions of the project

Git was created in **2005 by Linus Torvalds**, the creator of the Linux kernel.

---

# Why Git Was Created

Before Git existed, the Linux kernel used another version control system called **BitKeeper**.
When that tool became unavailable, Linus Torvalds designed Git with specific goals:

* **Speed**
* **Data integrity**
* **Distributed development**
* **Efficient branching**

Today Git is the **most widely used version control system in the world**.

---

# Key Characteristics of Git

Git is different from older version control systems in several important ways.

---

## 1. Distributed System

Every developer has a **complete copy of the repository**.

This includes:

* Full project files
* Complete commit history
* All branches

Example:

```
Developer A → Full repository
Developer B → Full repository
Developer C → Full repository
```

This means developers can work **offline** and still have access to the full history.

---

## 2. Snapshot-Based Model

Git stores **snapshots of the project**, not just differences between files.

When you create a commit, Git saves a **snapshot of the project at that moment**.

Example commit history:

```
Commit 1 → Initial project
Commit 2 → Added UI
Commit 3 → Fixed login bug
Commit 4 → Improved performance
```

Each commit represents the **state of the entire project at that time**.

---

## 3. Fast Operations

Most Git operations happen **locally**.

Examples:

* Creating commits
* Viewing history
* Creating branches
* Switching branches

Because Git works locally, these operations are extremely fast.

---

## 4. Strong Data Integrity

Every commit in Git is identified using a **cryptographic hash**.

Example commit hash:

```
05e9725785175d8466a2eba33ba50dc3a25ef5b6
```

This hash ensures:

* Commit history cannot be altered unnoticed
* Data corruption can be detected
* Every commit has a unique identity

---

# Git Workflow Overview

Git manages code using a **three-stage workflow**.

```
Working Directory
      ↓
git add
      ↓
Staging Area
      ↓
git commit
      ↓
Repository
```

### Working Directory

Where you edit your project files.

### Staging Area

Where changes are prepared before committing.

### Repository

Where Git permanently stores project history.

We will explore this workflow in detail later in this guide.

---

# Why Developers Use Git

Git has become the industry standard because it provides:

* Powerful branching system
* Reliable history tracking
* Fast local operations
* Safe collaboration
* Strong data integrity

It allows developers to **experiment safely without breaking the main project**.

---

# Git Is a Tool — Not a Hosting Platform

It is important to understand that **Git itself is just a tool** installed on your computer.

Git manages your project history locally.

To share repositories online, developers use platforms such as:

* GitHub
* GitLab
* Bitbucket

These platforms provide **hosting for Git repositories**.

---

In the next section, we will clearly understand the difference between **Git and GitHub**, which is a common point of confusion for beginners.

---

🔝 [Back to Table of Contents](#table-of-contents)

---


# Git vs GitHub

One of the most common beginner confusions is the difference between **Git** and **GitHub**.

Many people use these names interchangeably, but they are **not the same thing**.

Understanding the difference is important before learning how Git workflows operate.

---

# What is Git?

**Git is a version control system.**

It is a **software tool installed on your computer** that tracks changes in files and manages project history.

Git works **locally** on your machine.

Example Git operations:

```bash
git init
git add .
git commit -m "Initial commit"
git branch
git merge
```

All of these commands run **on your computer**, even without an internet connection.

Git manages:

* File history
* Commits
* Branches
* Merges
* Local repositories

Git itself **does not require the internet**.

---

# What is GitHub?

**GitHub is a cloud platform that hosts Git repositories.**

It provides an online location where developers can:

* Store Git repositories
* Share code with others
* Collaborate on projects
* Review code
* manage issues and pull requests

Example GitHub repository URL:

```bash
https://github.com/username/project-name
```

GitHub allows developers around the world to **collaborate on the same project**.

---

# Simple Analogy

A simple way to understand the difference:

```text
Git     = The version control tool
GitHub  = The website that hosts Git repositories
```

Another analogy:

```text
Git     = Microsoft Word
GitHub  = Google Drive
```

You write documents in Word (Git), but you store and share them on Google Drive (GitHub).

---

# How Git and GitHub Work Together

The typical workflow looks like this:

```text
Local Computer
      ↓
   Git Repository
      ↓
git push
      ↓
GitHub Repository
```

A developer:

1. Works locally using Git.
2. Saves history using commits.
3. Pushes the repository to GitHub.
4. Other developers pull the changes.

---

# Example Workflow

Developer creates a project locally:

```bash
git init
git add .
git commit -m "Initial project setup"
```

Then connects it to GitHub:

```bash
git remote add origin https://github.com/username/project.git
git push -u origin main
```

Now the project exists both:

* **locally on the developer's machine**
* **remotely on GitHub**

---

# Why GitHub Is Useful

GitHub provides many features beyond hosting repositories.

### Collaboration

Developers can contribute to the same project.

### Pull Requests

Code changes can be reviewed before merging.

### Issue Tracking

Teams can track bugs and tasks.

### Project Management

Projects can organize development tasks.

### Backup

Repositories stored on GitHub are safely backed up.

---

# Other Git Hosting Platforms

GitHub is not the only hosting service for Git repositories.

Other platforms include:

* GitLab
* Bitbucket
* Azure DevOps

However, **GitHub is the most widely used platform in the industry**.

---

# Key Differences Summary

| Feature           | Git                    | GitHub                        |
| ----------------- | ---------------------- | ----------------------------- |
| Type              | Version Control System | Hosting Platform              |
| Runs On           | Local Machine          | Cloud Platform                |
| Requires Internet | No                     | Yes                           |
| Purpose           | Track code history     | Share and collaborate on code |

---

# Important Concept

You can use **Git without GitHub**.

But you **cannot use GitHub without Git**, because GitHub repositories are based on Git.

---

In the next section, we will explore the difference between **Local Repositories and Remote Repositories**, which is essential for understanding collaboration workflows.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# Local vs Remote Repositories

To understand how Git works in real projects, you must understand the difference between **local repositories** and **remote repositories**.

Git allows developers to work **locally on their machines** while also sharing their work through **remote repositories hosted online**.

---

# What is a Local Repository

A **local repository** is the Git repository stored on your own computer.

It contains:

* Project files
* Complete commit history
* Branches
* Tags
* Git configuration
* The `.git` directory

When you run the following command:

```bash
git init
```

Git creates a hidden folder called:

```text
.git
```

This folder contains the **entire database of your Git repository**, including all commits and history.

Example structure:

```text
project-folder/
│
├── src/
├── package.json
├── README.md
└── .git/
```

Everything inside `.git` is how Git **tracks the history of the project**.

---

# What Happens in a Local Repository

All of the following operations happen **locally**:

* Creating commits
* Viewing commit history
* Creating branches
* Switching branches
* Merging branches
* Undoing changes

Example commands:

```bash
git add .
git commit -m "Add new feature"
git branch feature-ui
git switch feature-ui
git merge feature-ui
```

None of these commands require an internet connection.

---

# What is a Remote Repository

A **remote repository** is a copy of your repository hosted on a server.

Examples of remote hosting platforms:

* GitHub
* GitLab
* Bitbucket

Example remote repository URL:

```text
https://github.com/username/project-name
```

Remote repositories allow:

* Collaboration
* Code sharing
* Backup of project history
* Team development workflows

---

# Connecting Local and Remote Repositories

A local repository can be connected to a remote repository.

Example command:

```bash
git remote add origin https://github.com/username/project.git
```

Here:

* `origin` is the default name of the remote repository
* the URL points to the repository hosted online

You can verify the connection with:

```bash
git remote -v
```

Example output:

```text
origin  https://github.com/username/project.git (fetch)
origin  https://github.com/username/project.git (push)
```

---

# Sending Code to Remote Repository

Once a remote repository is connected, you can upload your commits using:

```bash
git push origin main
```

This command sends the commits from your **local repository** to the **remote repository**.

---

# Getting Code from Remote Repository

Developers can download updates from the remote repository using:

```bash
git pull origin main
```

or

```bash
git fetch origin
```

This allows developers to stay synchronized with the latest project changes.

---

# Visualizing Local and Remote Repositories

The relationship looks like this:

```text
Your Computer
(Local Repository)
       │
       │ git push
       ▼
Remote Server (GitHub)
(Remote Repository)
       ▲
       │ git pull
       │
Other Developers
```

Each developer has their own **local repository**, but they synchronize through the **remote repository**.

---

# Real World Example

Imagine a team of three developers working on a project.

```text
Developer A → Local Repository
Developer B → Local Repository
Developer C → Local Repository
```

All developers push their work to:

```text
GitHub Remote Repository
```

And everyone pulls updates to stay synchronized.

---

# Key Concept to Remember

```text
Local Repository  → Where you work
Remote Repository → Where teams collaborate
```

Git allows developers to **work independently locally**, while still sharing work through remote repositories.

---

In the next section, we will set up **Git Environment Configuration**, which is required before creating commits.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# Environment Setup

Before using Git for any project, we need to verify that Git is installed and configure some basic settings. These settings tell Git **who is making the commits**, which is important for tracking project history.

Every commit in Git stores information such as:

* Author name
* Author email
* Commit message
* Date and time

Without configuring these settings, Git cannot properly identify the developer responsible for each commit.

---

# Check Git Installation

First, verify that Git is installed on your system.

Run the following command in your terminal:

```bash
git --version
```

Example output:

```text
git version 2.45.1.windows.1
```

This confirms that Git is installed and available in your terminal.

If Git is not installed, you need to download and install it from:

```text
https://git-scm.com
```

---

# Configure Git Username

Git needs to know the name of the developer making commits.

Set your username using:

```bash
git config --global user.name "Your Name"
```

Example:

```bash
git config --global user.name "Rahul Tiwari"
```

This name will appear in every commit you create.

Example commit information:

```text
Author: Rahul Tiwari
```

---

# Configure Git Email

Git also stores the developer's email address.

Run:

```bash
git config --global user.email "your_email@example.com"
```

Example:

```bash
git config --global user.email "Rahul13Tiwari@example.com"
```

Example commit metadata:

```text
Author: Rahul Tiwari <Rahul13Tiwari@example.com>
```

---

# Why These Configurations Are Important

Every Git commit stores author metadata like this:

```text
commit 05e9725785175d8466a2eba33ba50dc3a25ef5b6
Author: Rahul Tiwari <Rahul13Tiwari@example.com>
Date:   Wed Feb 25 22:56:34 2026 +0530

    Updated Readme.md
```

This helps:

* Track who made each change
* Maintain clear project history
* Support team collaboration

---

# Understanding the `--global` Flag

The `--global` flag means the configuration applies to **all Git repositories on your computer**.

Example:

```bash
git config --global user.name "Your Name"
```

This means you only need to set it **once**, and every Git repository you create will use the same configuration.

---

# Checking Your Git Configuration

You can check your current Git configuration using:

```bash
git config --list
```

Example output:

```text
user.name=Rahul Tiwari
user.email=Rahul13Tiwari@example.com
core.editor=code
```

This command shows all Git settings currently applied to your system.

---

# Global vs Local Configuration

Git supports multiple configuration levels:

| Configuration Level | Scope                                 |
| ------------------- | ------------------------------------- |
| System              | Applies to all users on the machine   |
| Global              | Applies to the current user           |
| Local               | Applies only to a specific repository |

Example of local configuration:

```bash
git config user.name "Project Specific Name"
```

This would override the global setting for that repository only.

---

# Environment Setup Summary

Before starting any Git project, you should ensure:

1. Git is installed.
2. Your username is configured.
3. Your email address is configured.

Commands used:

```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
git config --list
```

Once these settings are configured, Git is ready to start tracking your projects.

---

In the next section, we will understand **HTTPS vs SSH authentication**, which is used when connecting Git to remote repositories like GitHub.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# HTTPS vs SSH Authentication

When working with **remote repositories** (like GitHub), Git needs a way to **authenticate your identity** before allowing you to push or pull code.

There are two primary methods used for authentication:

* **HTTPS**
* **SSH**

Both methods allow Git to communicate with remote servers, but they differ in how authentication works.

---

# Why Authentication is Required

When you perform operations such as:

```bash
git push
git pull
git fetch
git clone
```

Git must confirm that you **have permission to access the repository**.

Authentication ensures that:

* Only authorized users can push changes
* Repository security is maintained
* Developers are correctly identified

---

# HTTPS Authentication

HTTPS is the **simplest and most common authentication method for beginners**.

Repositories accessed through HTTPS use a URL like this:

```text
https://github.com/username/repository.git
```

Example clone command:

```bash
git clone https://github.com/username/project.git
```

When pushing code using HTTPS, GitHub may ask for:

* Username
* Personal Access Token (PAT)

Example push command:

```bash
git push origin main
```

---

# Personal Access Token (PAT)

GitHub no longer allows direct password authentication.

Instead, it uses **Personal Access Tokens**.

A Personal Access Token acts like a **secure password for Git operations**.

Example authentication flow:

```text
Git Push
   ↓
GitHub asks for credentials
   ↓
Username + Personal Access Token
   ↓
Authentication successful
```

---

# Advantages of HTTPS

* Easy to set up
* Works immediately
* Good for beginners
* No additional configuration required

---

# Disadvantages of HTTPS

* Requires authentication when pushing
* May require entering credentials multiple times
* Less convenient for frequent Git operations

---

# SSH Authentication

SSH is a more **secure and professional authentication method**.

Instead of entering credentials each time, SSH uses a **cryptographic key pair**.

SSH repository URLs look like this:

```text
git@github.com:username/repository.git
```

Example clone command:

```bash
git clone git@github.com:username/project.git
```

---

# How SSH Authentication Works

SSH uses two keys:

* **Private Key** → Stored on your computer
* **Public Key** → Stored on GitHub

Authentication flow:

```text
Your Computer
   │
   │ Private Key
   ▼
GitHub
   │
   │ Matches Public Key
   ▼
Authentication successful
```

When you push or pull code, GitHub verifies the key pair instead of asking for a password.

---

# Generating an SSH Key

SSH keys can be created using:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

This generates:

```text
~/.ssh/id_ed25519
~/.ssh/id_ed25519.pub
```

* `id_ed25519` → Private key
* `id_ed25519.pub` → Public key

The public key must be added to your **GitHub account**.

---

# Testing SSH Connection

You can verify the SSH setup with:

```bash
ssh -T git@github.com
```

Example output:

```text
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

---

# HTTPS vs SSH Comparison

| Feature          | HTTPS                      | SSH                     |
| ---------------- | -------------------------- | ----------------------- |
| Authentication   | Username + Token           | SSH Key Pair            |
| Setup Difficulty | Easy                       | Moderate                |
| Security         | Good                       | Very Secure             |
| Login Frequency  | May require repeated login | No repeated login       |
| Used By          | Beginners                  | Professional developers |

---

# Real World Usage

In professional development environments:

* **SSH is commonly used**
* Automated systems prefer SSH
* CI/CD pipelines often use SSH authentication

However, many developers begin with HTTPS because it is easier to configure.

---

# Key Takeaway

Both methods achieve the same goal:

```text
Allow Git to communicate securely with remote repositories.
```

The difference lies in **how authentication happens**.

---

In the next section, we will begin working with Git repositories by learning how to **initialize a repository using `git init` and inspect its status**.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# Initializing a Repository

Before Git can track a project, the project must first become a **Git repository**.

A Git repository is simply a project directory that Git is managing and tracking.

To convert a normal project folder into a Git repository, we use the command:

```bash
git init
```

This command creates the internal structure that Git uses to track the entire project history.

---

# What `git init` Does

When you run:

```bash
git init
```

Git creates a hidden directory called:

```text
.git
```

This directory contains the **entire Git database** for the project.

It stores:

* Commit history
* Branch references
* Git configuration
* Object database
* Metadata required for version control

Example project structure after initialization:

```text
project-folder/
│
├── src/
├── index.html
├── package.json
├── README.md
└── .git/
```

Everything inside `.git` is how Git manages the project internally.

---

# Running `git init`

Example command executed inside a project folder:

```bash
git init
```

Example terminal output:

```text
Initialized empty Git repository in C:/Users/Rahul/Desktop/git_and_github/.git/
```

This message confirms that Git has successfully initialized the repository.

At this point:

* Git is active in the project directory
* Git is ready to start tracking files
* No files are being tracked yet

---

# Understanding the Initial State

After running `git init`, Git knows about the project folder, but it has **not started tracking any files yet**.

To see the current repository state, run:

```bash
git status
```

Example output:

```text
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.md
        index.html
        package.json
        src/

nothing added to commit but untracked files present (use "git add" to track)
```

---

# Understanding the Output

Let's break down what this output means.

### Current Branch

```text
On branch main
```

Git automatically creates a default branch called **main**.

This branch will hold the primary history of the project.

---

### No Commits Yet

```text
No commits yet
```

This means the repository has been created, but **no snapshots of the project have been saved yet**.

---

### Untracked Files

```text
Untracked files:
```

Git sees these files in the project folder, but they are **not yet being tracked by Git**.

Examples:

```text
README.md
index.html
package.json
src/
```

These files must be added to Git's tracking system before they can be committed.

---

# Repository Initialization Summary

The first steps of any Git project usually follow this pattern:

```bash
git init
git status
```

This process:

1. Creates a Git repository.
2. Allows Git to start tracking the project.
3. Shows the current repository state.

---

# Important Concept

Initializing a repository **does not automatically track files**.

Files must first be added to the **staging area** before they become part of Git history.

That process uses the command:

```bash
git add
```

We will explore this in detail in upcoming sections.

---

# Workflow So Far

```text
Project Folder
      ↓
git init
      ↓
Git Repository Created (.git)
      ↓
git status
      ↓
Git Shows Untracked Files
```

This is the starting point of every Git project.

---

In the next section, we will explore **`git status` in detail** and understand how Git reports the state of the repository.

---

🔝 [Back to Table of Contents](#table-of-contents)

---


# Understanding Git Status

One of the most frequently used commands in Git is:

```bash
git status
```

This command shows the **current state of your repository**.

It tells you:

* Which files are **tracked**
* Which files are **untracked**
* Which files are **modified**
* Which files are **staged for commit**

Developers run `git status` constantly while working with Git to understand **what Git sees in the project**.

---

# Running `git status`

Example command:

```bash
git status
```

Example output:

```text
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        README.md
        index.html
        package.json
        src/

nothing added to commit but untracked files present (use "git add" to track)
```

---

# Breaking Down the Output

Let's understand each part of the output.

---

## Current Branch

```text
On branch main
```

This tells you **which branch you are currently working on**.

In most repositories, the default branch is called:

```text
main
```

All commits will initially be added to this branch unless you switch to another branch.

---

## No Commits Yet

```text
No commits yet
```

This means the repository has been initialized, but **no commits have been created yet**.

Git is aware of the repository but does not yet have any saved snapshots.

---

## Untracked Files

```text
Untracked files:
```

These are files that exist in the project folder but are **not yet tracked by Git**.

Example:

```text
README.md
index.html
package.json
src/
```

Git sees these files but has not started monitoring them.

To begin tracking them, you must add them using:

```bash
git add <file>
```

or

```bash
git add .
```

---

## Nothing Added to Commit

```text
nothing added to commit but untracked files present
```

This message means:

* Git found files in the directory
* But none of them are staged for commit

So there is **nothing ready to be committed yet**.

---

# Another Example After Staging a File

After running:

```bash
git add README.md
```

Running `git status` again might show:

```text
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   README.md

Untracked files:
        index.html
        package.json
        src/
```

Now Git shows a new section called:

```text
Changes to be committed
```

This means the file is **in the staging area** and ready to be committed.

---

# Git Status Categories

`git status` generally reports files in three categories.

| Category  | Meaning                             |
| --------- | ----------------------------------- |
| Untracked | Files Git has not started tracking  |
| Modified  | Files changed after the last commit |
| Staged    | Files prepared for the next commit  |

---

# Visualizing Git Status

Git internally tracks files using three areas:

```text
Working Directory
      ↓
git add
      ↓
Staging Area
      ↓
git commit
      ↓
Repository
```

`git status` helps you understand **where files currently exist in this workflow**.

---

# Why Developers Use `git status` Frequently

Developers run `git status` often because it helps answer important questions:

* What files changed?
* What files are staged?
* What files are not tracked?
* What will be included in the next commit?

This command provides a **quick overview of the repository state**.

---

# Key Takeaway

`git status` is the **primary command used to inspect the state of a Git repository**.

It helps developers understand:

* what Git is tracking
* what changes are pending
* what will be committed next

---

In the next section, we will learn about **`.gitignore`**, which allows Git to ignore certain files and folders that should not be tracked.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# `.gitignore`

In most projects, there are files and folders that **should not be tracked by Git**.

These files might include:

* Dependencies
* Build artifacts
* Temporary files
* Environment configuration files
* System-generated files

To prevent Git from tracking these files, we use a special file called:

```text
.gitignore
```

---

# Why Some Files Should Not Be Committed

Not every file in a project should be stored in the repository.

Some files are **generated automatically** or **contain sensitive information**.

Examples:

* dependency folders
* compiled files
* environment variables
* local configuration files

Tracking these files can cause problems such as:

* unnecessarily large repositories
* security risks
* merge conflicts
* inconsistent development environments

---

# Example: `node_modules`

In JavaScript projects, dependencies are installed in a folder called:

```text
node_modules/
```

This folder may contain **thousands of files** and can become extremely large.

However, these dependencies are already listed in:

```text
package.json
package-lock.json
```

Anyone cloning the project can simply run:

```bash
npm install
```

This will automatically recreate the `node_modules` folder.

Therefore, it is unnecessary and inefficient to commit it.

---

# Creating a `.gitignore` File

Inside the root of your repository, create a file called:

```text
.gitignore
```

Example structure:

```text
project-folder/
│
├── src/
├── package.json
├── README.md
└── .gitignore
```

---

# Example `.gitignore` File

A typical `.gitignore` file for a Node.js project might look like this:

```text
node_modules/
dist/
.env
.env.local
logs/
*.log
```

Explanation:

| Entry           | Meaning                      |
| --------------- | ---------------------------- |
| `node_modules/` | Ignore dependency folder     |
| `dist/`         | Ignore compiled build files  |
| `.env`          | Ignore environment variables |
| `*.log`         | Ignore log files             |

---

# How `.gitignore` Works

Git reads `.gitignore` and **ignores matching files that are not yet tracked**.

Example:

If `.gitignore` contains:

```text
node_modules/
```

Then running:

```bash
git status
```

will **not show the `node_modules` folder**.

Example output:

```text
On branch main

Untracked files:
        README.md
        index.html
        package.json
        src/
```

Notice that `node_modules/` is not listed.

---

# Important Rule

`.gitignore` only works for **files that are not already tracked**.

If a file has already been committed, adding it to `.gitignore` will **not remove it from Git tracking**.

Example situation:

```text
Step 1 → node_modules committed
Step 2 → node_modules added to .gitignore
```

Git will still track it.

To stop tracking it, you must remove it from the repository:

```bash
git rm -r --cached node_modules
```

Then commit the change.

---

# Example Workflow

Typical workflow with `.gitignore`:

```bash
git init
touch .gitignore
git status
git add .
git commit -m "Initial commit"
```

Git will ignore any files listed inside `.gitignore`.

---

# Why `.gitignore` is Important

A properly configured `.gitignore` file helps:

* keep repositories clean
* reduce repository size
* avoid committing unnecessary files
* protect sensitive data

Almost every professional repository includes a `.gitignore` file.

---

# Visual Example

```text
Project Folder
│
├── src/
├── package.json
├── README.md
├── node_modules/   ← ignored
└── .gitignore
```

Git will track:

```text
src/
package.json
README.md
```

Git will ignore:

```text
node_modules/
```

---

# Key Takeaway

`.gitignore` allows developers to **control which files Git should ignore**.

This ensures that only the **important project files** are stored in the repository.

---

In the next section, we will explore the **Git File Lifecycle**, which explains how files move between the **working directory, staging area, and repository**.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# Git File Lifecycle

To understand how Git tracks changes, you must understand the **Git File Lifecycle**.

Every file in a Git repository moves through a series of states as you modify and commit it.

These states define **how Git tracks the file and where it exists in the Git workflow**.

---

# The Three Main Areas in Git

Git manages files using three main areas:

```text
Working Directory
      ↓
git add
      ↓
Staging Area
      ↓
git commit
      ↓
Repository
```

Each area has a specific role in the version control process.

---

# 1. Working Directory

The **Working Directory** is the folder on your computer where your project files exist.

This is where you:

* create files
* edit files
* delete files

Example:

```text
project/
│
├── README.md
├── index.html
├── package.json
└── src/
```

At this stage, Git may or may not be tracking these files.

If Git has never seen a file before, it is called an **untracked file**.

Example:

```text
Untracked files:
    README.md
    index.html
```

---

# 2. Staging Area

The **Staging Area** (also called the **Index**) is where you prepare changes before committing them.

When you run:

```bash
git add README.md
```

Git moves the file from the **working directory** into the **staging area**.

Example:

```text
Changes to be committed:
    new file: README.md
```

This means the file is **ready to be included in the next commit**.

The staging area allows developers to **control exactly which changes will be committed**.

---

# 3. Repository

The **Repository** is where Git permanently stores project history.

When you run:

```bash
git commit -m "Add README"
```

Git creates a **commit** containing a snapshot of the staged files.

Example commit history:

```text
Commit 1 → Initial project
Commit 2 → Added README
Commit 3 → Updated UI
```

Once a file is committed, Git tracks its future modifications.

---

# File State Diagram

The lifecycle of a file in Git looks like this:

```text
Untracked
   ↓ git add
Staged
   ↓ git commit
Committed
   ↓ modify file
Modified
   ↓ git add
Staged again
```

This cycle continues throughout the life of the project.

---

# File States in Git

A file in Git can exist in several states:

| State     | Meaning                                |
| --------- | -------------------------------------- |
| Untracked | File exists but Git is not tracking it |
| Tracked   | Git is monitoring the file             |
| Modified  | File has changed since the last commit |
| Staged    | File is ready for the next commit      |
| Committed | File has been saved in Git history     |

---

# Example Workflow

Consider the following sequence:

Create a new file:

```text
README.md
```

Run:

```bash
git status
```

Output:

```text
Untracked files:
    README.md
```

Stage the file:

```bash
git add README.md
```

Check status again:

```text
Changes to be committed:
    new file: README.md
```

Commit the file:

```bash
git commit -m "Add README"
```

Now the file becomes part of the **Git repository history**.

---

# Why the Staging Area Exists

Many beginners wonder why Git has a staging area instead of committing changes directly.

The staging area allows developers to:

* choose specific files to commit
* group related changes
* review changes before committing
* create cleaner commit history

Example:

You modify three files:

```text
README.md
App.js
styles.css
```

You might only want to commit:

```text
README.md
```

Using staging makes this possible.

---

# Visual Workflow

```text
Edit File
    ↓
Working Directory
    ↓ git add
Staging Area
    ↓ git commit
Git Repository
```

This process repeats every time changes are made.

---

# Key Concept

Git does **not automatically track file changes**.

Developers must explicitly move files through the workflow:

```text
Working Directory → Staging Area → Repository
```

This design gives developers **precise control over project history**.

---

In the next section, we will learn how to **stage files using `git add` and manage the staging area effectively**.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# Staging Files

The **staging area** is one of the most important concepts in Git.

Before changes can become part of the repository history, they must first be placed in the **staging area**.

This process is called **staging**.

The command used for staging files is:

```bash
git add
```

---

# Why Staging Exists

Many beginners wonder why Git has a staging area instead of committing changes directly.

The staging area allows developers to:

* select specific files to commit
* group related changes
* review changes before committing
* avoid committing unfinished work

Without a staging area, every change would immediately become part of the commit history.

---

# Basic Staging Command

To stage a specific file, use:

```bash
git add filename
```

Example:

```bash
git add README.md
```

This command moves the file from the **working directory** to the **staging area**.

---

# Example Workflow

Suppose your project contains:

```
README.md
index.html
package.json
```

Running:

```bash
git status
```

Example output:

```
On branch main

Untracked files:
    README.md
    index.html
    package.json
```

Now stage one file:

```bash
git add README.md
```

Check the status again:

```bash
git status
```

Example output:

```
Changes to be committed:
    new file: README.md

Untracked files:
    index.html
    package.json
```

This means **README.md is staged and ready for commit**.

---

# Staging Multiple Files

You can stage multiple files at once:

```bash
git add file1 file2 file3
```

Example:

```bash
git add index.html package.json
```

---

# Staging an Entire Directory

To stage an entire directory:

```bash
git add src/
```

Example:

```
src/
├── App.js
├── main.js
└── styles.css
```

All files inside `src` will be staged.

---

# Staging All Files

To stage all new and modified files in the project:

```bash
git add .
```

Example workflow:

```bash
git add .
git status
```

Example output:

```
Changes to be committed:
    new file: README.md
    new file: index.html
    new file: package.json
```

---

# Updating the Staging Area

If a file is staged and then modified again, the staging area **does not update automatically**.

Example:

```
Step 1 → git add README.md
Step 2 → edit README.md again
```

Now run:

```bash
git status
```

Example output:

```
Changes to be committed:
    new file: README.md

Changes not staged for commit:
    modified: README.md
```

This means:

* The first version is staged
* The new modification is not staged yet

To update staging:

```bash
git add README.md
```

---

# Removing a File from the Staging Area

Sometimes a file is staged by mistake.

To remove it from staging without deleting it:

```bash
git restore --staged filename
```

Example:

```bash
git restore --staged README.md
```

After running this command:

* The file remains in the working directory
* It is no longer staged for commit

---

# Visualizing the Staging Process

```
Working Directory
       ↓
    git add
       ↓
Staging Area
       ↓
   git commit
       ↓
Git Repository
```

The staging area acts like a **preparation area for commits**.

---

# Real Example

Commands:

```bash
git add README.md
git status
```

Output:

```
Changes to be committed:
    new file: README.md
```

This means the file will be included in the **next commit**.

---

# Key Takeaway

The `git add` command does **not commit changes**.

Instead, it **prepares changes for the next commit** by moving them into the staging area.

Understanding staging is essential for using Git effectively.

---

In the next section, we will learn how to **inspect file changes using `git diff` before committing them**.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# Inspecting Changes

Before committing changes to a repository, developers often want to **review exactly what has changed**.

Git provides tools to inspect these changes.

The most commonly used command for this is:

```bash
git diff
```

This command shows the **line-by-line differences between file versions**.

---

# Why Inspect Changes?

Reviewing changes before committing helps developers:

* verify that the correct changes were made
* avoid committing unintended modifications
* understand how a file has changed
* maintain clean commit history

Inspecting changes is an important step in a professional Git workflow.

---

# `git diff`

The command:

```bash
git diff
```

shows the difference between:

```text
Working Directory
vs
Staging Area
```

This means it displays **changes that are not yet staged**.

---

# Example

Suppose you modify `README.md`.

Run:

```bash
git diff
```

Example output:

```diff
diff --git a/README.md b/README.md
index 954d373..7aad768 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,3 @@
-### This is my first Git learning project.
+### This is my first Git learning project.
+
+Project: Fitness Dashboard built with Vite and React.
```

---

# Understanding Diff Output

A Git diff output contains several important parts.

### File Comparison

```diff
diff --git a/README.md b/README.md
```

This shows which file is being compared.

---

### File Versions

```diff
--- a/README.md
+++ b/README.md
```

* `a/` represents the **previous version**
* `b/` represents the **new version**

---

### Line Changes

```diff
-### This is my first Git learning project.
+### This is my first Git learning project.
+
+Project: Fitness Dashboard built with Vite and React.
```

Symbols indicate the type of change:

| Symbol    | Meaning           |
| --------- | ----------------- |
| `-`       | Line removed      |
| `+`       | Line added        |
| no symbol | Unchanged context |

---

# `git diff --staged`

Once a file is staged, `git diff` will no longer show its changes.

To view staged changes, use:

```bash
git diff --staged
```

This command compares:

```text
Staging Area
vs
Last Commit
```

Example:

```bash
git add README.md
git diff --staged
```

Example output:

```diff
diff --git a/README.md b/README.md
new file mode 100644
index 0000000..c87cab0
--- /dev/null
+++ b/README.md
@@ -0,0 +1,3 @@
+### This is my first Git learning project.
+
+Project: Fitness Dashboard built with Vite and React.
```

This shows what will be included in the **next commit**.

---

# Using Diff Before Committing

A professional workflow often looks like this:

```bash
git status
git diff
git add README.md
git diff --staged
git commit -m "Update README"
```

This ensures that developers understand exactly **what is being committed**.

---

# Visualizing Diff Comparison

Git compares files between different areas:

```text
Working Directory
      ↓ git diff
Staging Area
      ↓ git diff --staged
Last Commit
```

This layered comparison allows developers to inspect changes at multiple stages.

---

# Why Diff Is Important

`git diff` helps developers:

* detect accidental changes
* verify code modifications
* review changes before committing
* maintain clean commit history

It is one of the most useful debugging and inspection tools in Git.

---

# Key Takeaway

Git provides powerful tools to inspect changes before committing.

```bash
git diff
git diff --staged
```

These commands allow developers to understand exactly **what modifications exist in their project**.

---

In the next section, we will learn how to **create commits and record changes permanently in Git history**.

---

🔝 [Back to Table of Contents](#table-of-contents)

---

# Commits and History

Once files are staged, the next step is to **save them permanently in the Git repository**.

This is done using a **commit**.

A commit represents a **snapshot of the project at a specific moment in time**.

The command used to create a commit is:

```bash
git commit
```

Most commits include a message describing the change.

Example:

```bash
git commit -m "Add README file"
```