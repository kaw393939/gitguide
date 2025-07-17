Here is a well-formatted **Git Setup Guide** page you can use in your Canvas LMS. It includes installation instructions for both Mac and Windows, the required configuration commands, and a narrative explaining their importance in a student-friendly tone. You can copy and paste this into Canvas, or into a Markdown file if you're linking to it from elsewhere.

---

# 🛠️ Git Setup Guide

Welcome to your first step toward mastering version control! Before you can use Git for tracking your projects, you need to install it and tell it who you are. Follow the setup instructions below for your operating system.

---

## 💻 Installing Git

### 🪟 Windows

1. Visit: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. The download should start automatically. Run the installer.
3. Use the default settings during installation unless instructed otherwise.
4. After installing, open **Git Bash** from your Start menu.

✅ **Verify Installation**
Open Git Bash and type:

```bash
git --version
```

You should see a version number like `git version 2.43.0`

---

### 🍏 macOS

**Option 1: Using Xcode Command Line Tools**

1. Open **Terminal**
2. Type:

```bash
git --version
```

3. If Git is not installed, macOS will prompt you to install the command line developer tools. Click “Install”.

**Option 2: Using Homebrew (recommended for devs)**

If you have Homebrew installed:

```bash
brew install git
```

✅ **Verify Installation**

```bash
git --version
```

---

## 🔧 Configuration

Once Git is installed, you must set your identity (name and email). This information will be attached to every commit you make.

### 🔧 Configuration Commands

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

### 📚 Example Format (Use This in Your README.md)

#### 🔧 Configuration

```bash
git config --global user.name "Alice Student"
git config --global user.email "alice@example.com"
```

**What it does:**
Sets your name and email so your commits are properly attributed.

**Narrative:**
Before you start using Git, you tell it who you are. Just like putting your name on your homework, this ensures your commits are properly attributed when working alone or on a team.

---

### ✅ Check Your Configuration

You can check your settings at any time:

```bash
git config --global --list
```

You should see:

```
user.name=Alice Student
user.email=alice@example.com
```

---

If you'd like, I can turn this into a downloadable PDF or generate a Markdown version for GitHub Pages or your class resource repo. Would you like that?
