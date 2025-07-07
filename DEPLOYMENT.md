# Deployment Guide for Render

## Steps to Deploy on Render:

1. **Go to [Render Dashboard](https://dashboard.render.com/)**
2. **Click "New +" and select "Static Site"**
3. **Connect your GitHub repository:**
   - Choose "Connect a repository"
   - Select your `clat` repository
   - Authorize Render to access your GitHub account

4. **Configure the deployment:**
   - **Name:** clat-react-app (or any name you prefer)
   - **Build Command:** `npm install && npm run build`
   - **Publish Directory:** `build`
   - **Environment:** Static Site

5. **Click "Create Static Site"**

## What happens next:
- Render will automatically build your React app
- It will run `npm install` to install dependencies
- Then run `npm run build` to create the production build
- Finally, it will serve the contents of the `build` folder

## Automatic Deployments:
- Every time you push to the `main` branch, Render will automatically redeploy
- You can also manually trigger deployments from the Render dashboard

## Your app will be available at:
- `https://your-app-name.onrender.com` (Render will provide the exact URL)

## Troubleshooting:
- If build fails, check the build logs in Render dashboard
- Make sure all dependencies are in `package.json`
- Ensure your React app builds successfully locally with `npm run build` 