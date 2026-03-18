<h1 align="center">⚡ CodeforcesSync</h1>

<p align="center">
  <b>Auto-sync your accepted Codeforces submissions to GitHub — fully automatic, zero manual work.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Chrome-MV3-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white"/>
  <img src="https://img.shields.io/badge/Edge-MV3-0078D7?style=for-the-badge&logo=microsoftedge&logoColor=white"/>
  <img src="https://img.shields.io/badge/GitHub_API-integrated-181717?style=for-the-badge&logo=github"/>
  <img src="https://img.shields.io/badge/Codeforces_API-integrated-1F8ACB?style=for-the-badge"/>
</p>

---

## 🌟 What is CodeforcesSync?

**CodeforcesSync** is a free, open-source Chrome/Edge browser extension that watches your Codeforces submissions and automatically pushes every **Accepted** solution to your GitHub repository — organized by problem rating and problem code.

No copy-pasting. No manual commits. Just solve, get accepted, and your GitHub updates itself.

---

## ✨ Benefits

- 🚀 **Fully automatic** — works in the background, no clicks needed after setup
- 📁 **Organized structure** — problems sorted by rating folder (`800/`, `1200/`, etc.)
- 📝 **Rich commit messages** — includes problem code, rating, runtime, and memory
- 🌐 **Multi-language** — supports C++, Python, Java, Kotlin, Rust, Go, C#, JavaScript, and more
- 📖 **Problem README** — each problem folder includes a `README.md` with problem metadata and a link to the problem statement
- 🔒 **Privacy first** — your GitHub token never leaves your browser (stored locally only)
- ⚡ **Fast** — syncs within ~10 seconds of getting Accepted

---

## 📁 Repository Structure

After using CodeforcesSync, your GitHub repo will look like this:

```
your-repo/
├── 800/
│   ├── 1A/
│   │   ├── README.md        ← problem info + CF link
│   │   └── 1A.cpp           ← your accepted solution
│   └── 71A/
│       ├── README.md
│       └── 71A.py
├── 1200/
│   └── 1234B/
│       ├── README.md
│       └── 1234B.java
├── 1600/
│   └── ...
└── unrated/
    └── ...
```

---

## 📝 Commit Message Format

Every commit looks like this:

```
[1A | 800] Accepted | Time: 46ms | Memory: 4096KB
```

---

## 🛠️ Setup (Step by Step)

### Step 1 — Create a GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Name it anything, e.g. `Codeforces`
3. Set it to **Public** or **Private** (your choice)
4. Click **Create repository** — leave it empty (no README needed)

---

### Step 2 — Get a GitHub Personal Access Token

1. Go to 👉 [github.com/settings/tokens/new](https://github.com/settings/tokens/new?scopes=repo&description=CodeforcesSync)
2. Fill in:
   - **Note**: `CodeforcesSync`
   - **Expiration**: `No expiration` (or 1 year)
3. Under **Select scopes**, check only ✅ **`repo`**
4. Click **Generate token**
5. **Copy it immediately** — GitHub only shows it once!

> Your token looks like: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`

---

### Step 3 — Install the Extension

1. Download or clone this repository to your computer
2. Open **Chrome** or **Edge** and go to:
   - Chrome: `chrome://extensions`
   - Edge: `edge://extensions`
3. Enable **Developer Mode** (toggle in top-right corner)
4. Click **Load unpacked**
5. Select the folder where you downloaded CodeforcesSync
6. The extension is now installed ✅

---

### Step 4 — Configure the Extension

1. Click the **⚡ CodeforcesSync** icon in your browser toolbar
   - *(If you don't see it, click the puzzle 🧩 icon and pin it)*
2. Click **⚙️ Settings**
3. Fill in the four fields:

| Field | What to enter |
|---|---|
| **Codeforces Handle** | Your Codeforces username (e.g. `tourist`) |
| **GitHub Username** | Your GitHub username (e.g. `parthopaul69`) |
| **Repository Name** | Just the repo name — **not the URL** (e.g. `Codeforces`) |
| **Personal Access Token** | The token you copied in Step 2 |

4. Click **💾 Save & Test Connection**
5. You should see: ✅ `Configuration saved and verified!`

> ⚠️ **Common mistake**: In the Repository Name field, enter only `Codeforces` — **not** `https://github.com/user/Codeforces`

---

## 🚀 Usage

After setup, just use Codeforces normally:

1. Go to [codeforces.com](https://codeforces.com)
2. Submit a solution to any problem
3. When the verdict is **Accepted** ✅
4. CodeforcesSync automatically:
   - Fetches your solution and problem details
   - Creates/updates the folder in your GitHub repo
   - Makes a commit with runtime and memory info
   - Shows a green **✓** badge on the extension icon
   - Sends a desktop notification

**That's it. Fully automatic.**

---

## 💻 Supported Languages

| Language | File Extension |
|---|---|
| C++ (all variants) | `.cpp` |
| C | `.c` |
| Python / PyPy | `.py` |
| Java | `.java` |
| Kotlin | `.kt` |
| Rust | `.rs` |
| Go | `.go` |
| C# (Mono) | `.cs` |
| JavaScript / Node.js | `.js` |
| Pascal | `.pas` |
| Haskell | `.hs` |
| Ruby | `.rb` |
| Others | `.txt` |

---

## 🔒 Privacy & Security

- Your GitHub token is stored **locally** in your browser (`chrome.storage.local`)
- It is **only** sent to `api.github.com` — never to any third-party server
- Codeforces data is fetched from the **public** Codeforces API
- No account login required — just your CF handle

---

## ❓ Troubleshooting

| Problem | Fix |
|---|---|
| `GitHub repo not accessible: Not Found` | Make sure Repository Name is just `Codeforces`, not the full URL |
| `Codeforces handle not found` | Double-check your exact CF username (case-sensitive) |
| Extension not detecting verdicts | Make sure you're on the verdict page after submission, not the editor |
| No notification on Accepted | Check Chrome/Edge notification permissions for the extension |
| Token expired | Generate a new PAT at github.com/settings/tokens and re-save settings |

---

## 🤝 Contributing

Pull requests are welcome! Feel free to open issues for bugs or feature requests.

---

## 📄 License

MIT — free to use, modify, and distribute.

---

<p align="center">Made with ❤️ for competitive programmers</p>
