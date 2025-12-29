# Past Question Papers App - Internship Application

**Developer**: Irvin Senwedi  
**Repository**: https://github.com/Khulow/past-question-paper-v0.01-develop  


---

## What This Project Is About

A comprehensive Flutter mobile application that helps students practice academic questions across all subjects. The app provides an interactive learning platform with multiple question formats, real-time grading, and progress tracking.

### Key Features
- **Multi-format Questions**: MCQ (text/image), True/False, Short Answer, Essay, and Drag & Drop
- **LaTeX Math Support**: Beautiful rendering of mathematical equations and formulas
- **Practice Sessions**: Configurable timed tests with instant feedback
- **Progress Analytics**: Detailed performance tracking and insights
- **Offline-first**: Practice questions even without internet connection
- **Admin Portal**: Web-based question management and content upload system

### Technology Stack
**Frontend**
- Flutter 3.8+ (cross-platform mobile/web development)
- Riverpod (state management)
- Go Router (navigation)
- Flutter Math Fork (LaTeX rendering)

**Backend & Services**
- Firebase Authentication (user management)
- Cloud Firestore (NoSQL database)
- Cloud Functions (serverless backend logic)
- Firebase Storage (image/file storage)

### Platform Support
✅ Android  ✅ Web 

---

## How to Run This Project

### Prerequisites
- **Flutter SDK**: 3.8.0 or higher
- **Dart SDK**: 3.0.0 or higher  
- **Firebase Account**: Free tier is sufficient
- **Git**: For cloning the repository

### Step 1: Clone the Repository
```bash
git clone https://github.com/Khulow/past-question-paper-v0.01-develop.git
cd past-question-paper-v0.01-develop
```

### Step 2: Install Flutter Dependencies
```bash
flutter pub get
```

### Step 3: Configure Firebase
**Important**: Firebase configuration files are excluded for security. You need to generate them locally.

```bash
# Install FlutterFire CLI (one-time setup)
dart pub global activate flutterfire_cli

# Configure Firebase for this project
flutterfire configure
```

When prompted:
- Select or create a Firebase project
- Choose platforms: Android, iOS, Web
- This generates:
  - `lib/firebase_options.dart`
  - `android/app/google-services.json`
  - `ios/Runner/GoogleService-Info.plist`

### Step 4: Run the Application

**Mobile (Android/iOS)**
```bash
flutter run
```

**Web**
```bash
flutter run -d chrome
```

```

**Admin Portal**
```bash
flutter run -d chrome -t lib/main_admin.dart
```

### Step 5: Optional - Run Backend Functions Locally
```bash
cd functions
npm install
npm run serve
```

---

## Project Architecture

```
lib/
├── model/              # Data models (Question, User, etc.)
├── providers/          # Riverpod state providers
├── repositories/       # Data access layer
├── services/          # Business logic (Auth, Database, Storage)
├── viewmodels/        # MVVM view models
├── views/             # UI screens
├── widgets/           # Reusable components
├── utils/             # Helpers and constants
└── main.dart          # App entry point

functions/
├── src/
│   ├── services/      # Cloud Functions logic
│   └── helpers/       # Utility functions
└── index.js           # Functions entry point
```

---

## Development Highlights

### Problem Solved
Students often struggle to find quality practice materials and track their performance across subjects. This app centralizes question papers and provides intelligent practice tools with instant feedback.

### Technical Challenges Overcome
1. **LaTeX Rendering**: Integrated `flutter_math_fork` for complex mathematical equation display
2. **Offline Capability**: Implemented caching strategy for seamless offline practice
3. **Scalable Backend**: Cloud Functions handle test generation with blueprint-based question selection
4. **Multi-platform Support**: Single codebase runs on 6+ platforms with consistent UX

### Code Quality
- MVVM architecture for clean separation of concerns
- Riverpod for predictable state management
- Repository pattern for data abstraction
- Type-safe Firebase integration
- Comprehensive error handling

---


```



## Contact

**Irvin Senwedi**  
GitHub: [@Khulow](https://github.com/Khulow)  
Email: irvinsenwedi@gmail.com

---

**Note**: This project demonstrates full-stack mobile development skills including Flutter, Firebase, state management, cloud functions, and cross-platform deployment.
