# DSR Attendance & Promo Suite (Updated Production Version)

Welcome to the **DSR Attendance & Promo Suite** repository. This repository provides a complete full-stack solution containing the Web Frontend, Backend API, and Cross-Platform React Native Mobile Application.

---

## 🌿 Repository Versions

This repository maintains two distinct branches for version control and baseline auditing:

| Branch | Version Description | Contents Included |
| :--- | :--- | :--- |
| **`main`** *(Active)* | **Updated Code (Production Ready)** | • **`frontend/`**: Updated production web frontend with unclipped branding, corrected input spacing, and attendance analysis.<br>• **`backend/`**: Node.js/Express API with AWS RDS MySQL integration and S3 storage.<br>• **`mobile/`**: Updated React Native mobile app with visit proof photo cards and native sharing. |
| **`before-update`** | **Previous Baseline Code** | The original working codebase before the recent branding, styling, and debundling enhancements. |

---

## 📁 Repository Structure (`main`)

```
dsr-attendance-promo/
├── frontend/               # Web Application (Port 3000)
├── backend/                # REST API (Port 5000)
│   ├── app/admin/          # Controllers, models, repositories, routes
│   └── .env.example        # Environment variable template
├── mobile/                 # React Native Mobile App (Android & iOS)
│   ├── android/            # Native Android Gradle configuration
│   ├── ios/                # Native iOS Xcode workspace & Podfile
│   └── src/                # Mobile screens, Redux, offline database
├── live_server.js          # Express proxy & static server
└── .gitignore              # Multi-tier exclusion for secrets & build caches
```

---

## 🚀 Getting Started

### 1. Backend Setup (Port 5000)
```bash
cd backend
npm install
cp .env.example .env
# Edit .env with your database credentials
node server.js
```

### 2. Frontend Setup (Port 3000)
```bash
# From project root
node live_server.js
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

### 3. Mobile App (Android & iOS)
```bash
cd mobile
npm install

# Run Android:
npm run android

# Run iOS (macOS only):
cd ios && pod install && cd ..
npm run ios
```

---

## 🔐 Security Notice
No sensitive database credentials, private API secrets, or Android release signing keys (`.jks`, `.pem`) are committed to this repository. All credentials should be provided via `.env` in the backend and local Gradle properties for mobile releases.
