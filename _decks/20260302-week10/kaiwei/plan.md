---
layout: deck
title: "Week 10 Plan"
date: 2026-03-02
week: "2026-W10"
type: plan
member: Kai Wei
---

## Week 10 Plan

**Aevatar Team** · March 2, 2026

---

## 1. Automated Deployment Pipeline

**Sisyphus Infrastructure** · Due Friday 3/6

CI/CD pipeline configured and tested for all Sisyphus services (API, Web, graph, notification, storage) enabling single-trigger deployments with zero manual steps.

- Each service deploys to staging via a single pipeline trigger
- Zero manual steps required in the deployment process
- Pipeline configs committed to the code repository
- Supports system stability by eliminating manual deployment errors

---

## 2. Mobile App Permission Management

**NyxID Mobile** · Due Friday 3/6

UI/UX design spec and technical architecture for permission management in the NyxID mobile app, plus initial backend/frontend development started.

- Design spec reviewed and approved by stakeholder
- At least 1 working API endpoint for permission CRUD operations deployed to dev
- Permission data model implemented
- Strengthens security compliance and supports mobile platform adoption

---

## 3. Apple Login Integration

**NyxID Platform** · Due Friday 3/6

Full Apple Sign-In integration for the NyxID platform, enabling users to authenticate with their Apple ID end-to-end.

- Apple Sign-In login flow fully functional (redirect, auth callback, token exchange)
- Server-side token verification and user account creation/linking implemented
- Frontend login button wired up and working in staging environment
- Supports user adoption by offering a trusted, frictionless sign-in option
