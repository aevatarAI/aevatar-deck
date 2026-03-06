---
layout: deck
title: "Week 10 Review"
date: 2026-03-06
week: "2026-W10"
type: review
member: Kai Wei
---

## Week 10 Review

**Aevatar Team** · March 6, 2026

---

## What is NyxID?

NyxID is our identity and access platform — it controls who can sign in, which services they can use, and acts as the secure gateway between users and all connected services.

---

## 1. Authentication Challenges (NyxID)

<div class="slide-meta"><span class="owner-tag">@Kai Wei</span> · <strong>NyxID Mobile · NyxID Platform</strong></div>

- When a service tries to use your credentials, you now get an approval challenge — you can approve or reject it in real time
- Two notification channels: **Telegram bot** and **mobile app push notifications**
- Includes a full management dashboard: notification settings, approval history, and active grants
- Deployed to production
- Mobile app submitted to the App Store for approval

***

### Telegram Authentication Challenge

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week10-review-kaiwei-telegram-challenge.png' | relative_url }}" alt="Telegram Authentication Challenge" style="max-height: 45vh;">
</div>

***

### Notification Settings

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week10-review-kaiwei-notification-settings.png' | relative_url }}" alt="Notification Settings" style="max-height: 45vh;">
</div>

***

### Active Grants

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week10-review-kaiwei-active-grants.png' | relative_url }}" alt="Active Grants" style="max-height: 45vh;">
</div>

***

### Approval History

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week10-review-kaiwei-approval-history.png' | relative_url }}" alt="Approval History" style="max-height: 45vh;">
</div>

---

## 2. Apple Login Integration (NyxID Platform)

<div class="slide-meta"><span class="owner-tag">@Kai Wei</span> · <strong>NyxID Platform</strong></div>

- Added Apple as a sign-in option — users can now log in with their Apple account alongside Google and GitHub
- Full flow working end-to-end and deployed to production: login, account creation, and account linking
- NyxID now supports **Google + GitHub + Apple** login

***

### Login Page with Apple Sign-In

<div style="display: flex; justify-content: center; align-items: flex-start; height: 60vh;">
<img src="{{ '/assets/images/week10-review-kaiwei-apple-login.png' | relative_url }}" alt="Apple Login" style="max-height: 45vh;">
</div>

---

## 3. Automated Deployment Pipeline (Sisyphus)

<div class="slide-meta"><span class="owner-tag">@Kai Wei</span> · <strong>Sisyphus</strong></div>

- Set up automated deployment so that our graph service can go from code change to live with a single click — no manual steps needed
- Web and API services now have full CI/CD pipelines ready — just waiting for merge to dev
