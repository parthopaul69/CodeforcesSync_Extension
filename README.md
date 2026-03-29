<div align="center">
  <h1>⚡ CodeforcesSync</h1>
  <img src="icon128.png" width="128" alt="CodeforcesSync Logo" />
  <p><b>Automated synchronization of your accepted Codeforces submissions directly to GitHub.</b></p>
</div>

<hr />

 🌟 Overview

**CodeforcesSync** is a professional browser extension for Chrome and Edge that monitors your Codeforces activity and automatically pushes every `Accepted` solution to a GitHub repository of your choice. It organizes your solutions by rating and generates a comprehensive `README.md` for each problem.

---

 ✨ Features

- **Autonomous Sync** — Background service worker syncs within seconds of an accepted verdict.
- **Rating Categorization** — Automatic folder organization by Codeforces rating (e.g., `800/`, `1200/`).
- **Rich Documentation** — Problem statements, time/memory limits, and sample test cases included in each folder.
- **Header Preservation** — Correctly handles C++ `#include` statements and supports 15+ languages.
- **Gym Support** — Specialized logic for Gym and unrated problems.
- **Local Privacy** — Your authentication tokens are stored only in your browser.

---

 🎨 Generated Problem UI Preview

Every synced solution automatically receives a beautifully crafted `README.md` that flawlessly tracks your performance.

>  1A. Theatre Square
> 
> | Field | Value |
> |---|---|
> | **Contest** | [1] |
> | **Problem** | [1A — Theatre Square] |
> | **Rating** | 1000 |
> | **Tags** | math |
> | **Verdict** | ✅ Accepted |
> | **Language** | C++23 (GCC 14-64) |
> | **Runtime** | 31 ms |
> | **Memory** | 100 KB |
> 
> | Item | Value |
> |---|---|
> | **Time Limit** | 1 second |
> | **Memory Limit** | 256 megabytes |

---

 📁 Repository Structure

```text
your-repo/
├── 800/                        # Rating-based categorization
│   ├── 4A.md                   # Scraped problem statement
│   └── 4A.cpp                  # Accepted source code
├── 1200/
│   ├── 1100C.md
│   └── 1100C.java
```

---

 ⚙️ Detailed Setup Instructions

Follow these steps carefully to ensure a seamless connection between Codeforces and GitHub.

 Step 1: Initialize Your GitHub Repository
1. Log in to [GitHub](https://github.com/).
2. Create a new repository (e.g., named `Codeforces`).
3. **Public or Private**: You can choose either.
4. **Important**: Keep the repository empty. Do not initialize with a README or License yet.

 Step 2: Generate a GitHub Personal Access Token (PAT)
1. Navigate to: [GitHub Developer Settings](https://github.com/settings/tokens/new?scopes=repo&description=CodeforcesSync).
2. **Note**: Name it `CodeforcesSync`.
3. **Expiration**: Select `No expiration` to avoid re-configuring the extension later.
4. **Select Scopes**: Check only the box for **`repo`** (this allows the extension to push code to your repositories).
5. Scroll down and click **Generate token**.
6. **Copy the token immediately**: Once you leave the page, you won't be able to see it again.

 Step 3: Install the Extension
1. Download this project folder from the release to your local computer.
2. Unzip it, then open your browser and go to `chrome://extensions` (Chrome) or `edge://extensions` (Edge).
3. Enable **Developer Mode** (toggle in the top-right corner).
4. Click **Load Unpacked**.
5. Select the `CodeforcesSync` project folder.
6. **Pin the extension**: Click the puzzle icon 🧩 in the toolbar and click the pin icon next to CodeforcesSync.

 Step 4: Configure Extension Options
1. Click the **CodeforcesSync** icon in your browser toolbar.
2. Click the **Settings** ⚙️ icon.
3. Fill in the following accurately:

| Option | What to enter |
|---|---|
| **Codeforces Handle** | Your exact CF username (e.g., `tourist`). |
| **GitHub Username** | Your GitHub handle (e.g., `parthopaul69`). |
| **Repository Name** | The name you chose in Step 1 (e.g., `Codeforces`). **Do not enter the full URL.** |
| **Personal Access Token** | The `ghp_...` token you copied in Step 2. |

4. Click **Save & Test Connection**.
5. You should see a success notification: ✅ `Configuration saved and verified!`.

 Step 5: Test the Sync
Go to any Codeforces problem and submit a solution. Once the verdict changes to **Accepted**, your code will appear on GitHub within ~10 seconds.

---

 🤝 Credit

**Created & Maintained by:**
- [parthopaul69](https://github.com/parthopaul69)

---

 📄 License

Copyright (c) 2026 Partho. All rights reserved.

<p align="center">Made for competitive programmers🐸</p>
