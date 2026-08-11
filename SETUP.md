# 🚀 Setup — Reel-Style GitHub Profile README (Windows)

Everything you need to put this profile live on
**https://github.com/Yogesh2201** in ~5 minutes.

---

## 1. Create the special repository (once)

A GitHub *profile* README lives in a repository whose name **exactly
matches your username**.

1. Go to https://github.com/new
2. **Repository name:** `Yogesh2201`
3. Visibility: **Public**
4. Tick **"Add a README file"** ✔
5. Click **Create repository**

GitHub now knows this is your profile repo. 🎉

---

## 2. Copy this package into the repo

### Option A — quickest (no git on the command line)

1. Download this folder (README.md, `assets/`, `.github/`).
2. On github.com, open your `Yogesh2201` repository → **Add file →
   Upload files**.
3. Drag & drop `README.md` and the `assets/` and `.github/` folders.
   (Drag the *folders* too — GitHub keeps the structure.)
4. Commit directly to `main`.

### Option B — with Git for Windows (recommended)

Open **Command Prompt** (Win+R → `cmd`) and run:

```bat
cd %USERPROFILE%\Desktop
git clone https://github.com/Yogesh2201/Yogesh2201.git
cd Yogesh2201
```

Then copy this package's files into that folder so you have:

```text
Yogesh2201\
├── README.md
├── assets\
│   ├── profile-scan.svg
│   └── github-snake-placeholder.svg
└── .github\
    └── workflows\
        ├── update-profile.yml
        └── snake.yml
```

Then push:

```bat
git add .
git commit -m "feat: add reel-style profile README"
git push origin main
```

> If your default branch is `master` instead of `main`, use:
> `git branch -M main` before pushing.

---

## 3. Verify

Open **https://github.com/Yogesh2201** in your browser.

You should see:

- 🖥️ The green terminal "Profile Scan" card (it has a moving scan line)
- 👨‍💻 The typing header animation
- 📊 Stats cards, top languages, streak & contribution graph
- 🧠 Learning, 🛠️ Tech stack, 🚀 Projects, 📬 Connect sections

> ⏳ The stat cards / graph load from external services — give them a
> few seconds. If they show nothing, hard-refresh (Ctrl+F5).

---

## 4. Make it yours (search for `TODO` in README.md)

| What                         | Where to change it |
| ---------------------------- | ------------------ |
| LinkedIn link                | `Connect With Me` section |
| Email address                | `Connect With Me` section |
| Kaggle link                  | `Connect With Me` section |
| Project repo links           | `Featured Projects` section |
| Tagline / skills             | Header + `About Me` |
| Tech icons                   | `Tech Stack` → change the `i=` list |

Edit the file directly on github.com (pencil icon) or locally and push.

---

## 5. Run the automations (one-time)

The workflows need one manual kick to generate their artwork:

1. Open the repo → **Actions** tab.
2. Click **Generate Snake** → **Run workflow** → **Run workflow**.
   → Creates `assets/github-snake.svg` (your contribution snake).
3. Click **Update Profile Metrics** → **Run workflow**.
   → Creates `assets/github-metrics.svg` (optional extra stats card).

After that, both run automatically **every day at 00:00 UTC**.

If you don't see the Actions tab: it's hidden while the repo has no
workflows yet — it appears after you push the `.github/workflows/`
folder (Step 2). If Actions are disabled for the account, enable them
under **Settings → Actions → General**.

---

## 6. Troubleshooting

| Problem | Fix |
| ------- | --- |
| Stat cards show nothing | The github-readme-stats service can return `503` when rate-limited — refresh in a minute. If it persists, that service is temporarily down (it affects everyone). |
| Snake image is a placeholder | Run the *Generate Snake* workflow (Step 5). |
| Icons missing | `skillicons.dev` occasionally adds/removes icons — check the names in the `i=` list. |
| Typing animation blank | The `readme-typing-svg.demolab.com` service is slow to start — refresh. |
| Wrong branch on push | `git branch -M main` then push again. |
| I want richer stats | Create a Personal Access Token (Settings → Developer settings → PAT, scopes `repo` + `read:user`), add it as a secret named `METRICS_TOKEN`, and change `token:` in `update-profile.yml`. |

---

## 7. Tips

- Star your own profile repo? No need — but do keep it **Public**,
  otherwise the README won't show.
- Pin your best 6 repositories under the profile header for extra impact.
- Update the ASCII art inside `assets/profile-scan.svg` (any text
  editor) to personalise the terminal card.
- The whole design works on mobile too — GitHub reflows the tables.

Happy hacking! 💚
