# Hot Beans Web Development Company

A complete, professional website for a fictional web development company with automated deployment and testing.

Assignment 2: Level 3 Computing - CI/CD Website Deployment -please bear in mind if using this template website you will be expected to customise it! Comments in the code will be expected as will screen shots of the code and the completed website running in 2 browsers  - this is part of testing too - you can also use a platform like Figma (industry standard tool) to develop the wireframes and more :) 

---

## Getting Started

### Run Locally

1. Clone this repository
2. Open `index.html` in your web browser

No build steps or dependencies required.

### Staff Portal Demo

| Field    | Value                 |
| -------- | --------------------- |
| Email    | staff@hotbeansweb.com |
| Password | hotbeans2024          |

**Access URLs:**

- Login page: `staff-login.html`
- Dashboard: `staff-dashboard.html`

---

## Project Structure

```
hot-beans-web/
│
├── index.html              # Homepage
├── about.html              # Company information
├── services.html           # Services offered
├── trainees.html           # Current trainees
├── jobs.html               # Open positions
├── apply.html              # Job application form
├── staff-login.html        # Staff portal login
├── staff-dashboard.html    # Staff management area
│
├── style.css               # Main stylesheet
├── script.js               # JavaScript functionality
│
├── images/                 # Image assets
│
└── README.md               # Documentation
```

> Some pages may be incomplete. Feel free to add more as needed.

---

## Setup Instructions

Estimated time: 30 minutes

### Phase 1: Fork and Clone

**Step 1: Fork the Repository**

1. Go to: `https://github.com/Willxxx7/hot-beans-web`
2. Click the green "Fork" button (top-right)
3. Select your GitHub account
4. Your copy: `https://github.com/YOUR-USERNAME/hot-beans-web`

**Step 2: Install Required Software**

| Software | Download Link                 |
| -------- | ----------------------------- |
| VS Code  | https://code.visualstudio.com |
| Git      | https://git-scm.com           |

**Step 3: Configure Git**

Open VS Code terminal (`Ctrl + `` ) and run:

```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
git config --global credential.helper manager-core
```

**Step 4: Clone Your Fork**

1. VS Code: `Ctrl+Shift+P` → Type "Git: Clone"
2. Paste: `https://github.com/YOUR-USERNAME/hot-beans-web.git`
3. Choose a folder → Click "Open"

**Step 5: Test Authentication**

1. Edit `index.html` (change any text)
2. Save file (`Ctrl+S`)
3. Open Source Control (`Ctrl+Shift+G`)
4. Click `+` next to index.html
5. Type a commit message → `Ctrl+Enter`
6. Click the cloud icon (↑) to push

**What happens next:**

- **Option A (Browser popup):** Click "Sign in with GitHub" → Authorize in browser
- **Option B (Device code):** Go to github.com/login/device → Enter the code shown

Success message: "✓ Published to: main"

---

### Phase 2: Live Website

**Enable GitHub Pages**

1. Go to your repository on GitHub.com
2. Click **Settings** → **Pages** (left sidebar)
3. Source: **Branch: main** → **Folder: / (root)**
4. Click **Save**
5. Wait 2 minutes
6. Your live URL: `https://YOUR-USERNAME.github.io/hot-beans-web`

**Add Automated Tests**

1. In your repository under Actions-click new workflow (green button), click **Add file** → **Create new file**
2. Filename: `.github/workflows/test.yml`
3. Copy and paste:

```yaml
name: CI/CD Website Tests
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v4
    - name: Test HTML Valid
      run: npx @html-validate/cli@latest .
    - name: Check Image Paths
      run: grep -r 'src=' *.html | grep -v 'data:' || true
    - name: Verify Pages Build
      run: |
        if [ -f "index.html" ]; then
          echo "✅ index.html exists in root"
        else
          echo "❌ No index.html - Pages will 404"
          exit 1
        fi
```

4. Click **Commit new file**
5. Go to the **Actions** tab → Wait for green checkmarks

---

## Daily Workflow

Repeat these 5 steps every time you work:

| Step | Action              | Shortcut                            |
| ---- | ------------------- | ----------------------------------- |
| 1    | Pull latest changes | `Ctrl+Shift+G` → `...` → Pull |
| 2    | Edit your files     | Edit HTML/CSS/JS                    |
| 3    | Stage changes       | `Ctrl+Shift+G` → Click `+`     |
| 4    | Commit              | Type message →`Ctrl+Enter`       |
| 5    | Push                | Click cloud↑ arrow                 |

Your live site updates automatically after each push.

---

## Troubleshooting

| Issue                        | Solution                                         |
| ---------------------------- | ------------------------------------------------ |
| Authentication error         | Repeat the authentication step (browser popup)   |
| 404 on live site             | Check Pages settings: main branch + /root folder |
| Red X in Actions             | Fix HTML errors → Commit → Push again          |
| Broken images                | Use relative paths:`./images/filename.jpg`     |
| No Source Control in VS Code | File → Open Folder → Select your project       |
| Push rejected                | Pull latest changes first, then push             |

---

## Assessment Checklist

| Item                                     | Complete? |
| ---------------------------------------- | --------- |
| Repository forked to your account        | ☐        |
| VS Code shows all project files          | ☐        |
| Authentication working (push successful) | ☐        |
| GitHub Pages configured correctly        | ☐        |
| Actions tab shows green checkmarks       | ☐        |
| Live website loads in browser            | ☐        |

### Grading

| Result                     | Grade     |
| -------------------------- | --------- |
| All 6 items complete       | A* (100%) |
| 4-5 items complete         | B (70%)   |
| Less than 4 items complete | Fail      |

---

## Quick Reference

**Live URL:** `https://YOUR-USERNAME.github.io/hot-beans-web`

**Repository:** `https://github.com/YOUR-USERNAME/hot-beans-web`

**Test Status:** View in the Actions tab

---

## Learning Outcomes

- GitHub Pages deployment
- VS Code Git workflow
- CI/CD automated testing
- Git authentication setup
- Responsive web development
- Portfolio project creation

---

## Credits

- Template by: Willxxx7/hot-beans-web
- Assignment: Level 3 Computing - CI/CD Website Deployment -please bear in mind if using this template website you will be expected to customise it! Comments in the code will be expected as will screen shots of the code and the completed website running in 2 browsers  - this is part of testing too - you can also use a platform like Figma (industry standard tool) to develop the wireframes and more :) 

---

**Submission deadline:** 30th April 2026

**Submit:** Live URL + 6 screenshots + GitHub repo link

---

*Fork → Customize → Deploy → Shine* 🚀

---

## What to change after pasting:

| Find                        | Replace with                |
| --------------------------- | --------------------------- |
| `YOUR-USERNAME` (3 times) | Your actual GitHub username |
| `[INSERT DATE]`           | Your submission deadline    |
| `Your Name`               | Your full name              |
| `your-email@example.com`  | Your GitHub email           |
