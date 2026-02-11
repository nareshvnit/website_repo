# Personal Website

A clean, minimal personal website built with 100% open source tools.

## Tech Stack

- **Static Site Generator**: [Hugo](https://gohugo.io/) - Fast, flexible static site generator
- **CMS**: [Decap CMS](https://decapcms.org/) - Open source content management (formerly Netlify CMS)
- **Hosting**: [GitHub Pages](https://pages.github.com/) - Free, reliable hosting
- **Deployment**: GitHub Actions - Automated CI/CD

## Features

- ✅ Personal homepage with introduction
- ✅ About page (editable)
- ✅ Work experience page (editable)
- ✅ Blog with weekly technical posts
- ✅ Responsive design
- ✅ Clean, minimal UI
- ✅ Easy content editing through CMS
- ✅ Automatic deployment

## Setup Instructions

### 1. Prerequisites

- Git installed on your computer
- A GitHub account
- Hugo installed (optional for local development)

### 2. Initial Setup

1. **Create a GitHub repository**
   - Go to GitHub and create a new repository named `yourusername.github.io`
   - Replace `yourusername` with your actual GitHub username

2. **Clone this project and push to your repository**
   ```bash
   git clone <this-repo>
   cd personal-website
   git remote set-url origin https://github.com/yourusername/yourusername.github.io.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository settings
   - Navigate to Pages (in the left sidebar)
   - Under "Source", select "GitHub Actions"
   - The site will deploy automatically

### 3. Configure Your Site

Edit `hugo.toml` to customize:

```toml
baseURL = 'https://yourusername.github.io/'
title = 'Your Name - Personal Website'

[params]
  description = 'Your tagline'
  author = 'Your Name'
  email = 'your.email@example.com'
  github = 'yourusername'
  linkedin = 'yourprofile'
```

### 4. Enable the CMS (Content Management System)

To edit content through a web interface:

1. **Enable GitHub Identity on your repository**
   - Go to your repository settings
   - Navigate to "Pages" 
   - Your site will be at `https://yourusername.github.io`

2. **Set up Decap CMS Authentication**
   
   Option A: Use Decap CMS with GitHub (Recommended)
   - Go to `https://yourusername.github.io/admin/`
   - Click "Login with GitHub"
   - Authorize the application
   - You can now edit content!

   Option B: Alternative - Direct File Editing
   - Edit markdown files directly in the `content/` folder
   - Commit and push changes
   - Site rebuilds automatically

### 5. Local Development (Optional)

If you want to preview changes locally before pushing:

1. **Install Hugo**
   ```bash
   # macOS
   brew install hugo
   
   # Linux
   sudo apt-get install hugo
   
   # Windows
   choco install hugo-extended
   ```

2. **Run local server**
   ```bash
   hugo server -D
   ```
   Visit `http://localhost:1313`

## Editing Content

### Through the CMS (Easy Way)

1. Visit `https://yourusername.github.io/admin/`
2. Log in with GitHub
3. Edit pages or create new blog posts
4. Click "Publish" - changes go live automatically!

### Directly (Advanced Way)

Edit markdown files in the `content/` folder:
- `content/_index.md` - Home page
- `content/about/_index.md` - About page
- `content/experience/_index.md` - Experience page
- `content/posts/` - Blog posts

Commit and push changes:
```bash
git add .
git commit -m "Update content"
git push
```

## Creating New Blog Posts

### Via CMS
1. Go to `/admin/`
2. Click "Blog Posts"
3. Click "New Blog Posts"
4. Write your post in markdown
5. Click "Publish"

### Via Files
Create a new file in `content/posts/`:

```bash
hugo new posts/2024-02-15-my-new-post.md
```

Edit the file:
```markdown
---
title: "My New Technical Post"
date: 2024-02-15T10:00:00Z
draft: false
---

Your content here...
```

## Customization

### Changing Colors

Edit `themes/personal/static/css/style.css`:

```css
:root {
    --primary-color: #2563eb;  /* Change this */
    --text-color: #1f2937;
    --bg-color: #ffffff;
}
```

### Adding New Pages

1. Create a new folder in `content/`
2. Add an `_index.md` file
3. Add to navigation in `hugo.toml`:

```toml
[[menu.main]]
  name = 'New Page'
  url = '/newpage/'
  weight = 4
```

## Deployment

Every push to the `main` branch automatically:
1. Builds your Hugo site
2. Deploys to GitHub Pages
3. Makes it live at `yourusername.github.io`

Check deployment status in the "Actions" tab of your repository.

## Troubleshooting

**Site not updating?**
- Check the Actions tab for build errors
- Ensure GitHub Pages is enabled in settings
- Wait a few minutes for changes to propagate

**CMS not working?**
- Make sure you're accessing `/admin/` with the trailing slash
- Check that you're logged into GitHub
- Clear browser cache

**Build failing?**
- Check Hugo version in `.github/workflows/hugo.yml`
- Validate your markdown syntax
- Check for missing front matter in posts

## Support

- Hugo Documentation: https://gohugo.io/documentation/
- Decap CMS Docs: https://decapcms.org/docs/
- GitHub Pages Docs: https://docs.github.com/en/pages

## License

This template is open source and free to use.

## Next Steps

1. Customize your information in `hugo.toml`
2. Edit the About and Experience pages
3. Write your first blog post
4. Share your site!

Happy blogging! 🚀
