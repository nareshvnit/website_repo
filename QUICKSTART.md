# Quick Start Guide

Get your personal website up and running in 5 minutes!

## Step 1: Create GitHub Repository (2 min)

1. Go to https://github.com/new
2. Repository name: `yourusername.github.io` (replace with YOUR GitHub username)
3. Make it Public
4. Click "Create repository"

## Step 2: Upload Files (2 min)

1. Download this entire folder
2. Open terminal/command prompt in the folder
3. Run these commands (replace `yourusername` with yours):

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

## Step 3: Enable GitHub Pages (1 min)

1. Go to your repository on GitHub
2. Click "Settings" → "Pages"
3. Under "Source", select "GitHub Actions"
4. Done! Your site will be live in 2-3 minutes

## Step 4: Customize

Edit `hugo.toml` and replace:
- `yourusername` with your GitHub username
- `Your Name` with your actual name
- Email, LinkedIn, etc.

Push changes:
```bash
git add hugo.toml
git commit -m "Personalize site"
git push
```

## Your Site is Ready! 🎉

Visit: `https://yourusername.github.io`

### Edit Content:
- Web interface: Visit `https://yourusername.github.io/admin/`
- Or edit files in `content/` folder directly

### Write Blog Posts:
1. Go to `/admin/`
2. Click "Blog Posts" → "New Blog Posts"
3. Write and publish!

## Need Help?

Check the full README.md for detailed instructions and troubleshooting.
