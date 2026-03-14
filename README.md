# WNDRbox Website

> *"Not just a business starter kit. An opportunity."*

Official website for **WNDRbox** — an entrepreneurship starter kit that empowers underprivileged youth to build real businesses.

Created by Pranav K, Tejas J, Adhiyan B · Mountain House High School · 2025

---

## Project Structure

```
wndrbox/
├── index.html          ← Main page (all sections)
├── css/
│   └── style.css       ← All styles
├── js/
│   └── main.js         ← Cursor, splash, scroll, forms, buttons
├── netlify.toml        ← Netlify deployment config
├── vercel.json         ← Vercel deployment config
├── .gitignore
└── README.md
```

---

## Deploy to Netlify (Recommended — Free)

### Option A: Drag & Drop (Fastest)
1. Go to [app.netlify.com](https://app.netlify.com)
2. Sign up / log in
3. Drag the entire `wndrbox/` folder onto the Netlify dashboard
4. Done — you'll get a live URL instantly

### Option B: GitHub + Netlify (Best for ongoing updates)
1. **Push to GitHub** (see below)
2. Go to [app.netlify.com](https://app.netlify.com) → **Add new site** → **Import from Git**
3. Connect GitHub and select the `wndrbox` repo
4. Build settings — leave blank (no build command needed)
5. Click **Deploy site**
6. Every push to `main` will auto-redeploy

### Enable Netlify Forms (Contact Form)
The contact form uses Netlify's built-in form handling — zero setup needed.
When deployed to Netlify, submissions appear under **Site → Forms** in the dashboard.
You can set up email notifications there.

---

## Deploy to Vercel (Alternative — Also Free)

### Option A: Vercel CLI
```bash
npm install -g vercel
cd wndrbox
vercel
```
Follow the prompts — it auto-detects static HTML.

### Option B: GitHub + Vercel
1. Push to GitHub (see below)
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import the repo — framework preset: **Other**
4. Click **Deploy**

> **Note:** Vercel doesn't handle form submissions natively.
> For contact form on Vercel, replace the `<form>` action with [Formspree](https://formspree.io):
> ```html
> <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
> ```

---

## Push to GitHub

```bash
# 1. Initialize git repo inside the wndrbox folder
cd wndrbox
git init
git add .
git commit -m "Initial commit — WNDRbox website"

# 2. Create a new repo on github.com (call it "wndrbox")
#    Then connect it:
git remote add origin https://github.com/YOUR_USERNAME/wndrbox.git
git branch -M main
git push -u origin main
```

---

## Local Preview

No build tools needed. Open `index.html` directly in your browser, or run a simple server:

```bash
# Python (usually pre-installed)
cd wndrbox
python3 -m http.server 3000
# Then open http://localhost:3000
```

---

## Customizing the Contact Form

### For Netlify (no code changes needed)
Form data is collected automatically. Go to **Netlify → Your Site → Forms** to view submissions and set up email alerts.

### For Formspree (works on any host)
1. Sign up at [formspree.io](https://formspree.io) and create a form
2. In `index.html`, find the `<form>` tag and update:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```
3. Remove the `netlify` and `netlify-honeypot` attributes

---

## Features

- **Golden Ticket splash screen** — scroll or click to reveal the site
- **Smooth scroll navigation** — all nav links scroll to correct sections
- **Box buttons auto-select** — clicking "Get Core/Fuse/Apex Box" pre-fills the contact form dropdown and scrolls to it
- **Form validation** — client-side checks for required fields and valid email
- **Scroll reveal animations** — sections fade in as you scroll
- **Custom cursor** — amber dot + ring that expands on hover
- **Nav shrinks on scroll** — subtle padding reduction
- **Fully responsive** — works on mobile, tablet, desktop
- **Netlify Forms ready** — just deploy and collect submissions
