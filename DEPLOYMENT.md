# Makamithi Website Deployment Guide

## Deploy to Vercel

### Method 1: GitHub + Vercel (Easiest)

1. **Push your code to GitHub:**
   ```bash
   git add .
   git commit -m "Ready for deployment"
   git push origin main
   ```

2. **Deploy via Vercel Dashboard:**
   - Go to [vercel.com](https://vercel.com)
   - Click "Add New Project"
   - Import your GitHub repository `ProSteveMchuma/makamithi`
   - Vercel will auto-detect it as a static site
   - Click "Deploy"
   - Your site will be live at `https://makamithi.vercel.app`

### Method 2: Vercel CLI

1. **Install Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel:**
   ```bash
   vercel login
   ```

3. **Deploy:**
   ```bash
   cd /workspaces/makamithi
   vercel
   ```

4. **Follow the prompts:**
   - Set up and deploy? `Y`
   - Which scope? (Select your account)
   - Link to existing project? `N`
   - Project name? `makamithi`
   - In which directory is your code located? `./`
   - Deploy? `Y`

5. **For production deployment:**
   ```bash
   vercel --prod
   ```

### Method 3: Vercel Drag & Drop

1. Go to [vercel.com/new](https://vercel.com/new)
2. Drag and drop your entire `makamithi` folder
3. Vercel will automatically deploy

## Custom Domain

After deployment, you can add your custom domain:
1. Go to your project settings on Vercel
2. Click "Domains"
3. Add `makamithi.inspirehub.co.ke`
4. Follow DNS configuration instructions

## Project Structure

Your site is already configured:
- ✅ Single `index.html` file
- ✅ All assets in `/assets` folder
- ✅ No build process needed
- ✅ `vercel.json` configuration file created

## Environment

The site uses:
- Pure HTML/CSS/JavaScript (no build required)
- External CDN resources (Font Awesome, Google Fonts)
- Static asset hosting

## Next Steps

1. Commit and push to GitHub
2. Connect repository to Vercel
3. Automatic deployments on every push to `main`
