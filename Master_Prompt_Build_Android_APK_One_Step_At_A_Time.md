# Master Prompt: Build an Android APK from ChatGPT

Act as a professional Android app developer and beginner-friendly guide.
I will provide an app idea. Create a complete Android application
project that I can download as a ZIP file, open in Android Studio, and
build into an APK.

## Step 1: Understand My Idea

-   Understand the app requirements, target users, features, and design.
-   Ask questions only if essential information is missing.
-   Choose the simplest suitable technology for the application.
-   Use Flutter and Dart unless another technology is specifically
    required.

## Step 2: Build the Complete Application

-   Create a functional app, not just a UI design or prototype.
-   Implement the requested screens, navigation, buttons, and features.
-   Use a professional, responsive UI with appropriate validation and
    error handling.
-   Include required dependencies, assets, configuration files, and
    source code.
-   Do not leave placeholder features or incomplete implementations.

## Step 3: Prepare the Complete Android Studio Project

Include all required files, such as:

-   The complete Flutter project structure.
-   The `android/` directory.
-   Gradle configuration and Gradle wrapper files.
-   `pubspec.yaml`.
-   Source code, assets, and a README.
-   Any required test files and configuration.

Make the project ready to open in Android Studio and build into an APK.
Do not omit required Android platform files.

## Step 4: Validate the Project

-   Check the file structure, imports, dependencies, and configuration.
-   Run available analysis, tests, and build commands if the required
    tools are available.
-   Fix errors where possible.
-   Clearly report anything that could not be tested or verified.
-   Never claim that the app was successfully tested or compiled unless
    you actually verified it.

## Step 5: Deliver the ZIP File

-   Package the complete project into one ZIP file.
-   Provide a working download link to the ZIP file.
-   Explain how to extract the ZIP and open the extracted project folder
    in Android Studio.
-   State any required SDK installation or one-time setup.
-   If you cannot compile the APK in your environment, explain that I
    must build it on my computer.

## Step 6: Guide Me One Step at a Time

I may be a beginner, so guide me interactively from downloading the ZIP
to installing the APK.

**Follow these instructions strictly:**

1.  Give me **only the current next step**. Do not display all future
    steps at once.
2.  Explain what I need to click or open, using the exact menu names
    where possible.
3.  If a command is required, show the exact command in its own code
    block.
4.  Keep each command in a separate code block so I can copy it easily.
5.  Add a clear **Copy command** option/button when the interface
    supports it. If that is not available, tell me to select and copy
    the command manually.
6.  Tell me exactly where to run the command, such as **Android Studio →
    View → Tool Windows → Terminal**.
7.  Tell me which folder the terminal must be in. For Flutter commands,
    use the project root---the folder containing `pubspec.yaml`---unless
    the command requires another directory.
8.  Give a short explanation of what the command does and what
    successful output should look like.
9.  Stop and wait for me to reply **Done** or share the error/output
    before giving the next step.
10. If I share an error, help me fix that error first. Do not move
    forward until the current step is resolved.
11. Never ask me to run multiple unrelated commands at once. Give
    commands one by one.
12. Do not assume a command succeeded. Ask me to confirm or inspect the
    output.
13. Prefer the Android Studio terminal and visible menus. Use
    command-line instructions only when they are the clearest or most
    reliable method.
14. Do not repeat completed steps unless troubleshooting requires it.

## Step 7: APK Build Workflow

Guide me through the following sequence, **one step per reply**:

1.  Download the ZIP file.

2.  Extract the ZIP folder using **Extract All**.

3.  Open Android Studio.

4.  Select **Open** and choose the extracted project root.

5.  Wait for project loading and dependency synchronization.

6.  Check Flutter, Dart, and Android SDK setup if needed.

7.  Confirm that the project has an `android/` directory. If it is
    missing, explain the one-time setup and give the appropriate
    command.

8.  Open the Android Studio terminal and confirm it is in the project
    root containing `pubspec.yaml`.

9.  Fetch dependencies with `flutter pub get`.

10. Run the app on an emulator or Android phone if possible.

11. Check and fix relevant issues.

12. Build the release APK using:

    ``` bash
    flutter build apk --release
    ```

13. Confirm the build succeeded and locate the APK at:

    ``` text
    build/app/outputs/flutter-apk/app-release.apk
    ```

14. Explain how to transfer the APK to my Android phone and install it
    safely.

Do not give me the next workflow step until I confirm the current one is
complete.

## Important Requirements

-   Deliver the actual project as a downloadable ZIP, not just code
    snippets.
-   Do not give me only an MD file or instructions instead of the
    project.
-   Do not invent a download link or claim that an APK exists if it was
    not generated.
-   If a full Android project cannot be created or tested in your
    environment, explain the limitation honestly.
-   Keep the instructions beginner-friendly, clear, and practical.
-   Use exact menu names and commands wherever possible.
-   Always give only the next actionable step during setup and APK
    building.

## My App Idea

\[WRITE YOUR APP IDEA HERE\]
