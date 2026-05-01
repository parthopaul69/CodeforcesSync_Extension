<div align="center">
  <h1>⚡ CodeforcesSync</h1>
  <img src="icon128.png" width="128" alt="CodeforcesSync Logo" />
  <p><b>Automatically sync every Accepted Codeforces submission — past and future — directly to your GitHub.</b></p>
</div>

---

## 🌟 Overview

**CodeforcesSync** is a Chrome/Edge browser extension that monitors your Codeforces activity and automatically pushes every `Accepted` solution to a GitHub repository of your choice.

It organizes solutions by **rating** and **division**, generates a rich `README.md` for each problem including the full problem statement, and now lets you **upload your entire submission history in one click** — with zero duplicates.

---

## ✨ Features

| Feature | Description |
|---|---|
| **Auto-Sync** | Background service worker syncs new AC submissions within seconds. |
| **⬆️ Bulk Upload** | Upload your **entire past AC history** in one click — no duplicates, re-uploads safely overwrite. |
| **Rating Folders** | Problems organized by CF rating (`800/`, `1200/`, `Unrated/`). |
| **Division Folders** | Further split by `Div. 1`, `Div. 2`, `Div. 3`, `Div. 4`, `Others`. |
| **Rich READMEs** | Problem statement, time/memory limits, sample I/O, tags — all scraped and formatted as Markdown. |
| **15+ Languages** | C++, Python, Java, Kotlin, Rust, Go, C#, JavaScript, and more. |
| **No Duplicates** | GitHub upsert via SHA — re-running bulk upload overwrites existing files, never creates duplicates. |
| **Gym Support** | Handles Gym and unrated contests cleanly. |
| **Local Privacy** | Tokens stored only in your browser's local storage. |

---

## ⬆️ Bulk Upload — Upload All Past Accepted

The standout new feature. One button uploads your **entire Codeforces accepted submission history** to GitHub.

**How it works:**
1. Open the extension popup → click **"⬆️ Upload All Past Accepted"**
2. The extension fetches **all** your accepted submissions from the Codeforces API (paginated, handles any history size)
3. Deduplicates by problem — keeps the **fastest accepted** submission per problem
4. Uploads each one to GitHub with full problem statement + source code
5. A live progress bar + log shows every upload in real time

**Re-run anytime safely** — if a problem is already in your repo, it gets **overwritten cleanly** (no duplicate files or folders).

```
⬆️ Upload All Past Accepted
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  72%
Uploading 63/87…                           72%
✓ 4A — Watermelon
✓ 1A — Theatre Square
✓ 71A — Way Too Long Words
…
```

---

## 📁 Repository Structure

```text
your-repo/
├── 800/
│   └── Div. 2/
│       └── 4A - Watermelon/
│           ├── 4A - Watermelon.cpp       ← Accepted source code
│           └── README.md                 ← Full problem statement
├── 1200/
│   └── Div. 3/
│       └── 1100C - Some Problem/
│           ├── 1100C - Some Problem.py
│           └── README.md
├── Unrated/
│   └── Others/
│       └── 100001A - Gym Problem/
│           ├── 100001A - Gym Problem.cpp
│           └── README.md
```

---

## 🗂️ Generated Problem README Preview

Each synced problem gets a `README.md` like this:

> ### A. Theatre Square
>
> | Field | Value |
> |---|---|
> | **Contest** | [1](https://codeforces.com/contest/1) |
> | **Problem** | [1A — Theatre Square](https://codeforces.com/contest/1/problem/A) |
> | **Rating** | 1000 |
> | **Tags** | math |
> | **Verdict** | ✅ Accepted |
> | **Language** | C++23 (GCC 14-64) |
> | **Runtime** | 31 ms |
> | **Memory** | 100 KB |
>
> | ⏱ Time Limit | 💾 Memory Limit |
> |---|---|
> | 1 second | 256 megabytes |
>
> *(Full problem statement, input/output spec, and examples follow…)*

---

## ⚙️ Setup Instructions

### Step 1 — Create a GitHub Repository

1. Log in to [GitHub](https://github.com/).
2. Create a new **empty** repository (e.g., `Codeforces`). Public or private — your choice.
3. Do **not** initialize it with a README, `.gitignore`, or License.

### Step 2 — Generate a GitHub Personal Access Token (PAT)

1. Go to: [GitHub → Settings → Developer Settings → Personal access tokens → Classic](https://github.com/settings/tokens/new?scopes=repo&description=CodeforcesSync)
2. Name it `CodeforcesSync`.
3. Set **Expiration** to `No expiration`.
4. Under **Scopes**, check only **`repo`**.
5. Click **Generate token** and **copy it immediately** (you won't see it again).

### Step 3 — Install the Extension

1. Download and unzip `CodeforcesSync_Extension.zip`.
2. Open `chrome://extensions` (Chrome) or `edge://extensions` (Edge).
3. Enable **Developer Mode** (toggle in the top-right corner).
4. Click **Load Unpacked** and select the unzipped `CodeforcesSync_Extension` folder.
5. Pin the extension: click 🧩 in the toolbar → pin CodeforcesSync.

### Step 4 — Configure the Extension

1. Click the ⚡ **CodeforcesSync** icon → click **⚙️ Settings**.
2. Fill in:

| Field | What to enter |
|---|---|
| **Codeforces Handle** | Your exact CF username (e.g., `tourist`) |
| **GitHub Username** | Your GitHub username (e.g., `parthopaul69`) |
| **Repository Name** | Repo name from Step 1 (e.g., `Codeforces`) — not the full URL |
| **Personal Access Token** | The `ghp_...` token from Step 2 |

3. Click **Save & Test Connection** → you should see ✅ `Configuration saved and verified!`

### Step 5 — Sync Future Submissions

Submit any solution on Codeforces. Once the verdict is **Accepted**, your code + problem statement will appear on GitHub within ~10 seconds automatically.

### Step 6 — Upload Past Accepted Submissions

1. Click the ⚡ CodeforcesSync popup icon.
2. Click **"⬆️ Upload All Past Accepted"**.
3. Watch the progress bar — every unique AC problem uploads automatically.
4. You can safely click it again later — no duplicates will be created.

---

## 🤝 Credits

**Created & Maintained by:**
- [parthopaul69](https://github.com/parthopaul69)

---

<p align="center">Made for competitive programmers 🐸</p>
