# joshuagoh.dev

My personal portfolio website, built to showcase my cybersecurity projects,
personal work and (soon) blog posts.

🔗 **Live site:** https://joshuagoh.dev

## About
I'm a first-year Bachelor of IT student at Monash University, majoring in
cybersecurity. I built this site to learn how websites actually work, from
code to hosting to security, rather than using a website builder.

## Built with
- HTML, CSS and JavaScript, written and edited in VS Code
- Git and GitHub for version control
- Cloudflare Pages for hosting (auto-deploys on every push)
- A custom domain with email through Purelymail

## Security
- **A+ on securityheaders.com:** HSTS, Content Security Policy, X-Frame-Options
  and Permissions-Policy, configured in [`_headers`](_headers)
- **Email authentication:** SPF, DKIM and DMARC on my domain to prevent spoofing
- **No inline scripts,** so the CSP can block injected JavaScript
- **Privacy by default:** no tracking cookies, image metadata stripped, minimal
  personal details published

## Dev log
I'm documenting the whole build, including every mistake, in
[DEVLOG.md](DEVLOG.md).

## Credits
Design based on the **Waldo** template by [StyleShout](https://styleshout.com),
used under its free licence and customised by me. Icons by
[Atomicons](https://atomicons.vercel.app/) (CC BY 4.0).