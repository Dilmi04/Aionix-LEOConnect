# 🦁 LEOConnect  
### Empowering Leos. Connecting Clubs. Inspiring Change.  

**LEOConnect** is a smart mobile application built to unite the **Leo Multiple District 306 (Sri Lanka)** community under one digital platform.  
It enables Leos to connect, collaborate, and celebrate their service through AI-powered recommendations, social interaction, and gamified experiences.  

---

## 🚀 Project Overview

| Category | Details |
|-----------|----------|
| **Competition** | AlgoArena 2025 – Phase 2 |
| **Team Name** | Aionix |
| **University** | University of Sri Jayewardenepura |
| **Faculty** | Faculty of Computing |
| **Team Members** | Dilmi Sandunika • Devini Thathsarani |

---

## 🧩 Key Features

✅ **AI-Based Event Recommendations** – Personalized volunteer opportunities based on user interests, district, and engagement.  
✅ **Role-Based Access** – Webmasters can create and manage posts/events; regular Leos can join, react, and share.  
✅ **Gamification System** – Earn badges and points for every action — making volunteering fun and rewarding.  
✅ **Impact Dashboard** – Track personal and collective service impact across districts.  
✅ **Explore + Event Calendar** – Discover ongoing and upcoming Leo events on a map or calendar view.  
✅ **Leo Stories & Media Upload** – Clubs can share short video clips to highlight achievements.  
✅ **AI Suggestion Popup** – Smart reminder for new events and projects matching your interests.  
✅ **Contact Admins & About Page** – Direct communication with Leo MD306 admins.

---

## 🧠 Tech Stack

| Layer | Technology |
|--------|-------------|
| **Frontend** | Flutter (Dart) |
| **Backend** | Firebase Cloud Functions |
| **Database** | Cloud Firestore (NoSQL) |
| **Authentication** | Firebase Auth (Google Sign-In) |
| **Storage** | Firebase Storage |
| **AI Logic** | Cloud Function (Node.js / Python) |
| **Hosting (optional)** | Firebase Hosting |
| **Design Tool** | Figma |

---

## ⚙️ System Architecture

![System Architecture](docs/system-architecture.png)

- **Flutter App** — Handles UI, authentication, and user interactions.  
- **Firebase Auth** — Secure Google login.  
- **Firestore DB** — Real-time data (users, posts, events).  
- **Cloud Functions** — AI matching, gamification logic, notifications.  
- **Firebase Storage** — Image & video uploads.  

---

## 🗄️ Database Structure (simplified)

**Collections**

- `users` → user profiles, interests, points, badges  
- `clubs` → club data & admins  
- `posts` → updates, announcements, and media  
- `events` → upcoming projects & joined members  
- `notifications` → system alerts  

---

## 🧮 AI Recommendation Logic (simplified)

Each event is scored based on:
```text
score = (tagMatches * 3) + (sameDistrict ? 2 : 0) + (recentEvent ? 1 : 0)
