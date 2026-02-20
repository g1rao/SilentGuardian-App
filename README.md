# 🛡 Silent Guardian

### Next-Gen Personal Safety & Anti-Theft System

> A Predictive, Context-Aware Personal Safety Engine — built with Flutter for Android & iOS.

---

## ✨ Features

### 🔐 Security & Authentication
- **Google Sign-In** — Authenticate with your Google account
- **App Lock PIN** — Set a custom PIN to protect app access
- **Biometric Unlock** — Fingerprint or Face ID authentication
- **Emergency Code System** — Green (cancel) / Yellow (alert) / Red (SOS) PIN codes

### 📱 Smart Safety Engine
- **4-Stage Escalation Tree** — Intelligent alert chain: Check-in → GPS to contacts → Call emergency → Auto-dial 112
- **Configurable Timers** — Set delays for each escalation stage
- **Adaptive Timing** — Auto-adjusts escalation based on context
- **Shake to SOS** — Shake device to activate emergency mode
- **Fake Call** — Simulate incoming call to escape situations

### 🗺 Location & Navigation
- **Live Location Sharing** — Share real-time location with family & friends (30s updates)
- **Safe Walk Mode** — Monitored walking with route tracking
- **Route Deviation Detection** — Alerts when you deviate from expected route
- **Risk Zone Geofencing** — Mark unsafe locations, get alerts when entering
- **Reverse Arrival Timer** — "I'll arrive in X minutes" safety countdown

### 🔒 Anti-Theft Protection
- **Intruder Photo Capture** — Auto-capture front camera on wrong PIN attempts
- **SIM Change Detection** — Detect & alert on SIM card swap
- **GPS Alert on Theft** — Automatic location tracking when theft detected
- **Fake Blank Screen** — Show fake powered-off screen
- **Warning Screen** — Display owner info & warnings
- **Stealth Mode** — Run protection silently in background
- **Alarm on Theft** — Loud alarm on unauthorized access

### ☁️ Cloud Sync & Backup
- **Auto-Sync to Firebase** — All settings automatically backed up (debounced, throttled)
- **Cross-Device Sync** — Sign in on a new device, all data restores automatically
- **Granular Sync Controls** — Toggle what to sync: contacts, zones, theft settings, app settings
- **Manual Sync & Restore** — One-tap backup or restore from cloud
- **Last Synced Display** — See when data was last synced
- **Intruder Photo Upload** — Photos synced to Firebase Storage

### 👥 Social & Family
- **Friend Management** — Add friends by email for mutual location sharing
- **Family Location** — View family members' live location on map
- **Emergency Contact Groups** — Organize contacts for escalation stages

### 📝 Evidence Vault
- **Encrypted Evidence Storage** — Secure local storage of safety events
- **GPS Trail Logging** — Track location history during events
- **Timestamped Records** — Every event logged with time & context
- **PDF Export** — Export evidence as structured reports

### 🎨 Appearance & Customization
- **Theme Mode** — Dark / Light / System theme support
- **Onboarding Walkthrough** — Guided setup for new users
- **Permission Management** — Clear permission request screen

### 🌐 Platform Support
- **Android** — Full support with native platform channels
- **iOS** — Full support with Firebase integration
- **Offline-First** — Core features work without internet
- **Android 13+ Back Gesture** — Predictive back navigation support

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Flutter (Dart) |
| Auth | Firebase Auth + Google Sign-In |
| Database | Cloud Firestore |
| Storage | Firebase Storage |
| Local DB | Hive |
| State | Provider |
| Maps | Google Maps / Geolocator |
| Camera | camera package |
| Fonts | Google Fonts (Inter, Outfit) |
| Native | Kotlin (Android) / Swift (iOS) |

---

## 📁 Project Structure

```
lib/
├── config/
│   ├── theme.dart          # App theme & colors
│   └── routes.dart         # Navigation routes
├── providers/
│   ├── auth_provider.dart
│   ├── safety_provider.dart
│   ├── contacts_provider.dart
│   ├── evidence_provider.dart
│   ├── zones_provider.dart
│   ├── timer_provider.dart
│   └── social_provider.dart
├── services/
│   ├── cloud_sync_service.dart    # Firebase sync, location sharing, friends
│   ├── google_auth_service.dart   # Google Sign-In
│   ├── storage_service.dart       # Hive local storage
│   ├── notification_service.dart  # Local notifications
│   ├── camera_service.dart        # Intruder photo capture
│   ├── sim_detection_service.dart # SIM card monitoring
│   └── theft_protection_service.dart
├── screens/
│   ├── home_screen.dart
│   ├── settings_screen.dart
│   ├── onboarding_screen.dart
│   ├── sos_screen.dart
│   ├── theft_protection_screen.dart
│   └── ... (15+ screens)
└── main.dart
```

---

## 🚀 Getting Started

### Prerequisites
- Flutter SDK ≥ 3.x
- Dart ≥ 3.x
- Android Studio / Xcode
- Firebase project configured

### Setup
```bash
# Clone the repository
git clone https://github.com/g1rao/SilentGuardian.git
cd SilentGuardian

# Install dependencies
flutter pub get

# Run on Android
flutter run

# Run on iOS
cd ios && pod install && cd ..
flutter run -d ios
```

### Firebase Setup
1. Create a Firebase project at [console.firebase.google.com](https://console.firebase.google.com)
2. Add Android app with package: `com.silentguardian.silent_guardian`
3. Add iOS app with bundle ID: `com.silentguardian.silentGuardian`
4. Download `google-services.json` → `android/app/`
5. Download `GoogleService-Info.plist` → `ios/Runner/`
6. Enable **Google Sign-In** in Authentication → Sign-in method
7. Create **Firestore Database** in test mode
8. Enable **Firebase Storage**

---

## 📱 App Screenshots

*Coming soon*

---

## 🏗 Architecture

- **Offline-First**: Core safety features work without internet using Hive local storage
- **Cloud-Enhanced**: Firebase provides sync, backup, and social features when online
- **Provider Pattern**: State management using Provider for reactive UI updates
- **Platform Channels**: Native Kotlin/Swift code for SIM detection and device features

---

## ⚠️ Privacy & Security

- No hidden surveillance — clear user consent for all features
- Encrypted local storage for evidence vault
- Cloud data synced only when signed in
- Granular control over what data syncs
- All location sharing is opt-in and user-controlled

---

## 📄 License

This project is licensed under the MIT License.

---

## 🤝 Contributing

Contributions welcome! Please open an issue or submit a pull request.

---

*Built with ❤️ for personal safety*
