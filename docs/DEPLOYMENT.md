# Deployment & DNS Setup

## GitHub Pages Configuration

The site is deployed via **GitHub Pages** directly from the `main` branch.

- **Repository:** https://github.com/waqarsheikh07/unlearntoreturn
- **Source branch:** `main`
- **Source path:** `/` (root)
- **HTTPS enforced:** Yes
- **CNAME file:** Contains `unlearntoreturn.com`

### How Deployment Works

1. Push changes to `main` branch
2. GitHub Pages automatically builds and deploys (~60 seconds)
3. Site is served at https://unlearntoreturn.com

### To Redeploy

```bash
cd /path/to/unlearntoreturn
git add .
git commit -m "your change description"
git push origin main
```

Wait ~60 seconds, then check the live site.

## DNS Configuration (Hostinger)

The domain `unlearntoreturn.com` is registered at **Hostinger**. DNS records point to GitHub Pages.

### Required DNS Records

| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | waqarsheikh07.github.io |

### Important Notes

- Do NOT add any other A records for `@` — remove stale ones (e.g., old Hostinger parking IPs like `2.57.91.91`)
- The CNAME for `www` must point to `waqarsheikh07.github.io` (your GitHub username, not the repo name)
- DNS changes can take up to 24 hours to propagate
- After DNS propagation, GitHub automatically provisions an HTTPS certificate (Let's Encrypt)

## Email Forwarding (Hostinger)

| From | Forwards To |
|------|------------|
| contact@unlearntoreturn.com | durreshehwar411@gmail.com |

This was configured in Hostinger hPanel under **Emails > Email Forwarding**.

## SSL/HTTPS Certificate

- **Provider:** Let's Encrypt (auto-provisioned by GitHub Pages)
- **Domains covered:** `unlearntoreturn.com`, `www.unlearntoreturn.com`
- **Auto-renews:** Yes
- **HTTPS enforced:** Yes (HTTP redirects to HTTPS)

## Facebook/Meta Integration

- **Domain verification:** Meta tag in `<head>` — `facebook-domain-verification` with content `t9r2qm19468fo8h13ieakt9cyo0tr2`
- **Meta Pixel ID:** `1303676877923844` — tracks PageView events
- **Meta Business Suite:** Domain owned by "Unlearntoreturn" (ID: 2014157306163891)
