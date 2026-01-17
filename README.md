# Dubblelab Film Sort Game - Deployment Guide

## Files in this package:
- `index.html` - The game (your film-sort-v12-mobile-optimized.html renamed)
- `package.json` - Tells Railway how to serve the files
- `railway.json` - Railway deployment configuration

## Step-by-Step Deployment Instructions:

### 1. CREATE GITHUB REPOSITORY
1. Go to https://github.com
2. Click the "+" button (top right) → "New repository"
3. Repository name: `dubblelab-film-game` (or whatever you want)
4. Set to: **Public**
5. DO NOT check "Add a README file"
6. Click "Create repository"

### 2. UPLOAD FILES TO GITHUB
You'll see an empty repository. Choose "uploading an existing file":

1. Click "uploading an existing file" link
2. Drag and drop ALL THREE files:
   - index.html
   - package.json
   - railway.json
3. Add commit message: "Initial game deployment"
4. Click "Commit changes"

### 3. DEPLOY TO RAILWAY
1. Go to https://railway.app
2. Click "New Project"
3. Click "Deploy from GitHub repo"
4. Select your `dubblelab-film-game` repository
5. Railway will automatically start deploying
6. Wait for deployment to complete (~2 minutes)

### 4. GENERATE DOMAIN
1. In Railway, click on your service
2. Go to "Settings" tab
3. Scroll to "Networking" section
4. Click "Generate Domain"
5. Railway will give you a URL like: `something.up.railway.app`
6. Test it to make sure the game loads!

### 5. SET UP CUSTOM DOMAIN (Optional)
If you want to use your own domain (like game.dubblelab.com):

**In Railway:**
1. Settings → Networking → "Custom Domain"
2. Enter your domain (e.g., `game.dubblelab.com`)
3. Select port 8080
4. Railway will show you the DNS record needed

**In Porkbun (or your DNS provider):**
1. Add a CNAME record:
   - Type: CNAME
   - Name: game (or whatever subdomain you want)
   - Value: [the Railway URL they give you]
   - TTL: 600
2. Save the record
3. Wait 5-15 minutes for DNS to propagate
4. Your game will be live at your custom domain!

## Troubleshooting:
- If you see "Index of app/" → The files weren't uploaded correctly. Make sure index.html is in the root.
- If Railway says "No start command" → Make sure both package.json and railway.json are uploaded
- If custom domain doesn't work → Check DNS is pointing to the correct Railway URL

## Need help?
Ask Claude for assistance!
