# CLAUDE.md — Marcus Jardinez Resume Site

## What This Is

A static single-page resume website for Marcus Jardinez, hosted on GitHub Pages with a custom domain. No frameworks, no build step — pure HTML/CSS/JS.

## Live URLs

- **Primary:** https://marcusjardinez.dev
- **GitHub Pages fallback:** https://mjardinez3ds.github.io/Resume/
- **Repo:** https://github.com/Mjardinez3ds/Resume

## Local Files

Located at: `C:\Users\Mark\Desktop\resume-site\`

| File | Purpose |
|---|---|
| `index.html` | The entire site — resume, sidebar, download widget |
| `Marcus_Jardinez_Resume.docx` | Original Word file (1-page, healthcare-targeted version edited to be general) |
| `Marcus_Jardinez_Resume.txt` | Plain text version (ATS-friendly) |

## Key Design Decisions

- **No sidebar on the side** — verification panel is below the resume on both desktop and mobile
- **Desktop:** credential cards display in a CSS grid (auto-fill, minmax 190px)
- **Mobile (≤900px):** credential cards stack to 1 column
- **Download button:** fixed top-left, opens a dropdown with PDF / Word / Plain Text options
- **PDF generation:** client-side via html2pdf.js CDN — no server needed, renders from `#resume-content`
- **Print styles:** hide download widget and sidebar, resume only

## Two Versions of the Resume

The website (`index.html`) has **more content** than the DOCX/TXT:
- Table Games Dealer section has 5 bullets on the site vs 2 in the DOCX
- The summary closing sentence was changed from healthcare-specific to general across all formats
- Keep DOCX/TXT at 1 page — only expand on the website

## Deployment

Push to `main` branch — GitHub Pages auto-deploys. No CI needed.

```bash
cd C:\Users\Mark\Desktop\resume-site
git add .
git commit -m "your message"
git push
```

Git identity configured locally:
- email: mark2k10@gmail.com
- name: Mjardinez3ds

## DNS (Cloudflare)

Domain registered and DNS managed via Cloudflare (login: Marcus.jardinez.contractor@3ds.com).
All 5 records set to DNS only (gray cloud — not proxied):

| Type | Name | Content |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | mjardinez3ds.github.io |

## Credential Verification Links

| Credential | Verify URL | Notes |
|---|---|---|
| CompTIA A+ | https://cp.certmetrics.com/comptia/en/public/verify/credential/LL15E4GYEMQQ1TKK | |
| CompTIA Network+ | https://cp.certmetrics.com/comptia/en/public/verify/credential/Z4VS3B4YE2F11NS6 | |
| CompTIA Security+ | https://cp.certmetrics.com/comptia/en/public/verify/credential/BKYVB0VQNEREQQ5D | |
| AWS Cloud Practitioner | https://cp.certmetrics.com/amazon/en/public/verify/credential/17fc910f1c7548d6a1ca2e685d708df7 | |
| Azure AZ-900 | https://learn.microsoft.com/en-us/users/marcusjardinez-8133/credentials/a4f731c0f05c9b07 | |
| LPI Linux Essentials | https://cs.lpi.org/caf/Xamman/certification/verify/LPI000643778/9xww8wh2ts | |
| ITIL v4 Foundation | https://www.peoplecert.org/for-corporations/certificate-verification-service | Requires CAPTCHA — cert # GR671727448MJ |
| WGU B.S. IT | https://www.wgu.edu/alumni/commencement/e-diploma-verification/validate.html | Requires code entry — code: 2580-5UHO-MWZ5 |
