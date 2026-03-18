<h1 align="center">⚡ CodeforcesSync</h1>

<p align="center">
  <b>Automated, seamless synchronization of accepted Codeforces submissions to GitHub.</b>
</p>

---

## 🚀 Overview

**CodeforcesSync** is a professional-grade browser extension for Chrome and Microsoft Edge designed for competitive programmers. It eliminates the manual effort of maintaining a repository of solved problems by automatically detecting, formatting, and pushing every `Accepted` solution to a GitHub repository of your choice.

With CodeforcesSync, you can focus on solving problems while the extension handles your documentation, organization, and version control automatically.

---

## ✨ Key Features

- 🛠 **Zero-Config Sync** — Once authenticated, every successful submission is pushed to GitHub within ~10 seconds.
- 📁 **Intelligent Hierarchy** — Submissions are automatically sorted into folders by **Problem Rating** (e.g., `800/`, `1200/`, `2400/`) for easy navigation.
- 📝 **Rich Problem Manifests** — Every problem folder includes a generated `README.md` containing:
  - Full problem statement scraping (Markdown-formatted).
  - Time and Memory limits.
  - Formatted Input/Output specifications.
  - Sample tests and explanations.
- 💻 **Syntax Fidelity** — Full support for over 15 programming languages with perfect preservation of source code formatting and C++ `#include` headers.
- ⚡ **Gym Problem Support** — Seamlessly detects and syncs problems from Codeforces Gym contests using dedicated fetching logic.
- 🔒 **Privacycentric Architecture** — Your GitHub Personal Access Token (PAT) is stored exclusively in your browser's local storage. No data is transmitted to third-party servers.

---

## 📁 Repository Structure

Your repository is automatically maintained in a clean, professional hierarchy:

```text
your-repo/
├── 800/                        # Rating-based categorization
│   ├── 1A/                     # Problem-specific folder
│   │   ├── README.md           # Problem statement and metadata
│   │   └── 1A.cpp              # Your accepted source code
│   └── 71A/
│       ├── README.md
│       └── 71A.py
├── 1200/
│   └── 1100C/
│       ├── README.md
│       └── 1100C.java
└── unrated/                    # For Gym or unrated problems
    └── 2200A/
        ├── README.md
        └── 2200A.cpp
```

---

## ⚙️ Professional Setup

### 1. Repository Creation
Create a new, empty repository on GitHub (e.g., `Codeforces`). It is recommended to leave the repository empty for the first sync.

### 2. Authentication (GitHub PAT)
Generate a **Personal Access Token (PAT)** with the `repo` scope at [GitHub Settings](https://github.com/settings/tokens/new?scopes=repo&description=CodeforcesSync). For security, set a reasonable expiration or store your token in a password manager.

### 3. Extension Installation
1. Open your browser's extensions page (`chrome://extensions` or `edge://extensions`).
2. Enable **Developer Mode**.
3. Use **Load Unpacked** to select the extension folder.
4. Access the **Settings** ⚙️ from the extension popup.
5. Provide your Codeforces handle, GitHub username, repository name, and the PAT.
6. Click **Save & Test Connection** to verify end-to-end connectivity.

---

## 🔐 Security & Implementation

CodeforcesSync operates as a background service worker using **Manifest V3** standards. It polls the Codeforces API for status updates and uses the GitHub REST API for atomic file updates.

- **Storage**: Authentication tokens are encrypted by the browser and stored in `chrome.storage.local`.
- **Integrity**: Each commit includes performance metrics (Runtime/Memory) in the message for future reference.
- **Reliability**: Robust error handling ensures that intermittent connectivity issues do not result in duplicate commits or lost data.

---

## 🤝 Contributing & Credit

The project was developed with the goal of empowering the competitive programming community. Contributions, bug reports, and feature requests are welcome via Pull Requests or Issues.

**Project Lead:**
- [parthopaul69](https://github.com/parthopaul69)

---

## 📄 License

© 2006-2026 Partho Paul (parthopaul69). All rights reserved.

<p align="center">Made with ❤️ for competitive programmers.</p>
