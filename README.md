<h1 align="center">⚡ CodeforcesSync</h1>

<p align="center">
  <b>Auto-sync your accepted Codeforces submissions to GitHub — fully automatic, zero manual work.</b>
</p>

<p align="center">
  <a href="https://developer.chrome.com/docs/extensions/mv3/intro/"><img src="https://img.shields.io/badge/Chrome-MV3-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Chrome MV3"/></a>
  <a href="https://learn.microsoft.com/en-us/microsoft-edge/extensions-chromium/"><img src="https://img.shields.io/badge/Edge-MV3-0078D7?style=for-the-badge&logo=microsoftedge&logoColor=white" alt="Edge MV3"/></a>
  <a href="https://docs.github.com/en/rest"><img src="https://img.shields.io/badge/GitHub_API-integrated-181717?style=for-the-badge&logo=github" alt="GitHub API"/></a>
  <a href="https://codeforces.com/apiHelp"><img src="https://img.shields.io/badge/Codeforces_API-integrated-1F8ACB?style=for-the-badge" alt="Codeforces API"/></a>
</p>

---

## 🌟 What is CodeforcesSync?

**CodeforcesSync** is a free, open-source browser extension for Chrome and Edge. It monitors your Codeforces submissions and automatically pushes every **Accepted** solution to your GitHub repository—beautifully organized by problem rating and problem code.

No more copy-pasting. No more manual commits. Focus on the logic; we'll handle the documentation.

---

## ✨ Key Benefits

- 🚀 **Zero Friction** — Runs in the background; syncs within ~10 seconds of getting `Accepted`.
- 📁 **Smart Organization** — Folders sorted by rating (`800/`, `1200/`, etc.) with problem subfolders.
- 📝 **Rich Artifacts** — Each problem folder contains a `README.md` with the full problem statement and a direct link.
- 💻 **Perfect Code** — Preserves all C++ headers (`#include`) and supports 15+ programming languages.
- 🔒 **Secure & Private** — Your GitHub token is stored locally in your browser. It never leaves your machine.
- ⚡ **Gym Support** — Automatically handles Gym problems (using `/gym/` URLs).

---

## 📁 Repository Structure

Your repository will look clean and professional:

```
your-repo/
├── 800/
│   ├── 1A/
│   │   ├── README.md        ← full problem statement + CF link
│   │   └── 1A.cpp           ← your accepted solution
│   └── 71A/
│       ├── README.md
│       └── 71A.py
├── 1200/
│   └── 1234B/
│       ├── README.md
│       └── 1234B.java
└── unrated/
    └── 2200A/               ← for problems without a rating yet
        ├── README.md
        └── 2200A.cpp
```

---

## ⚙️ Setup Instructions

### 1. Create a Repository
1. Create a new repository on GitHub (e.g., `Codeforces`).
2. Keep it empty (don't initialize with README).

### 2. Generate a Personal Access Token (PAT)
1. Go to [GitHub Token Settings](https://github.com/settings/tokens/new?scopes=repo&description=CodeforcesSync).
2. Set Expiration to **No expiration**.
3. Select the **`repo`** scope.
4. **Copy the token** (starts with `ghp_`).

### 3. Install & Configure
1. Open Chrome/Edge Extensions (`chrome://extensions`).
2. Enable **Developer Mode**.
3. Click **Load Unpacked** and select this folder.
4. Click the extension icon → **Settings** ⚙️.
5. Enter your Handle, GitHub Username, Repo Name, and Token.
6. Click **Save & Test Connection**.

---

## 🤝 Contributing & Credit

Contributions are welcome! If you find a bug or have a suggestion, feel free to open an Issue or Pull Request.

**Created & Maintained by:**
- [parthopaul69](https://github.com/parthopaul69)

---

## 📄 License

© 2006-2026 Partho Paul (parthopaul69). All rights reserved.

<p align="center">Made with ❤️ for the Competitive Programming community.</p>
