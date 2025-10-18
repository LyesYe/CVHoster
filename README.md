# Lyes Khoumeri - Resume Website

A simple static website that displays Lyes Khoumeri's resume PDF.

## Local Development

To run the website locally:

```bash
npm install
npm run dev
```

The website will be available at `http://localhost:3000`

## Deployment to Vercel

### Step 1: Push to GitHub

1. Initialize a Git repository in this folder:
   ```bash
   git init
   ```

2. Add all files to Git:
   ```bash
   git add .
   ```

3. Commit the files:
   ```bash
   git commit -m "Initial commit: Resume website"
   ```

4. Create a new repository on GitHub (https://github.com/new)
   - Repository name: `resume-website` (or any name you prefer)
   - Make it public or private (your choice)
   - Don't initialize with README, .gitignore, or license (since we already have files)

5. Add the GitHub repository as remote and push:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
   git branch -M main
   git push -u origin main
   ```

### Step 2: Deploy to Vercel

1. Go to [Vercel](https://vercel.com) and sign up/login with your GitHub account

2. Click "New Project" or "Import Project"

3. Select "Import Git Repository" and choose your resume website repository

4. Configure the project:
   - **Project Name**: `resume-website` (or your preferred name)
   - **Framework Preset**: Other (or leave as detected)
   - **Root Directory**: `./` (leave as default)
   - **Build Command**: Leave empty (static site, no build needed)
   - **Output Directory**: Leave empty
   - **Install Command**: `npm install` (should be auto-detected)

5. Click "Deploy"

6. Vercel will automatically deploy your website and provide you with a URL like:
   `https://your-project-name.vercel.app`

### Step 3: Custom Domain (Optional)

If you want to use a custom domain:

1. Go to your project dashboard on Vercel
2. Click on "Settings" → "Domains"
3. Add your custom domain
4. Follow Vercel's instructions to configure DNS

## Files Structure

```
├── index.html          # Main HTML file that displays the PDF
├── CV GRAPHICS LATEX LYES.pdf  # Your resume PDF
├── package.json        # Node.js configuration for deployment
├── vercel.json         # Vercel-specific configuration
└── README.md          # This file
```

## Features

- ✅ Responsive design that works on desktop and mobile
- ✅ Direct PDF embedding in the browser
- ✅ Fallback download option for browsers that don't support PDF embedding
- ✅ Optimized for Vercel deployment
- ✅ Proper MIME type handling for PDF files
- ✅ Security headers configured

## Updating Your Resume

To update your resume:

1. Replace the `CV GRAPHICS LATEX LYES.pdf` file with your new resume
2. Commit and push the changes to GitHub:
   ```bash
   git add .
   git commit -m "Update resume"
   git push
   ```
3. Vercel will automatically redeploy your website with the new resume

## Troubleshooting

- **PDF not displaying**: Some browsers have restrictions on PDF embedding. The website includes a fallback that shows a download link.
- **Deployment issues**: Make sure all files are committed to Git and pushed to GitHub before deploying to Vercel.
- **Custom domain not working**: Check your DNS settings and wait for propagation (can take up to 24 hours).