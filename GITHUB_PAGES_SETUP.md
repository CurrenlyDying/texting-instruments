# GitHub Pages Deployment Guide

## Configuring GitHub Pages for Criminal Web Services

To activate the GitHub Pages website for the Criminal Web Services documentation repository, follow these steps:

### Step 1: Access Repository Settings

1. Navigate to the repository at `https://github.com/CurrenlyDying/texting-instruments`
2. Click on the **Settings** tab (requires repository admin access)

### Step 2: Configure Pages Settings

1. In the left sidebar, scroll down to the **Code and automation** section
2. Click on **Pages**

### Step 3: Set Source Configuration

Configure the following settings:

- **Source**: Deploy from a branch
- **Branch**: Select `main` (or whichever is your default branch)
- **Folder**: Select `/docs`
- Click **Save**

### Step 4: Wait for Deployment

GitHub will automatically build and deploy your site. This typically takes 1-3 minutes. You can monitor the deployment progress by:

1. Going to the **Actions** tab in your repository
2. Looking for the "pages build and deployment" workflow
3. Waiting for the green checkmark indicating successful deployment

### Step 5: Access Your Site

Once deployed, your site will be available at:
- **Default URL**: `https://currentlydying.github.io/texting-instruments/`

### Optional: Configure Custom Domain

To use the custom domain `www.criminalwebservices.com`:

1. In the Pages settings, under "Custom domain", enter: `www.criminalwebservices.com`
2. Click **Save**
3. Configure DNS settings with your domain registrar:
   - Add a CNAME record pointing `www` to `currentlydying.github.io`
   - Alternatively, for apex domain, add A records to GitHub's IP addresses
4. Wait for DNS propagation (can take up to 48 hours)
5. Enable **Enforce HTTPS** once DNS is configured

### Verification

To verify your deployment:

1. Visit your GitHub Pages URL
2. Confirm all pages load correctly:
   - Home page (index.html)
   - Directives page (directives.html)
   - Resources page (resources.html)
   - Publications page (publications.html)
3. Check that PDF downloads work from the resources page
4. Verify navigation links function properly

### Troubleshooting

If the site doesn't deploy:

1. Check the Actions tab for build errors
2. Ensure the `docs/` folder exists in the selected branch
3. Verify `_config.yml` has correct baseurl: `/texting-instruments`
4. Check that all HTML files are valid

### Future Updates

To update the website:

1. Edit files in the `docs/` directory
2. Commit and push changes to the main branch
3. GitHub Pages will automatically rebuild and deploy within minutes
4. No manual intervention required after initial setup

---

**Note**: The website is designed to be framework-agnostic and will work with or without Jekyll processing. All pages are static HTML and will display correctly regardless of GitHub's build process.
