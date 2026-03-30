# Fix: Push to GitHub

## The Problem
Netlify says "missing git branch" because the GitHub repo is empty.

## Solution: Push Your Code

### Option 1: Command Line (Recommended)

Run these commands in your terminal:

```bash
cd /path/to/webapp

# Add the GitHub remote
git remote add origin https://github.com/janeivind/snoopy.git

# Rename branch to 'main' (GitHub standard)
git branch -M main

# Push to GitHub
# You'll be asked to authenticate
git push -u origin main
```

When prompted, use your GitHub credentials or personal access token.

---

### Option 2: Upload Files Directly (Easier)

1. Go to https://github.com/janeivind/snoopy
2. Click "uploading an existing file" link
3. Drag and drop these files from `webapp/` folder:
   - `index.html`
   - `README.md`
4. Commit with message: "Initial commit"
5. Go back to Netlify, it should auto-detect

---

### Option 3: Drag & Drop to Netlify (Skip GitHub)

1. Go to https://app.netlify.com
2. Find your site
3. Go to "Deploys" tab
4. Drag the `webapp/` folder directly onto the deploy area
5. No GitHub needed!

---

## After Push

Once files are on GitHub:
1. Netlify will auto-detect them
2. Click "Retry deploy" in Netlify
3. Your site will be live!

---

## Quick Check

To verify your local repo:
```bash
cd webapp
git log --oneline
# Should show:
# c3942ec Add README with deployment instructions
# 23be9b5 Initial commit: Simple collaboration page
```

---

*Need help? Try Option 2 (upload directly to GitHub) - it's the easiest.*
