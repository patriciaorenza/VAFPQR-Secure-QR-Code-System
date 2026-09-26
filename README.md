# VAFPQR — Secure QR Code Authentication System

**ICT302 IT Professional Practice Project — Murdoch University**
**Client:** Peter Cole & Mike Groeneweg <br>
**Team:** VAFPQR (6 members) <br>
**Timeline:** 20 May – 1 Aug 2026

> This repository is a **project showcase** curated by Patricia Orenza, who served as **Project Manager & Business Analyst** on this project. It documents the problem, solution, my role, and the outcome, with the original project documentation included for reference.
> 
---

## The Problem

Conventional QR codes have no built-in way to verify authenticity. A malicious person can print a fake QR code over a legitimate one, and users have no way of knowing before they scan, leading to phishing, fraud, or malware. As QR code adoption keeps growing across payments, menus, and event check-ins, so does the exposure to this risk.

## The Solution

VAFPQR is a secure QR authentication platform with three integrated parts:

- **Secure QR Code Generator & Admin Dashboard** (web) — generates QR codes with embedded JWT tokens (expiry, destination, signature), and lets admins manage codes, view scan metrics, and handle tampering reports.
- **Mobile Application** (Android) — scans QR codes, verifies their signature and expiry before redirecting, and lets users report suspicious codes with photo, location, and description.
- **Backend API & Database** — validates tokens, checks a blacklist of revoked codes, and logs scan telemetry.

Codes remain scannable by a normal phone camera app (backward compatible with standard QR scanners) while adding a verification layer for the VAFPQR mobile app.

**Tech stack:** Node.js + Express, PostgreSQL + Prisma ORM, React (admin dashboard), React Native (mobile app), hosted on Render.

## My Role: Project Manager & Business Analyst

Working across a 6-person team using a hybrid Waterfall/Agile methodology (2-week sprints), I was responsible for:

- **Requirements & analysis** — gathering requirements directly from the clients, analyzing and documenting them in the Requirements & Analysis document, and getting client sign-off before development began
- **Project planning & delivery** — building and maintaining the project schedule, breaking down and assigning work across the team, and tracking progress against milestones
- **Stakeholder management** — acting as the main point of contact for clients Peter Cole and Mike Groeneweg, running milestone updates and client demos
- **Risk management** — maintaining the project risk register and probability/impact matrix, and escalating issues early
- **UI/UX design** — designing the application's UI/UX prototype in Figma, feeding directly into the front-end build
- **Quality oversight** — defining component quality checklists and acceptance criteria alongside the team, and coordinating the test planning process

## Outcome

- All core functional requirements delivered: secure QR generation, JWT-based validation, expiry & blacklist checks, mobile scanning, tampering reports, and an admin dashboard with usage metrics.
- **26 of 27 documented test cases passed** in formal testing (the one failure — an admin-generated QR code with an invalid URL not being rejected as expected — was logged for follow-up).
- Delivered on schedule for the 1 Aug 2026 final submission, with full documentation (Project Management Plan, Requirements & Analysis, Design Document, Test Plan & Cases) and user/admin manuals handed over to the client.

## Repository Contents

| Folder | Contents |
|---|---|
| [`/docs`](./docs) | Project Management Plan, Requirements & Analysis, Design Document, Test Plan, Test Cases |
| [`/manuals`](./manuals) | Admin dashboard and mobile app user/installation manuals |
| [`/media`](./media) | Project slide deck and demo videos |

**Demo videos:**
- [Promo video](https://youtube.com/shorts/wxd6q5p9uVA)
- [Installation demo](./media/VAFPQR_Installation_Demo.mp4)

**Slide deck:** [VAFPQR_Slide_Deck.pptx](./media/VAFPQR_Slide_Deck.pptx)

> Note: the admin dashboard manual has had its demo login credentials redacted from this public copy for security reasons.

---

*This project was completed as part of Murdoch University's ICT302 IT Professional Practice unit. Team members: Patricia Orenza, Felixia Lim, Roy Hojin Yoo, Gu QiYu, Alvin Yeow, Vanessa Tan.*
