# 🚀 Automation Blog

![Website](https://img.shields.io/badge/Live-Online-green)
![Cloudflare Pages](https://img.shields.io/badge/Host-Cloudflare-blue)
![License](https://img.shields.io/badge/License-Free-lightgrey)
![GitHub](https://img.shields.io/badge/Repo-GitHub-black)

---

## Quick Start ⚡
Clone the repository and open it locally:

```bash
git clone <your-repo-url>
cd <your-repo-folder>
```

(Optional) Install dependencies and run a local server:

```bash
# Example for static site generators
npm install
npm run dev
```

Open your browser at `http://localhost:3000` (or the specified port).  

---

## Overview 📝
Automation Blog is a personal project by **Md. Rezaul Hasan (Reza / MRH Reza)** that shares tutorials, tips, and insights on automation, productivity, and technology.  
The site is hosted on **Cloudflare Pages** and supports a **custom domain**.

---

## 🌐 Live Site
- Temporary URL (Cloudflare Pages): [https://automationblog.pages.dev](https://automationblog.pages.dev)  
- Custom Domain: [https://blog.989247.xyz](https://blog.989247.xyz)

---

## Features ✨
- Fully static site for fast loading  
- Automatic HTTPS via Cloudflare  
- Easy deployment via GitHub & Cloudflare Pages  
- Clean, structured project setup  

---

## Deployment Instructions 🛠️

### 1. Local Development (Optional)
```bash
git clone <your-repo-url>
cd <your-repo-folder>
npm install
npm run dev
```
Open `http://localhost:3000` in your browser.

### 2. Cloudflare Pages Deployment
1. Push changes to the **main branch**.  
2. Cloudflare Pages builds & deploys automatically.  
3. Add `blog.989247.xyz` as a **custom domain** in Cloudflare Pages.  
4. Ensure DNS points correctly:

```text
Type: CNAME
Name: blog
Target: automationblog.pages.dev
Proxy: DNS only
```

---

## Notes ⚠️
- SSL certificates are managed automatically by Cloudflare Pages.  
- Avoid conflicting A records for `blog.989247.xyz`.  
- This README serves as a quick reference for future updates.

---

## Project Structure 📁
```
/blog-site
│
├─ index.html       # Main homepage
├─ assets/          # CSS, JS, images
├─ _posts/          # Blog content (if using static site generator)
└─ README.md        # Project documentation
```

---

## Tools & Platforms 🛠️
- Cloudflare Pages  
- GitHub  
- Markdown for documentation  

---

## Author / Affiliation 👤
**Md. Rezaul Hasan (Reza / MRH Reza)**  
Community pharmacist, tech enthusiast, and content creator  

---

## Tips & Tricks 💡

### Force redeploy on Cloudflare Pages
```bash
git commit --allow-empty -m "Trigger redeploy"
git push origin main
```

### Check DNS propagation quickly
```bash
nslookup blog.989247.xyz
```
- Should return `automationblog.pages.dev`.

### Flush local DNS cache
- Windows: `ipconfig /flushdns`  
- Mac: `sudo dscacheutil -flushcache`

### Preview changes locally
```bash
npm run dev
```
- Open `http://localhost:3000` to see changes instantly.

### SSL issues
- Cloudflare Pages manages SSL automatically.  
- If HTTPS fails after DNS update, wait **5–10 minutes** for SSL provisioning.  

### Avoid conflicts
- Do not create an A record for `blog.989247.xyz`—only use the CNAME pointing to `automationblog.pages.dev`.  
- Keep other records (MX, main domain, subdomains) unchanged.  

### Quick GitHub commit & push
```bash
git add .
git commit -m "Update site / blog content"
git push origin main
