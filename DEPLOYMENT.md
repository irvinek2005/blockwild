# Blockwild Deployment Guide

This guide covers deploying Blockwild to various platforms.

## 🌐 GitHub Pages (Recommended)

The easiest and most straightforward option!

### Automatic Deployment

The repository includes GitHub Actions workflow that automatically deploys on every push to `main`.

1. Push your changes to the `main` branch
2. GitHub Actions automatically builds and deploys
3. Your game will be available at: `https://YOUR-USERNAME.github.io/blockwild/`

### Manual Deployment

1. Go to your repository settings
2. Navigate to **Settings → Pages**
3. Under "Build and deployment", select:
   - **Source**: GitHub Actions
   - **Branch**: main (or your preferred branch)
4. Click Save
5. Wait for the deployment to complete (check the Actions tab)

### Custom Domain

To use your own domain:

1. Create a `CNAME` file in the repository root with your domain
2. Update your domain's DNS settings to point to GitHub Pages
3. Enable HTTPS in repository Settings → Pages

---

## 🔗 Replit

Perfect for live deployment with a simple URL.

### Setup

1. Create a new Replit project
2. Upload all files from the repository
3. Create a `.replit` file with:
   ```
   run = "python -m http.server 8000"
   ```
4. Click "Run" to start the server
5. Access your game via the Replit URL
6. Open in Safari and select "Add to Home Screen" for app-like experience

### Advantages
- HTTPS enabled (required for persistent storage)
- Live updates (just upload new files)
- Easy file management
- Always online

---

## 🎮 itch.io

Publish to the indie game community!

### Setup

1. Create an [itch.io](https://itch.io) account
2. Go to "Create new project"
3. Upload all files as a ZIP
4. Set the following:
   - **Kind of project**: HTML
   - **Viewport dimensions**: 1280x720 (or responsive)
   - **Enable fullscreen**: Yes
   - **Description**: Add features from FEATURES.md

### Sharing
- Your game gets a unique itch.io URL
- Embed it on your website
- Share with the gaming community
- Track downloads and plays

---

## 🖥️ Self-Hosted

Run on your own server.

### Requirements
- Web server (Apache, Nginx, Node.js, etc.)
- HTTPS certificate (required for persistent storage)
- Support for static file serving

### Setup

1. Upload all files to your server
2. Configure web server to serve index.html as default
3. Ensure HTTPS is enabled
4. Access your game at your domain

### Example (Node.js)
```bash
npm install -g http-server
http-server .
```

Then access at `https://your-domain.com`

---

## 📋 Checklist Before Publishing

- [ ] Tested on Chrome, Firefox, Safari
- [ ] Tested on iOS Safari (desktop + home screen)
- [ ] Tested on Android Chrome
- [ ] Game saves and loads correctly
- [ ] Service worker works offline
- [ ] No console errors
- [ ] README is up-to-date
- [ ] LICENSE file included
- [ ] Manifest looks correct

---

## 🚀 Going Live

### Recommended Flow

1. **Local Testing** - Test everything locally
2. **GitHub Staging** - Push to a test branch, deploy to test URL
3. **Final Testing** - Test deployed version thoroughly
4. **Production** - Merge to main and deploy
5. **Promote** - Share your itch.io page and GitHub Pages link

### Monitoring

After deployment:
- Check browser console for errors
- Test save/load functionality
- Verify offline play works
- Monitor itch.io stats (if published)

---

## 🆘 Troubleshooting

### Game won't load
- Check browser console (F12) for errors
- Ensure HTTPS is enabled
- Verify all files were uploaded correctly
- Check Three.js CDN is accessible

### Save data not persisting
- Ensure you're using HTTPS
- Check browser localStorage isn't disabled
- Verify service worker is registered
- Clear browser cache and try again

### Performance issues
- Reduce render distance in code
- Check GPU usage in DevTools
- Close other tabs
- Try a different browser

### Mobile issues
- Use Safari on iOS for best experience
- Rotate to landscape
- Disable Safari's reader mode
- Check iOS storage isn't full

---

## 📚 Resources

- [GitHub Pages Docs](https://docs.github.com/en/pages)
- [Replit Hosting](https://replit.com/talk/learn/Hosting-web-pages-on-Replit/5826)
- [itch.io Publishing](https://itch.io/docs/creators)
- [Three.js Documentation](https://threejs.org/docs)
