# 🌐 Localloop — SDG 8: Decent Work & Economic Growth

> **Find work, skills, and services nearby.**  
> Connecting communities, empowering fair opportunities, and supporting inclusive economic growth across Sri Lanka.

<p align="left">
  <img alt="SDG 8" src="https://img.shields.io/badge/SDG-08%20Decent%20Work%20%26%20Economic%20Growth-A21942?labelColor=1a1a1a">
  <img alt="React Native" src="https://img.shields.io/badge/React%20Native-mobile-blue">
  <img alt="Expo" src="https://img.shields.io/badge/Expo-CLI-black">
  <img alt="Appwrite" src="https://img.shields.io/badge/Backend-Appwrite-ff476f">
  <img alt="License" src="https://img.shields.io/badge/License-MIT-green">
  <img alt="PRs" src="https://img.shields.io/badge/PRs-welcome-brightgreen">
</p>

> **Why SDG 8?** Localloop is designed around UN **SDG 8** to promote sustainable work environments, fair pay, safe workplaces, and inclusive growth.

---

## ✨ Core Features
- 🔎 **Local Job & Gig Matching** — filter by skill, location, and fair-pay range.  
- 🧭 **Skills & Training** — curated micro-courses and badges to upskill youth.  
- 💸 **Fair Pay & Budget Helper** — simple calculators and transparent rates.  
- 🛡️ **Safe Work Tips** — in-app guidance aligned with labor rights.  
- 🌏 **Tri-lingual** — English / Sinhala / Tamil.  
- 📶 **Low-bandwidth & Offline-first** — essential flows work even with poor signal.

---

## 🎯 SDG-8 Alignment (Targets → App features)
- **8.3** (productive activities & entrepreneurship) → Local business listings + gig marketplace  
- **8.5** (full & equal pay for work of equal value) → Fair-pay ranges & pay-gap prompts  
- **8.6** (reduce youth not in employment/education/training) → Skill badges & training feed  
- **8.8** (labor rights & safe workplaces) → Safety tips, report-issue flow, and guidance links

---

## 🖼️ Screenshots
<p align="left">
  <img src="assets/screens/onboarding-1.png" width="240" />
  <img src="assets/screens/onboarding-2.png" width="240" />
  <img src="assets/screens/home.png" width="240" />
</p>

> Put your images into `assets/screens/` and update paths above.

---

## 🛠 Tech Stack
- **Frontend:** React Native (Expo)  
- **Auth & Backend:** Appwrite (Account, Database, Storage)  
- **Maps/Location:** Expo Location / Map provider  
- **State:** Zustand/Redux (your pick)  
- **i18n:** `react-native-localize` + JSON dictionaries

---

## 🚀 Quick Start

### 1) Prerequisites
- Node.js 18+, Git
- Expo CLI: `npm i -g expo-cli`
- Appwrite project (Cloud or self-hosted)

### 2) Configure Appwrite (example)
```js
// src/lib/appwrite.ts
import { Client, Account, Databases } from "react-native-appwrite";

const client = new Client()
  .setEndpoint("https://cloud.appwrite.io/v1")  // your endpoint
  .setProject("APPWRITE_PROJECT_ID")            // from Appwrite console
  .setPlatform("YOUR_BUNDLE_ID_OR_PACKAGE");    // e.g., com.localloop.app

export const account = new Account(client);
export const db = new Databases(client);
