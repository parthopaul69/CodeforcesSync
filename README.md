<h1 align="center">⚡ CodeforcesSync</h1>

<p align="center">
  <b>Automated, enterprise-grade synchronization of Codeforces submissions.</b>
</p>

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [How it Works](#-how-it-works)
- [Setup Guide](#-setup-guide)
- [Repository Structure](#-repository-structure)
- [Detailed Technical Specifications](#-detailed-technical-specifications)
- [Troubleshooting & FAQ](#-troubleshooting--faq)
- [Security & Ethics](#-security--ethics)
- [Credits & Contribution](#-credits--contribution)
- [License](#-license)

---

## 🚀 Overview

**CodeforcesSync** is a high-performance, open-source browser extension built for the competitive programming community. It bridges the gap between solving and documentation by capturing every `Accepted` submission on Codeforces and pushing it directly to your GitHub repository in a structured, professional format.

This extension is built on **Manifest V3**, ensuring modern standards of efficiency, security, and long-term reliability.

---

## ✨ Key Features

- **Automated Workflow** — Submissions are detected and synced within ~10 seconds of a successful verdict.
- **Intelligent Organization** — Categorizes problems by their official Codeforces rating.
- **Full Problem Documentation** — Every problem folder includes a Markdown-formatted `README.md` with:
  - Scraped problem statement, including LaTeX support.
  - Time and memory limits.
  - Input/Output specifications and sample cases.
- **Language Fidelity** — Perfect source code preservation with correct file extensions for 15+ languages.
- **Resilience Engine** — Automatic handling of Codeforces Gym contests and Edge-case URLs.
- **Offline Integrity** — Stores credentials and status locally; never communicates with third-party servers.

---

## 🛠 How it Works

1. **Detection**: The content script identifies a successful `Accepted` result on a Codeforces status page.
2. **Polling**: The background worker queries the Codeforces API to retrieve metadata (rating, tags, problem code).
3. **Scraping**: The worker fetches the problem page and submission page to extract the full statement and source code.
4. **Synchronization**: The GitHub REST API is used to atomically create or update files in your repository.

---

## ⚙️ Setup Guide

### 1. Repository Creation
1. Go to your GitHub profile and create a **new repository** (e.g., `Codeforces`).
2. **Important**: Do not initialize with a README if you want the extension to create the hierarchy.

### 2. Authentication (GitHub PAT)
1. Navigate to: [GitHub Developer Settings](https://github.com/settings/tokens/new?scopes=repo&description=CodeforcesSync).
2. Set Expiration based on your preference (**No expiration** is recommended for continuous sync).
3. Select the **`repo`** scope (full control of private/public repositories).
4. Click **Generate token** and copy it immediately to a secure location.

### 3. Extension Configuration
1. Install the extension via **Load Unpacked** in Developer Mode.
2. Click the extension icon and select **Settings** ⚙️.
3. Provide the following details:
   - **Codeforces Handle**: Your exact profile username (e.g., `parthopaul69`).
   - **GitHub Username**: Your GitHub handle.
   - **Repository Name**: Only the name of the repo (e.g., `Codeforces`), **not the full URL**.
   - **Personal Access Token**: The `ghp_` token you generated.
4. Click **Save & Test Connection**. A notification will confirm success.

---

## 📁 Repository Structure

Your code is archived in a professional, navigable hierarchy:

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
## 💻 Detailed Technical Specifications

| Feature | Specification |
|---|---|
| **Standards** | Manifest V3 (MV3) |
| **API Integration** | Codeforces REST API, GitHub REST API v3 |
| **Data Cleaning** | Regex-based HTML stripping and Entity Decoding |
| **Languages** | C++, C, Python, Java, Kotlin, Rust, Go, JS, and more |
| **Security** | `chrome.storage.local` (local only, no external servers) |

---

## ❓ Troubleshooting & FAQ

**Q: Why isn't my code syncing?**
- **Check Credentials**: Ensure your token hasn't expired and your repo name is correct (not a URL).
- **Accepted Verdict**: The extension only syncs problems with an `Accepted` status.
- **Reload**: If you just updated the extension or changed settings, click the **↻ refresh** button on the extension page.

**Q: How do I handle multiple accounts?**
- You can change the handle in the settings at any time, but only one account is monitored at a time.

**Q: Can I sync past submissions?**
- The extension starts syncing from your latest submission upon installation. To sync older problems, you may need to re-submit or manually trigger a poll.

---

## 🔒 Security & Ethics

- **Zero Data Harvesting**: We do not track users. Your GitHub token is your own.
- **API Respect**: We use standard polling intervals to avoid overloading Codeforces or GitHub servers.
- **Local Sovereignty**: All settings are stored within your browser's private storage.

---

## 🤝 Credits & Contribution

Contributions to the codebase are encouraged. Feel free to open a Pull Request or report an issue.

**Project Lead & Maintainer:**
- [parthopaul69](https://github.com/parthopaul69)

---

## 📄 License

This project is licensed under the **MIT License**. Refer to the [LICENSE](./LICENSE) file for the full legal text.

<p align="center">Built with precision for the next generation of Competitive Programmers.</p>
