<div align="center">

# 📱 Mobile App Development

### AI-Assisted App Development with Antigravity, Flutter and Android Studio

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Android Studio](https://img.shields.io/badge/Android_Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white)
![Google Antigravity](https://img.shields.io/badge/Google_Antigravity-E8590C?style=for-the-badge&logo=google&logoColor=white)

</div>

This guide explains how to build a Flutter mobile application with the help of AI tools, test it locally, generate an Android APK, and install it on a real Android device.

> **Workflow:** Idea → UI/UX Planning → AI Development → Flutter App → Testing → Android Studio → APK → Mobile Device

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Learning Outcomes](#2-learning-outcomes)
3. [Application Development Workflow](#3-application-development-workflow)
4. [Tools and Technologies](#4-tools-and-technologies)
5. [Environment Setup](#5-environment-setup)
6. [Build Your Application](#6-build-your-application)
7. [Test Your Application](#7-test-your-application)
8. [Prepare the App for Android Studio](#8-prepare-the-app-for-android-studio)
9. [Build the Android APK](#9-build-the-android-apk)
10. [Install the APK on a Phone](#10-install-the-apk-on-a-phone)
11. [Troubleshooting](#11-troubleshooting)
12. [Quick Reference](#12-quick-reference)

---

# 1. Introduction

AI-assisted app development uses AI tools to help with application design, code generation, project setup, testing, debugging, and development guidance.

The developer is still responsible for:

- Defining the application requirements.
- Reviewing the generated code.
- Testing the application.
- Fixing problems.
- Making final decisions about the application.

This guide follows the complete process:

**Idea → UI/UX Planning → AI Development → Flutter App → Testing → Android Studio → APK → Mobile Device**

---

# 2. Learning Outcomes

After completing this guide, you will be able to:

1. Understand the AI-assisted application development workflow.
2. Convert an application idea into a structured UI/UX design.
3. Use AI tools to assist with application development.
4. Understand the role of Flutter and Dart.
5. Run and test a Flutter application.
6. Prepare a Flutter project for Android Studio.
7. Generate an Android APK.
8. Install and test the APK on an Android phone.

---

# 3. Application Development Workflow

The complete workflow is:

| Step | Activity | Tool / Technology | Result |
|---|---|---|---|
| 1 | Define the application idea | Developer | Requirements and screen list |
| 3 | AI-assisted development | Google Antigravity | Flutter project and source code |
| 4 | Build the application | Flutter + Dart | Working mobile application |
| 5 | Test and debug | Antigravity + Browser | Verified application |
| 6 | Build the Android app | Android Studio | APK file |
| 7 | Install and test | Android device | Working mobile application |

---

# 4. Tools and Technologies

| Tool | Purpose |
|---|---|
| **MCP (Model Context Protocol)** | Connect AI tools with external tools and services |
| **Google Antigravity** | AI-assisted application development |
| **Flutter** | Framework for building cross-platform applications |
| **Dart** | Programming language used by Flutter |
| **Android Studio** | Android development, building, testing, and APK generation |

## 4.1 What is MCP?

**MCP** stands for **Model Context Protocol**.

In simple terms, MCP acts as a bridge between an AI tool and external tools or services. It allows the AI development environment to interact with supported external tools.

It helps maintain consistency between different screens instead of designing every screen completely separately.

---

# 5. Environment Setup

Before building the application, install and configure the required tools.

## 5.1 Set Up Google Antigravity

Antigravity is the AI-powered development environment used in this workflow.

1. Open a web browser.
2. Search for **Google Antigravity** and open the official website.
3. Click **Download**.
4. Download the version for your operating system.
5. Install Antigravity.
6. Open Google Antigravity.
7. Click **Sign in / Log in**.
8. Sign in with your Google account.
9. Use the Google account that has access to your Gemini plan or credits, if applicable.
10. Complete the initial setup.
11. Allow the required permissions.
12. Confirm that the Antigravity workspace opens successfully.

---

## 5.2 Install the Dart / Flutter MCP

The Dart MCP helps Antigravity work with Dart and Flutter.

1. Open **Google Antigravity**.
2. Open your Flutter project.
3. Go to **Settings**.
4. Open **Customization**.
5. Find **MCP Servers**.
6. Click **Install MCP** or **+ Add MCP**.
7. Search for `Dart`.
8. Find **Dart MCP Server**.
9. Click **Install**.
10. Wait for the installation to finish.
11. Confirm that Dart MCP is **Installed / Enabled**.

### If an Error Appears

1. Copy the complete error message.
2. Open the Antigravity Agent.
3. Paste the error.
4. Ask Antigravity to identify and fix the problem.
5. Try the installation again.

Use this prompt:

```text
I am trying to install the Dart MCP for my Flutter project, but I received the following error.

Analyse the error, identify the cause, fix the issue, and then help me install the Dart MCP successfully.

Error:
[PASTE THE COMPLETE ERROR HERE]
```

---
        [ or ] 
## Install Flutter

Use the official Flutter installation guide:

**Official Flutter Installation:**  
https://docs.flutter.dev/install/manual

### Windows Installation

1. Download the Flutter SDK ZIP from the official Flutter website.
2. Extract the ZIP file.
3. Use a suitable location such as:

```text
C:\Users\<YourName>\develop\flutter
```

4. The Flutter `bin` directory will be:

```text
C:\Users\<YourName>\develop\flutter\bin
```

### Add Flutter to Windows PATH

Open:

**Start → Search → Environment Variables → Edit the system environment variables → Environment Variables**

Under **User variables**:

1. Select `Path`.
2. Click **Edit**.
3. Click **New**.
4. Add:

```text
C:\Users\<YourName>\develop\flutter\bin
```

5. Click **OK → OK → OK**.
6. Close and reopen Command Prompt or PowerShell.

### Verify Flutter

Open a new Command Prompt and run:

```bash
flutter --version
```

Then:

```bash
dart --version
```

Finally:

```bash
flutter doctor
```

`flutter doctor` checks the Flutter, Dart, Android Studio, Android SDK, and other required components.

### Quick Verification

Run:

```bash
flutter --version
dart --version
flutter doctor
```

If `flutter --version` works successfully, Flutter has been added to the Windows PATH.

---

# 6. Build Your Application

After setting up Flutter, Dart, MCP, and Antigravity, you can build your application.

## 6.1 Live Demonstration: CookSmart

For the demonstration, we will build an application called **CookSmart**.

### Application Purpose

CookSmart is a recipe discovery application.

### Prompt for Antigravity

Copy and paste the following prompt into the Antigravity Agent:

```text
Build a complete Flutter mobile application called "CookSmart".

The application is a recipe discovery app.

TECHNOLOGY:
- Flutter
- Dart
- Android
- Use a clean and maintainable Flutter project structure.

SCREENS:

1. HOME SCREEN
- Display the CookSmart application name.
- Show featured recipes.
- Show food categories.
- Add a search bar.
- Display recipe cards with image, title and short information.

2. INGREDIENT SEARCH SCREEN
- Allow users to enter ingredients they currently have.
- Add an input field and Add Ingredient button.
- Display added ingredients as removable chips.
- Add a Search Recipes button.
- Display suitable recipe results.

3. RECIPE DETAILS SCREEN
- Display recipe name.
- Display recipe image.
- Display ingredients.
- Display preparation time.
- Display instructions.
- Add a Save Recipe button.

4. SAVED RECIPES SCREEN
- Display recipes saved by the user.
- Allow the user to open a saved recipe.
- Show a suitable empty state when there are no saved recipes.

NAVIGATION:
- Connect all screens correctly.
- Use simple and consistent navigation.
- Make sure the Android back button works correctly.

UI/UX:
- Modern mobile interface.
- Dark background.
- Warm orange accent colour.
- Clean white typography.
- Rounded cards.
- Good spacing.
- Responsive layout.
- Consistent buttons and components.
- Professional visual hierarchy.

FUNCTIONALITY:
- Implement working navigation.
- Implement ingredient input.
- Implement search/filter behaviour using local demo data.
- Implement save recipe behaviour.
- Use local/demo data initially.
- Keep the project structured so that an API or database can be connected later.

DEVELOPMENT REQUIREMENTS:
- Create the complete Flutter project.
- Use Dart.
- Organise the source code properly.
- Create reusable widgets where appropriate.
- Avoid unnecessary packages.
- Check for Dart and Flutter errors.
- Run Flutter analysis.
- Fix errors that prevent the application from running.
- Run the application locally.
- Verify navigation and major features.

Do not stop after creating the UI.

Build the complete working Flutter application and verify that it runs successfully.
```

### CookSmart Screens

| Screen | Main Content |
|---|---|
| Home | Featured recipes, categories, search |
| Ingredient Search | Ingredient entry and recipe search |
| Recipe Details | Recipe name, ingredients, time, instructions |
| Saved Recipes | Saved recipes and empty state |

### CookSmart Design

| Design Element | Specification |
|---|---|
| Background | Dark |
| Accent | Warm orange |
| Typography | Clean white |
| Style | Modern and mobile-friendly |
| Layout | Responsive with rounded cards |

---

## 6.2 Student Practice: Build Your Own App

After the CookSmart demonstration, create your own application.

Replace the information in the template below with your own idea.

```text
Build a complete Flutter mobile application called "[APP NAME]".

APPLICATION PURPOSE:
[Describe what the application does in 2–3 sentences.]

TECHNOLOGY:
- Flutter
- Dart
- Android
- Use a clean and maintainable Flutter project structure.

SCREENS:

1. [SCREEN NAME]
- [Feature]
- [Feature]
- [Feature]

2. [SCREEN NAME]
- [Feature]
- [Feature]
- [Feature]

3. [SCREEN NAME]
- [Feature]
- [Feature]
- [Feature]

4. [SCREEN NAME]
- [Feature]
- [Feature]
- [Feature]

Add more screens if required.

NAVIGATION:
- Connect all screens correctly.
- Use simple and consistent navigation.
- Make sure back navigation works correctly.

UI/UX:
- Design style: [DESCRIBE STYLE]
- Theme: [LIGHT / DARK]
- Primary colour: [COLOUR]
- Accent colour: [COLOUR]
- Typography: [DESCRIBE]
- Use consistent spacing, cards, buttons and components.
- Make the application responsive and mobile-friendly.

FUNCTIONALITY:
- [FEATURE 1]
- [FEATURE 2]
- [FEATURE 3]
- [FEATURE 4]

Use local/demo data initially where a backend is not available.

DEVELOPMENT REQUIREMENTS:
- Create the complete Flutter project.
- Use Dart.
- Organise the code properly.
- Create reusable widgets where appropriate.
- Implement all screens.
- Implement navigation.
- Check dependencies.
- Run Flutter analysis.
- Fix Dart and Flutter errors.
- Run the application.
- Test the major features.
- Make sure the application is ready for further development.

Do not only create a visual prototype.

Build the complete working Flutter application.
```

---

# 7. Test Your Application

After Antigravity builds the application, run it locally and test it.

Use this prompt:

```text
Hey, can you take this mobile app design and turn it into a working Flutter application?

Please:
- Convert the current design into a functional Flutter application.
- Make sure all screens are properly connected.
- Make sure navigation between screens works correctly.
- Keep the UI as close as possible to the approved design.
- Check for Flutter/Dart errors and fix them.
- Run the application locally.
- Make sure the app is ready for testing.
```

## 7.1 Open the App in the Browser

After the application starts successfully, Antigravity may provide a local URL such as:

```text
http://localhost:8080
```

Open the URL in your browser.

### Test These Items

- Application startup
- Every screen
- Navigation
- Buttons
- Forms
- Search
- Data display
- UI layout
- Responsiveness
- Application stability

### If an Error Appears

Do not immediately try to fix the error manually.

1. Copy the complete error.
2. Paste it into the Antigravity Agent.
3. Ask the Agent to diagnose the problem.
4. Apply the suggested fix.
5. Run the application again.
6. Test the affected feature again.

---

# 8. Prepare the App for Android Studio

After testing the application, prepare the Flutter project for Android Studio.

## 8.1 Prepare the Flutter Project

For example, for CookSmart:

```text
Prepare the CookSmart Flutter project for Android Studio and make sure it is ready to build as an Android APK.

Please:
- Check the complete Flutter project structure.
- Make sure all required dependencies are properly configured.
- Check and fix any Dart or Flutter errors.
- Configure the Android project correctly.
- Check for missing packages, files, or configuration issues.
- Run Flutter analysis.
- Fix errors that could prevent the app from building.
- Clean the project and fetch all required dependencies.
- Verify that the project is ready to open and build in Android Studio.
- Do not change the existing UI or functionality unnecessarily.

Finally, confirm that the project is ready to build an Android APK.
```

### For Your Own App

Replace the application name:

```text
Prepare my [APP NAME] Flutter project for Android Studio and make sure it is ready to build as an Android APK.

Please:
- Check the complete Flutter project structure.
- Make sure all required dependencies are properly configured.
- Check and fix any Dart or Flutter errors.
- Configure the Android project correctly.
- Check for missing packages, files, or configuration issues.
- Run Flutter analysis.
- Fix errors that could prevent the app from building.
- Clean the project and fetch all required dependencies.
- Verify that the project is ready to open and build in Android Studio.
- Do not change my existing UI or functionality unnecessarily.
```

### If Antigravity Reports an Error

Use:

```text
I received this error while preparing the Flutter project for Android Studio.

Analyse the error, identify the root cause, fix the issue, and verify the project again.

Error:
[PASTE THE COMPLETE ERROR HERE]
```

---

# 9. Build the Android APK

## 9.1 Open the Flutter Project in Android Studio

A Flutter project normally contains an Android-specific folder:

```text
Your Flutter Project
│
├── lib/
├── assets/
├── pubspec.yaml
│
└── android/
    ├── app/
    ├── gradle/
    ├── gradle.properties
    ├── settings.gradle
    └── ...
```

### Important Folders

| Folder / File | Purpose |
|---|---|
| `lib/` | Dart source code |
| `assets/` | Images, fonts, and other resources |
| `pubspec.yaml` | Dependencies, assets, and project configuration |
| `android/` | Android-specific project files |

## 9.2 Open the Project

1. Open **Android Studio**.
2. Select **Open**.
3. Navigate to your Flutter project.
4. Select the project or its `android` folder as required by your Android Studio setup.
5. Click **Open**.
6. Wait for Android Studio to load the project.
7. Wait for Gradle synchronisation.
8. Allow required dependencies to download.
9. Do not close Android Studio during synchronisation.

Example:

```text
C:\Users\<YourName>\Documents\Mobile_Apps\CookSmart
```

## 9.3 Wait for Gradle Sync

Android Studio may display messages such as:

```text
Importing 'android' Gradle Project
```

or:

```text
Gradle: Downloading...
```

Wait until the process finishes.

Do not interrupt Gradle synchronisation unless it is clearly stuck or has failed.

### If a Gradle Error Appears

Copy the complete error and use this prompt in Antigravity:

```text
Android Studio is showing the following error while importing or syncing the Android project.

Please analyse the error, identify the root cause, fix the project configuration, and make sure the Flutter project can be opened and built successfully in Android Studio.

Error:
[PASTE THE COMPLETE ERROR HERE]
```

After the issue is fixed, return to Android Studio and sync the project again.

---

## 9.4 Generate the APK

Once Gradle synchronisation completes successfully:

1. Open the **Build** menu.
2. Select **Generate App Bundles or APKs**.
3. Select **Generate APKs**.
4. Wait for the build to finish.
5. Do not close Android Studio during the build.
6. When the build succeeds, Android Studio will show a success message.
7. Click **Locate**.
8. Find the generated `.apk` file.
9. Copy the APK to a convenient location, such as the Desktop.

---

# 10. Install the APK on a Phone

## 10.1 Transfer the APK

You can transfer the APK using:

- USB cable
- Quick Share
- Google Drive
- WhatsApp
- Another suitable file-transfer method

### Recommended: USB

1. Connect the Android phone to the computer using USB.
2. Unlock the phone.
3. Select **File Transfer** when prompted.
4. Open the phone storage on the computer.
5. Copy the `.apk` file.
6. Paste it into the phone's **Downloads** folder.
7. Safely disconnect the phone.

## 10.2 Install the APK

1. Open **Files / File Manager** on the phone.
2. Open **Downloads**.
3. Tap the `.apk` file.
4. If Android asks for permission, allow installation from the requested source.
5. Tap **Install**.
6. Wait for the installation to complete.
7. Tap **Open**.

## 10.3 Test the Installed Application

Check:

- Application startup
- Every screen
- Navigation
- Buttons
- Forms
- Search
- Data display
- UI layout
- Responsiveness
- Application stability

---

# 11. Troubleshooting

Use the same basic troubleshooting process throughout the workflow.

### Error-Resolution Process

```text
Error occurs
     ↓
Copy the complete error
     ↓
Paste it into Antigravity
     ↓
Ask AI to identify the root cause
     ↓
Apply the fix
     ↓
Run analysis / build again
     ↓
Test the application
```

## 11.1 General Error Prompt

```text
I found an error in my Flutter application.

Please:

1. Analyse the complete error.
2. Identify the root cause.
3. Identify the file responsible.
4. Fix the issue.
5. Check whether the fix affects other parts of the application.
6. Run Flutter analysis again.
7. Run the application again.
8. Verify that the issue is completely resolved.

Error:
[PASTE COMPLETE ERROR HERE]
```

## 11.2 Where to Use the Error Method

| Problem | What to Do |
|---|---|
| Dart MCP installation | Paste the complete error into Antigravity and ask for a fix |
| Running the app | Paste the complete error and run the app again |
| Preparing the project | Use the error prompt and verify the project |
| Gradle / Android Studio error | Paste the error into Antigravity, fix it, then sync again |

---

# 12. Quick Reference

## Complete Workflow

| Step | Task | Tool |
|---:|---|---|
| 1 | Define the application idea | Developer |
| 3 | Set up Antigravity | Antigravity |
| 5 | Install Flutter and Dart | Flutter |
| 6 | Build the application | Antigravity + Flutter |
| 7 | Run and test the application | Browser |
| 8 | Prepare the project for Android | Antigravity |
| 9 | Open and sync the project | Android Studio |
| 10 | Wait for Gradle synchronisation | Android Studio |
| 11 | Generate the APK | Android Studio |
| 12 | Transfer and install the APK | Android device |

## Important Points

- The developer defines the requirements and reviews the result.
- AI tools assist with design, development, debugging, and guidance.
- Flutter is used to build the mobile application.
- Dart is the programming language used by Flutter.
- Android Studio is used to prepare and build the Android application.
- Test the application before generating the APK.
- Always use the complete error message when asking AI to fix a problem.
- Keep API keys and other credentials private.
- Never place API keys in public repositories or source code.
- Restart Antigravity after installing or changing MCP servers when required.

---

## Final Goal

By following this guide, you should be able to go from:

**Application Idea**

↓

**UI/UX Design**

↓

**AI-Assisted Flutter Development**

↓

**Local Testing**

↓

**Android Studio**

↓

**APK Generation**

↓

**Android Phone**

↓

**Working Mobile Application**
