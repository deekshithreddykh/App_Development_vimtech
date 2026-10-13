# Master Prompt: Build an Android APK from ChatGPT

Act as a professional Android app developer. I will provide an app idea,
and you must create a complete, functional Android application that I
can download as a ZIP file, open in Android Studio, and build into an
APK.

## Step 1: Understand My Idea

-   Understand the app requirements, target users, features, and design.
-   Ask questions only if essential information is missing.
-   Choose the simplest suitable technology for the application.

## Step 2: Build the Complete Application

-   Create a fully functional app, not just a UI design or prototype.
-   Use Flutter and Dart unless another technology is specifically
    required.
-   Implement all requested screens, navigation, buttons, and features.
-   Use a professional, responsive UI with proper error handling.
-   Include all required dependencies, assets, configuration files, and
    source code.
-   Do not leave placeholder features or incomplete implementations.

## Step 3: Prepare the Android Studio Project

-   Include the complete Flutter project structure.
-   Include the `android/` directory, Gradle configuration, and Gradle
    wrapper files.
-   Include `pubspec.yaml`, all source files, assets, and a README.
-   Ensure the project is configured for Android APK generation.
-   Do not omit files required to open and build the project.

## Step 4: Validate the Project

-   Check the file structure, imports, dependencies, and configuration.
-   Run available analysis, tests, and build commands when the required
    tools are available.
-   Fix errors where possible.
-   Never claim that the app was tested or compiled successfully unless
    you actually verified it.

## Step 5: Deliver the ZIP File

-   Package the entire Android Studio project into one ZIP file.
-   Provide a direct download link to the ZIP.
-   Explain how to extract it and open the extracted project in Android
    Studio.
-   Clearly mention any required SDK installation or one-time setup.
-   If you cannot compile the APK in your environment, explain that the
    APK must be built on my computer.

## Step 6: Explain How to Generate the APK

Give me these steps in order:

1.  Download the ZIP file.

2.  Extract the ZIP folder.

3.  Open Android Studio.

4.  Select **Open** and choose the extracted project folder.

5.  Wait for project synchronization and dependency downloads.

6.  Resolve any required SDK setup.

7.  Run the app on an emulator or Android phone to test it.

8.  Build the release APK using Android Studio's available Flutter build
    action or the terminal command:

    ``` bash
    flutter build apk --release
    ```

9.  Tell me the exact APK output path:

    ``` text
    build/app/outputs/flutter-apk/app-release.apk
    ```

10. Explain how to copy the APK to my Android phone and install it.

## Important Requirements

-   Deliver the actual project as a downloadable ZIP, not just code
    snippets.
-   Include all necessary Android project files.
-   Do not give me only an MD file or instructions instead of the
    project.
-   Do not invent a download link or claim that an APK exists if it was
    not generated.
-   Make the project as complete and easy to build as possible.

## My App Idea

\[WRITE YOUR APP IDEA HERE\]
