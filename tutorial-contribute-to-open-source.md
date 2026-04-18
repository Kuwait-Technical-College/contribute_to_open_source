# Tutorial: Your First Open-Source Contribution

### Kuwait Technical College (ktech)

**Using VS Code, the Terminal, and GitHub Copilot to Contribute to a Real Project**

---

## Lesson Overview

| | |
|---|---|
| **Duration** | 2 – 2.5 hours |
| **Audience** | Complete beginners — no prior experience with VS Code, Git, or the terminal required |
| **OS** | Windows (notes for macOS included where relevant) |
| **End Goal** | Each student adds a new cybersecurity zen koan to an open-source app and submits a Pull Request on GitHub |
| **Repository** | [Kuwait-Technical-College/cybersecurity_zen_koans_app](https://github.com/Kuwait-Technical-College/cybersecurity_zen_koans_app) |

> 🎥 **Video walkthrough**: Prefer to follow along with a video? Watch the full tutorial on YouTube: [https://www.youtube.com/watch?v=a8poI7DmBYs](https://www.youtube.com/watch?v=a8poI7DmBYs)

## What Students Will Learn

- How to use VS Code (editor, terminal, extensions)
- Basic terminal/command-line commands
- Git fundamentals (clone, add, commit, push)
- GitHub workflow (fork, pull request)
- Using AI (GitHub Copilot) to assist with development

## About the App

**Cybersecurity Zen Koans** is a real mobile app built with Flutter, available on both the [App Store](https://github.com/Kuwait-Technical-College/cybersecurity_zen_koans_app) and [Google Play Store](https://github.com/Kuwait-Technical-College/cybersecurity_zen_koans_app). The app displays short, zen-style sayings about cybersecurity — each one paired with a detailed technical explanation. Think of them as fortune cookies for hackers.

The koans live in a single JSON file (`src/assets/koans.json`) inside the app's open-source repository. That means **anyone can contribute new koans via a Pull Request** — and once your PR is approved and merged, a new version of the app will be published to both stores with your contribution included. Your words will literally be in the hands of people around the world.

## What is Open Source?

Open source means the **source code** of a project is publicly available for anyone to view, use, modify, and share. Instead of software being a locked box that only one company controls, open-source projects are built in the open — anyone can read the code, suggest improvements, or fix bugs.

Some of the most important software in the world is open source: **Linux** (runs most servers on the internet), **Android** (the world's most popular mobile OS), **Firefox**, **VS Code**, **Python**, and thousands more.

> Think of it like a community recipe book. Anyone can read the recipes, try them, suggest improvements, or add new ones. The more people contribute, the better the collection gets.

## Why Should We Care About Open Source?

- **Learning**: Reading real-world code written by experienced developers is one of the fastest ways to learn.
- **Career**: Open-source contributions are visible on your GitHub profile. Employers and recruiters look at them — it shows you can collaborate, write code, and ship real work.
- **Community**: Open source connects you with developers worldwide. You can contribute to projects used by millions of people, from your laptop.
- **Freedom**: Open-source tools are free to use. You're not locked into expensive licenses or vendors.
- **Quality**: When thousands of eyes review code, bugs get caught faster. Open source often produces more reliable and secure software than closed alternatives.

## Open Source and the Internet

The internet as we know it **would not exist without open source**. Almost every layer of the technology stack that powers the web is built on open-source projects:

| Layer | Open-Source Examples |
|---|---|
| Operating systems | Linux powers ~96% of the world's top 1 million web servers |
| Web servers | Nginx, Apache |
| Programming languages | Python, JavaScript (Node.js), PHP, Ruby, Go, Rust |
| Databases | MySQL, PostgreSQL, MongoDB |
| Frameworks | React, Django, Flutter, Express |
| Infrastructure | Docker, Kubernetes, Terraform |
| Version control | Git itself is open source (created by Linus Torvalds, who also created Linux) |

When you visit any website — Google, YouTube, Wikipedia, your bank — you are almost certainly using open-source software, even if you don't see it. The internet was built by people sharing their work openly.

## AI and Open Source

The AI revolution is deeply tied to open source:

- **Most AI frameworks are open source**: TensorFlow, PyTorch, scikit-learn, Hugging Face Transformers — the tools researchers and companies use to build AI are free and open.
- **Open-source models**: Projects like Meta's LLaMA, Mistral, and Stable Diffusion release powerful AI models for anyone to use, study, and improve.
- **GitHub Copilot** (the AI assistant you'll use today) was trained on open-source code. Without millions of developers sharing their work publicly, AI coding assistants would not exist.
- **AI helps open source back**: Tools like Copilot make it easier for beginners to contribute to projects — it can explain code, generate boilerplate, and help you write your first Pull Request (exactly what we're doing today).

Open source and AI fuel each other: open code trains better AI, and better AI helps more people write and contribute open code.

## How It All Connects to Cybersecurity

Cybersecurity sits at the intersection of all of this:

- **Open-source security tools**: Many of the tools security professionals use daily are open source — Wireshark, Metasploit, Snort, OWASP ZAP, Nmap. Understanding open source is essential for a career in cybersecurity.
- **Transparency builds trust**: When security software is open source, anyone can audit the code. There are no hidden backdoors. This is why governments and enterprises often prefer open-source security tools.
- **Vulnerabilities are found faster**: With open-source code, the global security community can find and fix vulnerabilities quickly. The Log4Shell vulnerability (2021) was discovered and patched within days because Log4j was open source.
- **AI in cybersecurity**: AI is increasingly used for threat detection, malware analysis, and automated security testing. Many of these AI-powered security tools are built on open-source frameworks.
- **The app you're contributing to today** is about cybersecurity wisdom. By adding a koan, you're helping spread cybersecurity awareness through a real, publicly available application.

> **The bottom line**: Open source, the internet, AI, and cybersecurity are all deeply interconnected. By learning to contribute to open source today, you're stepping into the ecosystem that powers modern technology.

---

## Phase 0 — Pre-Class Setup

**⏱ ~15 minutes** (ideally sent to students as pre-work before class)

> **Instructor Note**: If students arrive without completing setup, allocate the first 15 minutes of class. Have a printed or projected checklist. Walk around and help.

### 0.1 — Install Visual Studio Code

1. Go to **https://code.visualstudio.com/**
2. Click **Download for Windows**
3. Run the installer with default settings
4. **Important**: On the "Select Additional Tasks" screen, check ✅ **"Add to PATH"** — this lets you open VS Code from the terminal later

### 0.2 — Install Git for Windows

1. Go to **https://git-scm.com/download/win**
2. Download and run the installer
3. Accept all default settings (click Next through each screen)
4. This installs both `git` (version control) and **Git Bash** (a Linux-like terminal on Windows)

### 0.3 — Create a GitHub Account

1. Go to **https://github.com/join**
2. Sign up with a personal email address
3. Verify your email
4. **Remember your username and password** — you will need them later
5. Follow the college's GitHub account: **https://github.com/Kuwait-Technical-College** — click the **Follow** button on the organization page

### 0.4 — Install the GitHub Copilot Extension

1. Open VS Code
2. Press **Ctrl+Shift+X** to open the Extensions sidebar
3. Search for **"GitHub Copilot"**
4. Click **Install** on "GitHub Copilot" (by GitHub)
5. It will also install "GitHub Copilot Chat" automatically
6. Click **Sign in to GitHub** when prompted — sign in with the account you just created
7. Copilot's free tier is available to all GitHub accounts

> **Fallback**: If a student cannot activate Copilot (unverified account, region issue), they can use [Gemini free](https://gemini.google.com) in a browser tab as an alternative. The workflow is the same — ask AI to generate a koan, then paste it in.

### ✅ Setup Checklist

- [ ] VS Code installed and opens correctly
- [ ] Git installed (open a terminal and type `git --version` — should show a version number)
- [ ] GitHub account created and email verified
- [ ] GitHub Copilot extension installed and signed in

---

## Phase 1 — Orientation: VS Code and the Terminal

**⏱ ~20 minutes**

**Goal**: Students can navigate VS Code and run basic terminal commands.

### 1.1 — Tour of VS Code

Open VS Code. Point out these key areas:

| Area | Shortcut | What It Does |
|---|---|---|
| **File Explorer** | `Ctrl+Shift+E` | Browse files and folders in your project |
| **Search** | `Ctrl+Shift+F` | Search across all files |
| **Source Control** | `Ctrl+Shift+G` | Visual Git interface |
| **Extensions** | `Ctrl+Shift+X` | Install add-ons (like Copilot) |
| **Terminal** | `` Ctrl+` `` | Built-in command line at the bottom |
| **Command Palette** | `Ctrl+Shift+P` | Search for any VS Code action |

> **Instructor Tip**: Spend a moment just opening and closing each panel so students know where everything is.

### 1.2 — Opening the Terminal

1. Press `` Ctrl+` `` (the backtick key, usually above Tab)
2. A terminal panel opens at the bottom of VS Code
3. This is a real command line — you can do everything here that you'd do in a separate terminal app

> **What is a terminal?** Think of it as a text-based version of File Explorer. Instead of clicking to open folders, you type commands. Developers use the terminal because it's faster and more powerful — and many tools (like Git) are designed to be used this way.

### 1.3 — Essential Terminal Commands

Type each command and observe the result:

| Command (Windows) | Command (macOS/Linux) | What It Does |
|---|---|---|
| `cd` | `pwd` | Shows your current location (directory) |
| `dir` | `ls` | Lists files and folders in current location |
| `cd Desktop` | `cd Desktop` | Move into the Desktop folder |
| `cd ..` | `cd ..` | Move up one level |
| `mkdir my-folder` | `mkdir my-folder` | Create a new folder |
| `cls` | `clear` | Clear the terminal screen |

> **Key concept**: You are always "inside" a folder. The terminal shows you which folder you're in (this is called your **working directory**). When you type `cd`, you move to a different folder, just like double-clicking a folder in File Explorer.

### 1.4 — Practice Exercise

Follow these steps in your terminal:

```
cd Desktop
mkdir projects
cd projects
dir
```

You should now be inside an empty `projects` folder on your Desktop.

> **Instructor checkpoint**: Walk around. Every student should see `Desktop\projects` (or similar) as their current location. Help anyone who gets lost — a common mistake is misspelling folder names.

---

## Phase 2 — Git and GitHub: Fork and Clone

**⏱ ~25 minutes**

**Goal**: Students have a personal copy of the project on their computer.

### 2.1 — Key Concepts (5 minutes)

Before we touch any tools, understand these terms:

| Concept | Analogy |
|---|---|
| **Git** | Like "Track Changes" in Microsoft Word, but for code. It remembers every version of every file. |
| **GitHub** | A website that hosts Git projects — like Google Drive, but for code. |
| **Repository (repo)** | A project folder tracked by Git. |
| **Fork** | Making your own personal copy of someone else's project on GitHub. |
| **Clone** | Downloading your fork from GitHub to your computer. |
| **Commit** | Saving a snapshot of your changes (with a description of what you changed). |
| **Push** | Uploading your commits from your computer back to GitHub. |
| **Pull Request (PR)** | Asking the original project owner to review and accept your changes. |

**The full workflow looks like this:**

```
Fork (on GitHub) → Clone (to your computer) → Edit → Commit → Push → Pull Request
```

### 2.2 — Fork the Repository

1. Open your browser and go to:
   **https://github.com/Kuwait-Technical-College/cybersecurity_zen_koans_app**
2. Click the **Fork** button (top-right corner of the page)
3. On the "Create a new fork" page, keep all defaults
4. Click **Create fork**

You now have your own copy at `https://github.com/YOUR-USERNAME/cybersecurity_zen_koans_app`

> **Instructor Tip**: Show what the fork looks like — it says "forked from Kuwait-Technical-College/cybersecurity_zen_koans_app" at the top. Emphasize: "You are now working on YOUR copy. Nothing you do here affects the original project until you submit a Pull Request."

### 2.3 — Clone to Your Computer

1. On **your fork's** GitHub page, click the green **Code** button
2. Make sure **HTTPS** is selected
3. Click the 📋 copy button to copy the URL
4. Go back to VS Code's terminal (you should still be in `Desktop\projects`)
5. Type:

```
git clone https://github.com/YOUR-USERNAME/cybersecurity_zen_koans_app.git
```

*(Replace `YOUR-USERNAME` with your actual GitHub username)*

6. Wait for it to finish, then:

```
cd cybersecurity_zen_koans_app
```

7. Open this folder in VS Code:

```
code .
```

A new VS Code window will open with the project loaded. You should see folders like `src/`, files like `README.md`, etc.

> **Troubleshooting**: If `code .` doesn't work, use **File → Open Folder** in VS Code and navigate to `Desktop\projects\cybersecurity_zen_koans_app`.

### 2.4 — Configure Your Git Identity

This is a one-time setup. Git needs to know who you are so it can label your changes:

```
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Use the same email you used for GitHub.

### 2.5 — Explore the Project

In VS Code's File Explorer (left sidebar), navigate to:

```
src → assets → koans.json
```

Click on `koans.json` to open it. This is the file you will edit. It contains **217 cybersecurity zen koans** — short, thought-provoking sayings about cybersecurity, each with a technical explanation.

Scroll through it and read a few. Each koan looks like this:

```json
{
  "koanText": "The strongest firewall is useless against a user who clicks 'Allow'.",
  "technicalExplanation": "This koan highlights the critical importance of user behavior in security...",
  "uniqueCode": "7H93FT"
}
```

| Field | Description |
|---|---|
| `koanText` | The zen koan — a short, wise saying about cybersecurity |
| `technicalExplanation` | A detailed explanation of the cybersecurity concept behind the koan |
| `uniqueCode` | A unique 6-character code (letters and numbers) that identifies this koan |

> **Instructor checkpoint**: Every student should have `koans.json` open in VS Code. If anyone is stuck, help them navigate to `src/assets/koans.json`.

---

## Phase 3 — Using Copilot to Create a New Koan

**⏱ ~25 minutes**

**Goal**: Students use GitHub Copilot to generate a new koan and add it to the file.

### 3.1 — Open Copilot Chat

1. Press **Ctrl+Shift+I** to open Copilot Chat (or click the Copilot icon in the left sidebar)
2. A chat panel opens — this is your AI assistant

> **What is GitHub Copilot?** It's a free AI assistant built into VS Code. You can ask it questions, have it explain code, or ask it to generate content. Think of it as a knowledgeable coding partner you can chat with.

### 3.2 — Generate a Koan

Make sure `koans.json` is open in the editor (Copilot can see your open files for context).

In the Copilot Chat, type a prompt like:

> Generate a new cybersecurity zen koan in JSON format matching the structure in my open koans.json file. The koan should be about **phishing**. Include the fields: koanText, technicalExplanation, and a unique 6-character alphanumeric uniqueCode.

**Pick your own topic!** Some ideas:
- Phishing
- Ransomware
- Two-factor authentication
- Social engineering
- Password security
- Wi-Fi security
- Software updates
- Data privacy

### 3.3 — Review and Iterate

Read the koan Copilot generated. Ask yourself:
- Does the `koanText` sound wise and thought-provoking?
- Is the `technicalExplanation` accurate and informative?
- Does it feel similar in style to the existing koans?

You can ask Copilot to improve it:
- *"Make the koan shorter and more poetic"*
- *"Make the technical explanation more detailed"*
- *"Give me a different koan about the same topic"*

> **Instructor talking point**: "AI is a tool, not a replacement for your brain. Always review what it generates. You are the expert on whether it makes sense and reads well."

### 3.4 — Add the Koan to koans.json

1. In `koans.json`, press **Ctrl+End** to jump to the bottom of the file
2. Find the very last koan entry — it ends with `}` followed by `]` (the closing of the array)
3. Place your cursor **after** the last `}` and **before** the `]`
4. Type a comma `,` after the `}`
5. Paste your new koan

It should look like this:

```json
    "uniqueCode": "Q1PFVW"
  },
  {
    "koanText": "Your new koan text here",
    "technicalExplanation": "Your explanation here",
    "uniqueCode": "YOUR6C"
  }
]
```

6. Save the file: **Ctrl+S**

> **Common mistakes to watch for:**
> - ❌ Missing comma between the last existing koan and your new one
> - ❌ Extra comma after your new koan (before the `]`)
> - ❌ Wrong field names — must be `koanText`, NOT `koan`
> - ✅ VS Code will show **red squiggly underlines** if your JSON has syntax errors — fix them before moving on

### 3.5 — Verify Your uniqueCode is Unique

Your 6-character code must not already exist in the file. Let's use the terminal to check.

**Option A — Use `findstr` (Windows Command Prompt / PowerShell):**

```
findstr "YOUR6C" src\assets\koans.json
```

**Option B — Use `grep` (Git Bash / macOS / Linux):**

```
grep "YOUR6C" src/assets/koans.json
```

Replace `YOUR6C` with the actual code from your koan.

- **If nothing appears** → Your code is unique. You're good!
- **If a line appears** → That code already exists. Ask Copilot to generate a different one, or change a character manually.

> **Instructor talking point**: "`grep` is one of the most useful commands in all of computing. It searches for text inside files. The name stands for **G**lobally search for a **R**egular **E**xpression and **P**rint. On Windows, the equivalent is `findstr`. Since you installed Git for Windows, you actually have `grep` available too — try switching your terminal to Git Bash (click the dropdown arrow next to the `+` button in the terminal panel)."

**Bonus — count how many koans exist now:**

```
grep -c "uniqueCode" src/assets/koans.json
```

This counts how many lines contain the word "uniqueCode". After adding yours, it should print **218**.

> **Instructor checkpoint**: Every student should have a valid, saved `koans.json` with their new koan at the end, no red underlines, and a confirmed-unique code.

---

## Phase 4 — Commit, Push, and Pull Request

**⏱ ~25 minutes**

**Goal**: Students submit their change back to the original repository via a Pull Request.

### 4.1 — Check What Changed

In the terminal:

```
git status
```

You should see:

```
modified:   src/assets/koans.json
```

This means Git detected your changes. To see exactly what changed:

```
git diff src/assets/koans.json
```

- Lines in **green** (with `+`) are lines you added
- Lines in **red** (with `-`) are lines you removed

> **Visual alternative**: Click the **Source Control** icon in VS Code's sidebar (`Ctrl+Shift+G`). You'll see `koans.json` listed as a changed file. Click it to see a side-by-side comparison.

### 4.2 — Stage Your Changes

Tell Git which files you want to include in your commit:

```
git add src/assets/koans.json
```

> **What does "staging" mean?** Think of it like putting items in a box before shipping. You choose exactly which changes go into this commit. This is useful when you've changed multiple files but only want to commit some of them.

### 4.3 — Commit Your Changes

Save a snapshot of your staged changes with a descriptive message:

```
git commit -m "Add new cybersecurity koan about phishing"
```

Change "phishing" to whatever topic your koan is about.

> **What is a commit?** A commit is like a save point in a video game. It records the exact state of your files at that moment. The `-m` flag lets you write a message describing what you changed.

### 4.4 — Push to GitHub

Upload your commit from your computer to your GitHub fork:

```
git push origin main
```

- `origin` means "the GitHub repository you cloned from" (your fork)
- `main` is the branch name (the main line of development)

> **Authentication**: Windows will likely open a browser window asking you to sign in to GitHub. Sign in and authorize Git. This should only happen once.
>
> **Troubleshooting**: If you get an authentication error, ask your instructor for help. You may need to generate a [Personal Access Token](https://github.com/settings/tokens) and use it as your password.

### 4.5 — Verify on GitHub

1. Open your browser and go to your fork: `https://github.com/YOUR-USERNAME/cybersecurity_zen_koans_app`
2. You should see your recent commit at the top (e.g., "Add new cybersecurity koan about phishing")
3. Click on `src/assets/koans.json` and scroll to the bottom to see your koan

