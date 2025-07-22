# GradMate NZ – Supporting International Students in Aotearoa 🇳🇿📱

**GradMate NZ** is an all-in-one Android application built using Java and Firebase to help international students transition and thrive in New Zealand. It covers onboarding, housing, navigation, mental health, finance, legal support, and social connection — all tailored to your city, university, and visa type.

---

## 🌟 Features Overview

### 🛬 1. Arrival Toolkit
- Personalized onboarding wizard (City, Uni, Visa Type, Language)
- Smart checklist system for IRD, bank setup, SIM, Wi-Fi, student discounts
- Deadline-based reminders and progress tracking

### 🏡 2. Flatting & Housing Support
- Flatmate finder with university email verification
- Flat contract decoder (future OCR integration)
- Rent estimators by suburb using real data
- Tenancy guide and issue reporting tools

### 🗺️ 3. City Navigation
- Google Maps integration showing clinics, banks, groceries, libraries
- Region-specific transport tips (AT Hop, Bee Card, etc.)
- Cultural POIs and student discounts by region

### 🤝 4. Peer Connect
- Match with peers based on language, university, country
- In-app moderated chat (Realtime)
- Interest-based groups and virtual campus tours

### 🧠 5. Mental Health & Culture Shock Aid
- Daily mood check-ins and wellbeing dashboard
- Coping resources for homesickness, loneliness, language barriers
- Story sharing board and Kiwi culture tips

### 💰 6. Finance 101
- IRD registration guidance and reminders
- GST explained simply, cost-of-living planner
- Bank comparison tool for student accounts
- Visa work rights checker and aggregated job board

### 🧑‍⚖️ 7. Legal & Emergency Support
- One-tap 111 emergency button with GPS location
- Legal guide for exploitation, tenancy, visa overstays
- Contacts for Immigration NZ, embassies, campus security

### 🌐 8. Multilingual & Accessibility
- Interface available in:
  - 🇬🇧 English
  - 🇨🇳 Chinese (Simplified)
  - 🇮🇳 Hindi
  - 🇵🇭 Tagalog
  - 🇰🇷 Korean
  - 🇪🇸 Spanish
- Read-aloud mode and Kiwi-English glossary

---

## 🧠 Architecture & Data Flow
### 🔄 Firebase Integration
Service	Usage
Firebase Auth	Login, sign-up
Firestore	User profiles, checklist progress
Realtime Database	Live in-app chat
Cloud Messaging	Local & remote notifications

### 🔧 MVVM Pattern
Activities: Handle navigation and user input

Fragments: Display feature views and observe LiveData

ViewModels: Contain business logic, communicate with Firebase

Models: Define app data (e.g., User, ChecklistItem)

Helpers: Modular utility classes (auth, i18n, notifications)

### 🚧 Development Roadmap
✅ Phase 1: Project Setup
 Firebase Auth & Firestore initialized

 Basic Login & Onboarding functionality

 User profile storage

📝 Phase 2: Checklist System
 ChecklistFragment with progress tracking

 Checklist sync with Firestore

 Reminder system with NotificationHelper

🗺️ Phase 3: Map Integration
 MapFragment using Google Maps SDK

 Static pin data for clinics, groceries, banks

🏠 Phase 4: Flatting & Legal Support
 Rent estimator UI

 Issue logging system

 OCR-based contract reader (future)

🤝 Phase 5: Peer Connect
 Matchmaking by country, uni, language

 Realtime chat with safety filters

 Interest-based groups (basic)

🚨 Phase 6: Emergency & Multilingual
 Emergency SOS screen

 Language selector + translated strings.xml

 Glossary for Kiwi slang

###🧪 Tech Stack
Feature	Technology
UI	XML + Material Design
Language	Java
Architecture	MVVM
Auth & DB	Firebase Auth + Firestore
Maps	Google Maps SDK
Notifications	FCM + Android NotificationManager
Real-Time Chat	Firebase Realtime Database
OCR (future)	ML Kit / Tesseract

## 🛠️ Project Setup
### 📁 Folder Structure (Simplified MVVM)

```plaintext
com.gradmate
├── activities
│   ├── LoginActivity.java
│   ├── OnboardingActivity.java
│   └── MainActivity.java
├── fragments
│   ├── DashboardFragment.java
│   ├── ChecklistFragment.java
│   ├── MapFragment.java
│   ├── ConnectFragment.java
│   └── HelpFragment.java
├── adapters
│   ├── ChecklistAdapter.java
│   └── UserAdapter.java
├── models
│   ├── ChecklistItem.java
│   ├── User.java
│   └── LocationPoint.java
├── viewmodels
│   ├── ChecklistViewModel.java
│   └── UserViewModel.java
├── firebase
│   ├── AuthHelper.java
│   └── DatabaseHelper.java
├── utils
│   ├── LanguageHelper.java
│   ├── Constants.java
│   └── NotificationHelper.java
