<div align="center">
  <h1>⚡ CodeforcesSync</h1>
  <p><b>A professional-grade automated synchronization tool for competitive programmers.</b></p>
</div>

<hr />

## 🌟 Executive Summary

**CodeforcesSync** is a high-performance browser extension (Manifest V3) compatible with Google Chrome and Microsoft Edge. It bridges the gap between competitive programming and version control by automatically synchronizing every "Accepted" Codeforces submission to a designated GitHub repository. 

Designed for scalability and organization, it categorizes solutions by problem rating, generates rich metadata, and handles edge cases like Gym contests and various programming languages with clinical precision.

---

## ✨ Primary Features

- ✅ **Autonomous Synchronization** — Zero-click operation. After initial setup, every accepted solution is pushed to GitHub within seconds.
- 📂 **Rating-Driven Hierarchy** — Problems are strictly categorized by their official Codeforces rating (`800/`, `1200/`, `3500/`, etc.).
- 🗒️ **Dynamic Documentation** — Automatically generates a `README.md` for every problem folder, featuring:
  - Markdown-formatted problem statements.
  - Runtime and memory usage metrics.
  - Sample test cases with input/output blocks.
- 🔍 **Gym & Educational Support** — Specialized logic to handle Gym contests and unrated problems seamlessly via `/gym/` URL redirection.
- 🛡️ **Encryption & Privacy** — GitHub Personal Access Tokens are stored locally using browser-level encryption (`chrome.storage.local`).
- 🚀 **Polyglot Support** — Intelligent detection and extension mapping for 15+ programming languages.

---

## 🏗️ Project Architecture

CodeforcesSync utilizes a non-intrusive background service worker architecture to ensure stability and battery efficiency.

```text
your-repo/
├── 800/                        # Rating-based categorization
│   ├── 1A/                     # Problem-specific unique folder
│   │   ├── README.md           # Scraped problem statement, limits, and links
│   │   └── 1A.cpp              # Formatted source code (Preserves headers)
│   └── 71A/
│       ├── README.md
│       └── 71A.py
├── 1200/
│   └── 1100C/
│       ├── README.md
│       └── 1100C.java
```

---

## ⚙️ Deployment & Setup Guide

### Phase 1: GitHub Repository Initialization
1. Create a **Public** or **Private** repository at [github.com/new](https://github.com/new).
2. Note your repository name (e.g., `Codeforces`). **Do not use the full URL.**

### Phase 2: Generating Authentication
1. Navigate to your [GitHub Developer Settings](https://github.com/settings/tokens/new?scopes=repo&description=CodeforcesSync).
2. Set the expiration to **No expiration** for permanent sync.
3. Select the **`repo`** scope (Full control of private/public repositories).
4. **Copy the generated Personal Access Token (PAT)** immediately.

### Phase 3: Extension Configuration
1. Access `chrome://extensions` or `edge://extensions` in your browser.
2. Toggle **Developer Mode** in the top-right corner.
3. Select **Load Unpacked** and navigate to this project's directory.
4. Open the extension popup from the toolbar and select **Settings** ⚙️.
5. Provide your Codeforces Handle, GitHub Username, Repository Name, and PAT.
6. Click **Save & Test Connection**. A confirmation notification will appear upon success.

---

## 🔐 Security & Privacy Standards

CodeforcesSync is built with a **Private-by-Default** philosophy:
- **No Third-Party Servers**: Communications are strictly peer-to-peer (Codeforces API ↔ Browser ↔ GitHub API).
- **Token Security**: Your Personal Access Token is never exposed in logs or transmitted as plain text. 
- **Permissions**: The extension only requests minimum necessary permissions (`storage`, `alarms`, `notifications`).

---

## 🛠️ Performance & Maintenance

- **Polling Frequency**: Every 60 seconds (optimized for browser resource consumption).
- **Verification**: Each commit contains the submission ID in the message to prevent duplication.
- **Support**: For bugs or feature requests, please open an issue on the GitHub repository.

---

## 🤝 Maintenance & Credit

This project is actively maintained to ensure compatibility with evolving browser and Codeforces API standards.

**Lead Developer:**
- [parthopaul69](https://github.com/parthopaul69)

---

## 📄 Licensing

Copyright (c) 2026 Partho. All rights reserved.

<hr />
<div align="center">
  <sub>Developed for the competitive programming community. ✨</sub>
</div>