### 4.6 — Create a Pull Request

Now ask the original project to accept your change:

1. On your fork's page, you should see a banner that says: **"This branch is 1 commit ahead of Kuwait-Technical-College:main"**
2. Click **Contribute** → **Open pull request**
3. Fill in the details:
   - **Title**: `Add new koan: [brief description of your koan]`
   - **Description**: Write 1–2 sentences about what koan you added and what cybersecurity topic it covers
4. Click **Create pull request**

### 🎉 Congratulations!

You just:
- Used a professional code editor (VS Code)
- Navigated the terminal like a developer
- Used AI (GitHub Copilot) to help you create content
- Used Git to track and submit your changes
- Contributed to a real open-source project on GitHub

Your Pull Request is now visible on the [project's Pull Requests page](https://github.com/Kuwait-Technical-College/cybersecurity_zen_koans_app/pulls). The project maintainer will review it and may merge it into the app!

> **What happens next?** Once your Pull Request is approved and merged, a new version of the Cybersecurity Zen Koans app will be published to the **App Store** and **Google Play Store** — with your koan included. You'll be a published open-source contributor with your work in a real app used by real people. 🚀

---

## Phase 5 — Wrap-Up and Recap

**⏱ ~10 minutes**

### The Workflow You Learned

```
┌─────────┐     ┌─────────┐     ┌─────────┐     ┌─────────┐     ┌─────────┐     ┌─────────┐
│  FORK   │ ──▶ │  CLONE  │ ──▶ │  EDIT   │ ──▶ │ COMMIT  │ ──▶ │  PUSH   │ ──▶ │   PR    │
│(GitHub) │     │(Terminal)│     │(VS Code)│     │  (Git)  │     │  (Git)  │     │(GitHub) │
└─────────┘     └─────────┘     └─────────┘     └─────────┘     └─────────┘     └─────────┘
 Your copy      Download it     Change the      Save a          Upload to       Ask original
 on GitHub      to computer     file            snapshot        your fork       to merge
```

### Skills You Practiced

| Skill | Examples |
|---|---|
| **VS Code** | Opening files, using the terminal, extensions, Copilot Chat |
| **Terminal** | `cd`, `dir`/`ls`, `mkdir`, `findstr`/`grep`, `cls`/`clear` |
| **Git** | `git clone`, `git status`, `git diff`, `git add`, `git commit`, `git push` |
| **GitHub** | Creating an account, forking, creating a Pull Request |
| **AI-Assisted Development** | Using Copilot to generate content, reviewing and iterating on AI output |

### Resources to Keep Learning

| Resource | Link |
|---|---|
| VS Code Documentation | https://code.visualstudio.com/docs |
| Git Basics (free online book) | https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control |
| GitHub Skills (interactive courses) | https://skills.github.com/ |
| GitHub Copilot Documentation | https://docs.github.com/en/copilot |

### Bonus Challenges (Fast Finishers)

1. **Add 2 or more koans** in a single Pull Request
2. **Review another student's PR**: Go to the [Pull Requests page](https://github.com/Kuwait-Technical-College/cybersecurity_zen_koans_app/pulls), find a classmate's PR, and leave a constructive comment
3. **Explore the codebase**: Look at other files in the repository — the app is built with Flutter (Dart programming language). Can you figure out how `koans.json` gets loaded into the app?
4. **Try `grep` tricks**:
   - `grep -i "firewall" src/assets/koans.json` — search for "firewall" (case-insensitive)
   - `grep -c "koanText" src/assets/koans.json` — count how many koans exist
   - `grep "uniqueCode" src/assets/koans.json | head -5` — show only the first 5 matches

---

## Instructor Notes

### Before Class

- [ ] Test the full workflow yourself (fork → clone → edit → commit → push → PR) to ensure there are no surprises
- [ ] Test Git authentication on a Windows machine similar to the students' setup — the browser-based GitHub login flow via Git Credential Manager should work automatically
- [ ] Prepare a projected browser tab with the repository open so you can demonstrate forking
- [ ] Have a backup plan for Copilot: if the free tier requires verification that some students haven't done, they can use [Gemini free](https://gemini.google.com) in a browser tab to generate their koan

### During Class

- **Walk around frequently** during Phases 2 and 4 — these are where students get stuck most often
- **Common blockers**:
  - Typos in `git clone` URL → have them re-copy from GitHub
  - Wrong directory → use `cd` to navigate to the right folder, or `dir` to see where they are
  - JSON syntax errors → look for red squiggly underlines in VS Code, common issues are missing commas or wrong field names
  - Authentication failures during `git push` → help them sign in via the browser, or set up a Personal Access Token
- **Live-review 1–2 Pull Requests** on the projector near the end to demonstrate what the review process looks like

### Timing Guide

| Phase | Content | Duration |
|---|---|---|
| Intro | What is open source, AI, internet & cybersecurity | ~15 min |
| Phase 0 | Setup (pre-work or start of class) | ~15 min |
| Phase 1 | VS Code and terminal orientation | ~20 min |
| Phase 2 | Fork and clone | ~25 min |
| Phase 3 | Copilot + editing koans.json | ~25 min |
| Phase 4 | Commit, push, pull request | ~25 min |
| Phase 5 | Wrap-up and recap | ~10 min |
| | **Total** | **~2.5 hours** |
