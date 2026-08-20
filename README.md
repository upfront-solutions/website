# Upfront Solutions Website

Static website ready for free hosting on Vercel via GitHub. No build step, no dependencies.

## Files

- `index.html` - Home page with contact form
- `services.html` - Services and pricing
- `case-studies.html` - Case studies (placeholders ready for your screenshots)
- `free-audit.html` - Free audit request form
- `terms.html` - Terms and privacy (paste your existing policy text in before launch)
- `styles.css` - All styling (brand colors: navy #151C34, gold #EFBD41, cream #F7F2EF, font Figtree)

## Launch checklist

### 1. Formspree (done)

Both forms are live: Contact Us uses form `xykrvowq` (index.html), Free Audit uses form `mojgbrwq` (free-audit.html). Submissions arrive by email and include the lead's email address, so you can add each one to Instantly as a contact.

### 2. Save your logo files locally (2 min, important)

The site currently loads your logo from Webflow's CDN. Before you cancel Webflow, save local copies:

1. The `assets` folder already exists (it holds your case study images)
2. Download these two images (open each URL, right-click, Save Image As):
   - Logo: https://cdn.prod.website-files.com/65ef8e5d98ceea40872999fa/665e4ff89b907810824c2d86_Logo%20Horizontal%20copy.png (save as `assets/logo.png`)
   - Icon: https://cdn.prod.website-files.com/65ef8e5d98ceea40872999fa/66c4f976a3eae9d45327159d_Icon%20Only%20copy.png (save as `assets/icon.png`)
3. In all 5 HTML files, replace the two CDN URLs with `assets/logo.png` and `assets/icon.png`

(Ask Claude to do step 3 for you once the files are saved.)

### 3. Push to GitHub (5 min)

1. Go to github.com, click + then "New repository", name it `upfront-website`, keep it private, create
2. Click "uploading an existing file" and drag all files from this folder in
3. Commit

### 4. Deploy on Vercel (5 min)

1. Go to vercel.com and sign up with your GitHub account (free Hobby plan)
2. Click "Add New" then "Project", import `upfront-website`
3. No settings needed, click Deploy
4. Your site is live at `upfront-website.vercel.app` (or similar)

Every time you push a change to GitHub, Vercel redeploys automatically.

### 5. Move your domain (when ready)

1. In Vercel: Project Settings, Domains, add `upfront-solutions.com` and `www.upfront-solutions.com`
2. At your domain registrar, update DNS as Vercel instructs:
   - A record for `upfront-solutions.com` pointing to `76.76.21.21`
   - CNAME record for `www` pointing to `cname.vercel-dns.com`
3. Wait for DNS to propagate (minutes to a few hours), Vercel adds free HTTPS automatically
4. Once confirmed working, cancel Webflow

### 6. Before launch

- Paste your Terms and Privacy text into `terms.html`
- Case studies are done (anonymized results with screenshots in `assets/`)
