# Flutter Prompts - Apps for Senior Citizens

One standalone prompt per page. Give each team only its own page.

Each prompt below is in its own box. Use the copy button on the box to copy just that prompt.

26. ONE-TAP HELP
27. MY MEDICINE SCHEDULE
28. EASYVIEW CLOCK
29. PHONE FRIEND
30. SCAM SHIELD SENIOR
31. FAMILY PHOTO MEMORIES
32. VOICE NOTES POCKET
33. MY APPOINTMENT BOOK
34. WATER BELL
35. GENTLE MOVEMENT GUIDE
36. DAILY BRAIN GYM
37. LARGE TEXT READER
38. MY IMPORTANT NUMBERS
39. HOUSEHOLD REMINDER
40. SIMPLE UPI TUTOR
41. GROCERY VOICE LIST
42. MY SPENDING BOOK
43. DAILY WELLNESS JOURNAL
44. HEARING-FRIENDLY ALERTS
45. MY WALK LOG
46. HOME SAFETY CHECKER
47. PRESCRIPTION ORGANIZER
48. FESTIVAL & BIRTHDAY CALENDAR
49. VOICE READING HELPER
50. MY DOCUMENTS GUIDE

---

## 26. ONE-TAP HELP

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 26. ONE-TAP HELP

## APPLICATION PURPOSE

Build "One-Tap Help", a Flutter app that gives quick access to saved family contacts and emergency services. It solves the problem of a senior having to search through a phone in a stressful moment. Target users are senior citizens and their families; main use case: tap one large button to call a family member or emergency services. The app does not replace emergency services and cannot guarantee any call or message; emergency numbers are editable, with 112 pre-filled as a default for India and other numbers entered by the family after verifying them.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, url_launcher (opens the dialer or SMS composer, which the user confirms), geolocator (optional location link with a permission explanation).

## SCREENS

1. Home – very large buttons: each saved family contact with photo or initials, Call Emergency Number, Send "I need help" Message, Show My Details.
2. Contacts Setup (family mode) – name, phone, relationship, optional photo and order; at least one contact prompted on first run; validation.
3. Emergency Numbers – editable list (general emergency, ambulance, police, local doctor) with tap-to-dial.
4. Help Message – editable text with an optional location link; opens the SMS composer pre-filled for the user to send.
5. Show My Details – full-screen large text of name, address note, key contact and a short note (typed by the user) to show a helper.
6. Settings – button size, confirm-before-call or press-and-hold, haptics, theme.

## NAVIGATION

Home is the main screen; Setup and Settings behind a family PIN or a long-press so they are not changed by accident. Back returns one level.

## UI/UX

Very clear, calm style, light, dark and high-contrast. Primary red #C62828 for emergency actions, accent blue #1565C0, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Buttons at least 96dp tall with icon and text, no hidden gestures. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Tap or hold opens the dialer with the number pre-filled; the user presses call.
- Help message opens the SMS composer with the prepared text and optional location link.
- Handle missing permissions and no-handler cases with plain messages; validation and persistence.

## DATA AND BACKEND

Local storage only; no cloud, account or analytics. Test on a physical device and do not place real emergency calls during testing.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for contact ordering and validation, message building, press-and-hold confirmation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 27. MY MEDICINE SCHEDULE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 27. MY MEDICINE SCHEDULE

## APPLICATION PURPOSE

Build "My Medicine Schedule", a Flutter app where the user sets medicine names and times and receives local notifications. It helps seniors remember doses and lets family see what was taken. Target users are senior citizens and carers; main use case: add each medicine once with its times, get reminders and tap Taken. The app gives no medical advice: names, doses and times are entered exactly as the doctor or pharmacist directed, and the app tells users to follow their doctor's instructions.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, share_plus, intl. Reminders must be rescheduled after reboot; handle the Android 13+ notification and exact-alarm permissions.

## SCREENS

1. Today – timeline of doses by time with large Taken and Skip buttons, status (Upcoming, Taken, Missed) and a simple progress summary; empty state prompting the first medicine.
2. Add/Edit Medicine – name, strength or dose text, form (tablet, syrup, drops, other), times per day, days of the week, start and end date, with-food note, optional notes; validation.
3. Reminder Alert – full-screen notification action: medicine name, dose text, Taken and Remind Me in 10 Minutes buttons.
4. Medicines – list of all medicines with next dose; edit, pause and delete with confirm.
5. History – calendar of days with doses taken and missed; detail per day.
6. Refill Reminder – optional tablet count and refill-by date.
7. Share Summary – last 7 days as text for a family member or doctor visit.
8. Settings – snooze length, alert sound and vibration, text size, theme.

## NAVIGATION

Bottom tabs Today, Medicines, History, Settings; floating Add. Back returns one level.

## UI/UX

Large, calm, clear style, light, dark and high-contrast. Primary teal #00796B, accent amber #FFA000, background #F6FBFA. Font Atkinson Hyperlegible (bundled). Status by icon and text, 80dp action buttons. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Dose instances generated from schedules; reminders scheduled for each; rescheduled after edits, boot and restart.
- Taken and Skip recorded with timestamp; missed after a configurable window; the app never suggests doubling or changing doses.
- Refill reminders; adherence history; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud. Test notifications on a physical device.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for dose generation from schedules, missed detection, reminder scheduling and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 28. EASYVIEW CLOCK

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 28. EASYVIEW CLOCK

## APPLICATION PURPOSE

Build "EasyView Clock", a Flutter app that displays a large clock, the date and a day or night indicator. It helps seniors with low vision or memory difficulties know the time and the day at a glance. Target users are senior citizens; main use case: keep the phone on a stand as a bedside or table clock. It is not an alarm app.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts (speak the time),

wakelock_plus, intl.

## SCREENS

1. Clock – huge digital or analog time, full date with the day of the week in words, and a greeting with a sun or moon icon (Good Morning, Good Afternoon, Good Evening, Good Night); tap anywhere to hear the time and date spoken.
2. Display Settings – digital or analog, 12 or 24 hour, show seconds, show greeting, font size slider, colour theme (white on black, black on white, yellow on black), keep screen on, night dimming schedule.
3. Day Info – an optional second screen showing today's date, the month calendar and "Today is..." in large type.
4. Settings – language of day and month names, speech on tap, theme.

## NAVIGATION

Clock is home; Settings and Day Info through two large buttons on a hidden-until-tapped bar. Back exits the app only from the Clock.

## UI/UX

Minimal very large style, light, dark and high-contrast. Primary white and black pairing with yellow accent #FFD600. Font Atkinson Hyperlegible or Roboto Mono for numerals (bundled). Time text at least 120sp, scalable; strong contrast; no fine details. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Time updates each second using the system clock; midnight rollover and timezone changes handled.
- Greeting by time-of-day ranges that the user can adjust.
- Night dimming reduces brightness and switches to a dark theme in the chosen hours; speak on tap.

## DATA AND BACKEND

Local shared_preferences only; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for greeting ranges, date formatting, night schedule logic and settings persistence and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 29. PHONE FRIEND

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 29. PHONE FRIEND

## APPLICATION PURPOSE

Build "Phone Friend", a Flutter app that teaches seniors how to make calls, send messages and adjust phone settings. It builds confidence with smartphones. Target users are senior citizens and family helpers; main use case: follow a short step-by-step lesson, practise in a safe mock phone and open the real setting when ready. Android versions and phone makers differ, so steps are general and the app says so.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts (optional), android_intent_plus (open real system settings such as sound, display, Wi-Fi and accessibility).

## SCREENS

1. Home – lesson groups, practice, My Progress.
2. Lessons – Make a Call, Answer or End a Call, Save a Contact, Send a Text Message, Send a Photo, Adjust Volume, Make Text Bigger, Brightness, Connect to Wi-Fi, Turn On Do Not Disturb, Charge and Battery Tips.
3. Lesson – numbered steps with large illustrations, Next and Back, Read Aloud, and a button "Show me on my phone" that opens the real setting where one exists.
4. Practice Phone – a mock phone with a dialer, contacts and messages where the user taps through the lesson tasks and is told when each is done; nothing real is called or sent.
5. Words to Know – glossary (app, icon, swipe, tap, notification, Wi-Fi).
6. Progress – lessons completed and badges.
7. Settings – text size, speech, theme.

## NAVIGATION

Home > Group > Lesson > Practice; Words to Know and Progress from Home. Back returns one level.

## UI/UX

Friendly large-print style, light, dark and high-contrast. Primary blue #1976D2, accent orange #FB8C00, background #F7FAFD. Font Atkinson Hyperlegible (bundled). One step per screen, large arrows, 72dp buttons, illustrations drawn in Flutter with highlighted tap targets. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Lesson JSON (steps, illustration key, practice task, optional system-setting intent).
- Practice mode detects the expected tap sequence and gives encouraging feedback; no real calls or messages.
- Intent launching handles unsupported settings gracefully; progress saved.

## DATA AND BACKEND

Bundled JSON and local progress; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for lesson progression, practice task matching, intent fallback handling and progress storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 30. SCAM SHIELD SENIOR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 30. SCAM SHIELD SENIOR

## APPLICATION PURPOSE

Build "Scam Shield Senior", a Flutter app that teaches seniors about OTP, UPI, fake-call and suspicious-link scams. It helps protect savings and personal details. Target users are senior citizens and families; main use case: learn the warning signs through short lessons, test knowledge with "Is this a scam?" scenarios and keep a quick-reference card. The app does not scan messages or calls; helpline numbers are editable, with 1930 (India's national cyber crime helpline) pre-filled for the team to verify.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts (optional), url_launcher (dialer).

## SCREENS

1. Home – Learn, Test Yourself, Quick Rules, If I Was Scammed.
2. Lessons – OTP Scams, UPI and QR Scams, Fake Calls (bank, police, courier, relative in trouble), Suspicious Links and Messages, Lottery and Prize Scams, Fake Customer Care Numbers.
3. Lesson – a short story-style example, "How to spot it" signs, "What to do", Read Aloud.
4. Test Yourself – realistic sample messages and call descriptions with the choices Scam and Safe, followed by an explanation; 10 per round.
5. Quick Rules – a large card of golden rules (never share OTP, PIN or password; receiving money never needs your PIN; hang up and call back on a trusted number).
6. If I Was Scammed – step list: contact the bank, call the helpline (tap-to-dial), note details, change passwords, tell family.
7. Progress – lessons done and test scores.
8. Settings – editable helpline numbers, text size, speech, theme.

## NAVIGATION

Home > Lessons > Lesson; Home > Test > Result. Back returns one level.

## UI/UX

Protective calm style, light, dark and high-contrast. Primary navy #1A237E, accent orange #FF6F00, red #C62828 for danger with text, background #F6F7FC. Font Atkinson Hyperlegible (bundled). 20sp+ text, plain language, large Scam and Safe buttons. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Lesson and scenario JSON written and reviewed by the team with real-world accuracy.
- Scenario quiz with explanations, score and weak topics; quick rules card; dialer opened pre-filled.
- Progress persistence; no personal data entered.

## DATA AND BACKEND

Bundled JSON and local progress; no network, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for scenario generation, scoring and weak-topic logic, content parsing and progress storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 31. FAMILY PHOTO MEMORIES

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 31. FAMILY PHOTO MEMORIES

## APPLICATION PURPOSE

Build "Family Photo Memories", a Flutter app for viewing family photos with captions and dates. It helps seniors enjoy and revisit memories, and helps families add captions. Target users are senior citizens and their families; main use case: browse albums, see each photo with its caption, names and date, and play a slideshow. Photos stay on the device.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, image_picker (multi-select from the gallery), path_provider, flutter_tts (read captions), image (resize), intl.

## SCREENS

1. Albums – large album cards with a cover photo and count; empty state with a big Add Photos button.
2. Photo Grid – thumbnails in a large grid; tap to open.
3. Photo Viewer – full-screen photo with caption, date and names in large text; Next and Previous large buttons or swipe; pinch to zoom; Read Caption Aloud; Favourite.
4. Add/Edit Photo (family mode) – choose photos, caption, date, people's names, album; validation.
5. Slideshow – automatic advance with the caption, interval choice (5, 10, 20 seconds), pause and resume; no sound required.
6. Favourites – hearted photos.
7. Settings – text size, slideshow interval, caption on or off, family PIN for editing, theme.

## NAVIGATION

Albums > Grid > Viewer; Slideshow from an album or favourites; Add and Settings in a family area. Back returns one level.

## UI/UX

Warm nostalgic but clear style, light, dark and high-contrast. Primary amber-brown #8D6E63, accent teal #00897B, background #FFFBF5. Font Atkinson Hyperlegible (bundled). Large photos, 24sp+ captions, 72dp navigation buttons. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Photos copied into the app folder and compressed; thumbnails cached.
- Captions, dates and names stored per photo; album assignment; sort by date.
- Slideshow timer with pause; read-aloud caption; validation and persistence.

## DATA AND BACKEND

Local sqflite and app-folder images; no cloud, account or social sharing.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for sort and album logic, slideshow sequencing, photo repository and caption validation and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 32. VOICE NOTES POCKET

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 32. VOICE NOTES POCKET

## APPLICATION PURPOSE

Build "Voice Notes Pocket", a Flutter app that records short voice reminders and personal notes. It helps seniors who find typing hard to capture thoughts and reminders. Target users are senior citizens; main use case: press one big button, speak, save, and optionally attach a reminder time.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, record, audioplayers,

path_provider, flutter_local_notifications + timezone, intl.

## SCREENS

1. Notes – list of voice notes with title (or date and time), length and a large Play button; empty state; big Record button.
2. Record – a very large Record and Stop button, a running timer, a level indicator and Save or Discard after stopping; maximum length 3 minutes with a visible countdown.
3. Note Detail – large player with Play, Pause, Back 10 seconds and speed choice (slow, normal), title, optional typed label, reminder time, delete with confirm.
4. Set Reminder – date and time pickers with large controls; repeat none, daily or weekly.
5. Reminder Alert – the notification opens the note ready to play.
6. Settings – maximum length, text size, microphone help, delete all, theme.

## NAVIGATION

Notes is home with a big Record button; Detail from the list. Back returns one level; leaving a recording asks Save or Discard.

## UI/UX

Large simple style, light, dark and high-contrast. Primary blue #1565C0, accent red #D32F2F for recording, background #FFFFFF. Font Atkinson Hyperlegible (bundled). 96dp Record button, recording state by colour, text and icon. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Recording saved to the app folder; metadata in the database; microphone permission explanation and denied-permission handling.
- Playback controls with speed; reminders rescheduled after boot and restart.
- Storage use shown; deletion removes the file; validation and persistence.

## DATA AND BACKEND

Local sqflite, app-folder audio and shared_preferences; recordings never leave the device.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for recording metadata, reminder scheduling, deletion cleanup and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 33. MY APPOINTMENT BOOK

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 33. MY APPOINTMENT BOOK

## APPLICATION PURPOSE

Build "My Appointment Book", a Flutter app that stores doctor visits and other appointments with reminders. It helps seniors remember where to go, when and what to bring. Target users are senior citizens and their carers; main use case: add appointments, get reminders, and prepare questions and notes for each visit.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, url_launcher (dial and open maps by address), share_plus,

table_calendar, intl.

## SCREENS

1. Upcoming – next appointments as large cards with the date, time, place and countdown; empty state with a big Add Appointment button.
2. Add/Edit Appointment – title, type (doctor, dentist, eye check, test, bank, family, other), person or place name, date and time, address text, phone, things to bring, questions to ask, transport arranged, reminders (day before and 2 hours before by default); validation.
3. Appointment Detail – all details, Call, Open in Maps (if an address exists), Share with Family, Mark Done and Add Visit Notes.
4. Calendar – month view with appointment markers; day list.
5. Past Visits – completed appointments with the notes written after the visit; search.
6. Settings – default reminder times, text size, theme.

## NAVIGATION

Bottom tabs Upcoming, Calendar, Past, Settings; floating Add. Back returns one level.

## UI/UX

Clear reassuring style, light, dark and high-contrast. Primary blue #1565C0, accent green #2E7D32, background #F6F9FC. Font Atkinson Hyperlegible (bundled). Large date and time text, 72dp buttons, one task per screen. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Multiple reminders per appointment; reschedule on edit, completion, boot and restart.
- Visit notes and question lists; Share text for family; tap-to-dial and open-in-maps via intents.
- Overlap warning; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no calendar sync, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for reminder times, overlap detection, calendar grouping and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 34. WATER BELL

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 34. WATER BELL

## APPLICATION PURPOSE

Build "Water Bell", a Flutter app that schedules reminders to drink water. It helps seniors who forget to drink through the day. Target users are senior citizens and carers; main use case: set a gentle schedule, tap each time a glass is finished and see the day's count. The goal is chosen by the user; the app gives no medical advice and tells anyone who has been told to limit fluids to follow their doctor's advice.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences,

flutter_local_notifications + timezone, intl.

## SCREENS

1. Today – a large glass visual with the count of glasses and the goal, a huge "I drank a glass" button, next reminder time and a gentle encouragement line.
2. Reminder Setup – wake and sleep times, number of reminders or interval (for example every 2 hours), custom times, goal glasses per day; validation.
3. Alert – the reminder opens a large screen with I Drank and Remind Me Later buttons.
4. History – last 7 and 30 days with glasses per day and a bar chart.
5. Settings – bell sound or vibration only, visual flash alert, glass size label, text size, theme.

## NAVIGATION

Today is home; History and Settings via bottom tabs. Back returns to the tab.

## UI/UX

Fresh gentle style, light, dark and high-contrast. Primary blue #0288D1, accent teal #26C6DA, background #F2FAFD. Font Atkinson Hyperlegible (bundled). Giant drink button (96dp), glass fill animation with a reduced-motion option, count always shown as text. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Reminders scheduled between wake and sleep times; rescheduled after edits, boot and restart; Android 13+ permission handling.
- Tap logging with undo; daily totals; history aggregation; reminders optionally skipped once the goal is reached.
- Validation and persistence.

## DATA AND BACKEND

Local storage only; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for reminder time generation, goal and count logic, history aggregation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 35. GENTLE MOVEMENT GUIDE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 35. GENTLE MOVEMENT GUIDE

## APPLICATION PURPOSE

Build "Gentle Movement Guide", a Flutter app that shows illustrated, gentle movement routines. It gives seniors simple ways to stay active at home. Target users are senior citizens; main use case: pick a short routine and follow each illustrated step at their own pace. The app is not medical advice: it shows a safety notice at first launch, tells users to stop if they feel pain, dizziness or breathlessness, and to ask a health professional first; routines must be reviewed by a qualified physiotherapist before release.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite, flutter_tts (optional spoken cues). Illustrations drawn in Flutter or original art with alt text.

## SCREENS

1. Safety Notice – acknowledged on first launch and reachable later.
2. Home – today's suggested routine, categories, My Routines and a weekly activity log.
3. Routines – Seated Warm-up, Neck and Shoulders, Arms and Hands, Gentle Legs, Balance Holding a Chair, Breathing and Relaxing, each with duration and a "seated" or "standing with support" label.
4. Exercise Card – large illustration, numbered steps, repeat count or seconds, an easier option and a safety tip.
5. Routine Player – one card at a time with a visual countdown, Pause, Previous and Next, rest between exercises and optional spoken cues.
6. Activity Log – optional record of completed routines with a feel-good rating (easy, good, tired).
7. Settings – text size, speech, rest length, theme.

## NAVIGATION

Home > Routine > Player; Log from Home. Back asks to confirm leaving a routine.

## UI/UX

Calm encouraging style, light, dark and high-contrast. Primary green #43A047, accent teal #00ACC1, background #F4FAF4. Font Atkinson Hyperlegible (bundled). Large illustrations with text steps, no flashing, no pressure language. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Exercise JSON (title, steps, reps or seconds, easier option, safety tip, position).
- Routine player with timestamp-based timers; log and weekly summary; acknowledgement stored.

## DATA AND BACKEND

Bundled JSON and local storage; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for routine sequencing, timer logic, log aggregation and acknowledgement gating and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 36. DAILY BRAIN GYM

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 36. DAILY BRAIN GYM

## APPLICATION PURPOSE

Build "Daily Brain Gym", a Flutter app with easy word, number and memory games. It gives seniors a pleasant daily mental activity. Target users are senior citizens; main use case: play a short daily set of games at a relaxed pace. The app makes no medical claims about memory or health.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, flutter_tts (optional),

fl_chart.

## SCREENS

1. Home – today's set of three games, streak and a Play button; all-done state.
2. Word Games – Find the Missing Letter, Unscramble the Word (with a picture clue), Word Search (small grid).
3. Number Games – Easy Sums, Number Sequence, Which Number Is Bigger.
4. Memory Games – Match the Pairs, What Was Missing (remember objects), Repeat the Pattern.
5. Game Result – friendly summary, stars and Play Again.
6. Progress – days played, games played and a gentle weekly chart.
7. Settings – difficulty (very easy, easy, medium), sound, text size, show hints, theme.

## NAVIGATION

Home > Game > Result > Home; Word, Number and Memory sections from Home. Back confirms leaving a game.

## UI/UX

Bright friendly style, light, dark and high-contrast. Primary orange #FB8C00, accent blue #1E88E5, background #FFF9F2. Font Atkinson Hyperlegible (bundled). Large tiles (72dp+), clear instructions, no timers by default, no failure sounds. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Word list and puzzle generators with guaranteed solutions; number question generators by difficulty.
- Daily set picks one game from each type, avoiding repeats; scoring is encouraging; hints available.
- Streak and progress saved; validation and persistence.

## DATA AND BACKEND

Local sqflite or shared_preferences with bundled word lists; no ads, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for puzzle solvability, daily set selection, scoring and progress storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 37. LARGE TEXT READER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 37. LARGE TEXT READER

## APPLICATION PURPOSE

Build "Large Text Reader", a Flutter app that shows saved text in adjustable, extra-large fonts. It helps seniors with low vision read letters, notes and instructions comfortably. Target users are senior citizens and families who add the text; main use case: save a text and read it at a comfortable size, with optional read-aloud.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, flutter_tts, file_picker (import .txt), share_plus.

## SCREENS

1. Library – saved texts as large cards with title and the first lines; empty state with a big Add Text button.
2. Add/Edit Text – title, paste or type, or import a .txt file; validation; delete with confirm.
3. Reader – the text in extra-large type with big A+ and A- buttons, a Read Aloud button, line spacing and contrast choices; scroll position remembered.
4. Reading Settings – font size from 24sp to 80sp with a live preview, line spacing, font (Atkinson Hyperlegible or a serif), theme (black on white, white on black, yellow on black).
5. Settings – default reading style, speech speed, theme.

## NAVIGATION

Library > Reader > Reading Settings. Back returns one level.

## UI/UX

Extra-large simple style, light, dark and high-contrast. Primary slate #37474F, accent amber #FFB300, background follows the reading theme. Font Atkinson Hyperlegible (bundled). Controls with text labels, 72dp buttons, no clutter. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Settings apply instantly and persist per user; text stored with title and date.
- Read aloud with sentence highlighting, pause and resume.
- Text import with size limits and encoding handling; share text.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for settings persistence, text import limits, sentence splitting for read-aloud and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 38. MY IMPORTANT NUMBERS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 38. MY IMPORTANT NUMBERS

## APPLICATION PURPOSE

Build "My Important Numbers", a Flutter app that keeps important contacts and reference numbers in one place. It helps seniors and families find phone numbers and service references quickly. Target users are senior citizens and carers; main use case: save doctors, family, services and utility reference numbers and call them in one tap. Privacy rule: the app warns users not to store bank card numbers, PINs, passwords or government ID numbers, and flags long digit patterns that look like them.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, flutter_secure_storage (database key), local_auth (optional lock), url_launcher (dialer), pdf and printing (large-print list), share_plus, intl.

## SCREENS

1. Numbers – grouped list (Family, Doctors and Hospitals, Services such as gas, electricity and water, Neighbours, Other) with large Call buttons; search; empty state.
2. Add/Edit Entry – name, category, phone number, optional reference label and number (for example "Gas consumer number"), notes; validation and the warning for sensitive-looking numbers.
3. Entry Detail – large text, Call, Copy and Share, edit and delete with confirm.
4. Large-Print List – a preview and PDF export of selected entries in very large type for printing and keeping by the phone.
5. Lock Setup – optional biometric or device-credential lock.
6. Settings – text size, groups, theme.

## NAVIGATION

Numbers is home with floating Add; Detail, Print and Settings from there. Back returns one level.

## UI/UX

Clear large style, light, dark and high-contrast. Primary blue #1565C0, accent green #2E7D32, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Call buttons 72dp, group headers with icons and text. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Contact and reference CRUD with search and grouping.
- Pattern warning for 12-digit and 13-19 digit numbers or words like PIN and password in notes; the user can proceed only after reading the warning.
- PDF generation of the large-print list; optional lock; validation and persistence.

## DATA AND BACKEND

Local sqflite with a key in secure storage; no cloud, account or analytics.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for sensitive-pattern detection, search and grouping, PDF content generation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 39. HOUSEHOLD REMINDER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 39. HOUSEHOLD REMINDER

## APPLICATION PURPOSE

Build "Household Reminder", a Flutter app that reminds users about bills, chores and important dates. It helps seniors keep the home running smoothly. Target users are senior citizens and carers; main use case: add reminders once and tick them off when done.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, table_calendar, intl. Reminders must be rescheduled after reboot.

## SCREENS

1. Today – reminders due today and overdue as large cards with a Done button; the next few days below; empty state with a friendly message.
2. Add Reminder – a simple three-step flow: what (type: bill, chore, date, other, with title), when (date and time, repeat), and how to be reminded; validation and a final summary.
3. All Reminders – list grouped by type with filters; edit, pause and delete with confirm.
4. Calendar – month view with markers; day list.
5. Bill Details – optional amount and payee note on bill reminders and a Mark Paid history.
6. Settings – default reminder time, snooze length, sound or vibration, text size, theme.

## NAVIGATION

Bottom tabs Today, Calendar, All, Settings; floating Add. Back returns one level.

## UI/UX

Clear warm style, light, dark and high-contrast. Primary teal #00897B, accent orange #FB8C00, background #F5FAF9. Font Atkinson Hyperlegible (bundled). 72dp buttons, large cards, icons with text. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Recurrence (daily, weekly, monthly, yearly, custom) generating the next occurrence on completion.
- Overdue detection; snooze from the notification; reminders rescheduled on edit, boot and restart.
- Bill payment history; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for recurrence next-date rules, overdue detection, reminder scheduling and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 40. SIMPLE UPI TUTOR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 40. SIMPLE UPI TUTOR

## APPLICATION PURPOSE

Build "Simple UPI Tutor", a Flutter app that explains QR payments, PIN safety and common payment steps through practice on a mock payment screen. It helps seniors feel confident and safe with digital payments. Target users are senior citizens and families; main use case: learn each step slowly and practise on a clearly marked simulation. The app never connects to UPI, a bank or any real payment; every practice screen shows a banner "Practice only - no real money".

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts (optional). Practice screens built from Flutter widgets (no real payment SDK, camera or QR scanning needed).

## SCREENS

1. Home – lessons, practice, safety rules, progress.
2. Lessons – What Is UPI, Pay by Scanning a QR Code, Pay to a Phone Number, Check That Money Was Paid, Receive Money (you never enter your PIN to receive), Check Your Balance Safely, What to Do If a Payment Fails.
3. Lesson – numbered steps with large illustrations, Read Aloud and a "Try it" button.
4. Practice Payment – a mock app with a pretend QR scan, a pretend amount and a pretend PIN pad (any number accepted, never stored); guided prompts tell the user what to tap next and what to check.
5. PIN Safety – clear rules: never share your PIN, OTP or screen; a collect request that asks you to pay is not receiving money; bank staff never ask for your PIN.
6. Quiz – sample situations with a Safe or Not Safe choice and explanations.
7. Progress – lessons done and quiz scores.
8. Settings – text size, speech, theme.

## NAVIGATION

Home > Lessons > Practice > Quiz; PIN Safety from Home. Back returns one level; the practice banner is always visible.

## UI/UX

Reassuring clear style, light, dark and high-contrast. Primary indigo #3949AB, accent green #2E7D32, banner amber #FFA000, background #F6F7FC. Font Atkinson Hyperlegible (bundled). Large buttons, one step per screen, a very clear "Practice only" banner. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Lesson JSON reviewed by the team; practice flow state machine that checks steps in order and explains mistakes kindly.
- The mock PIN is never saved or logged; quiz scoring and progress persistence.

## DATA AND BACKEND

Bundled JSON and local progress; no payment, bank, account or cloud integration. State clearly that all payments are simulated.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for practice step sequencing, quiz scoring, PIN non-persistence and progress storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 41. GROCERY VOICE LIST

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 41. GROCERY VOICE LIST

## APPLICATION PURPOSE

Build "Grocery Voice List", a Flutter app for creating shopping lists using voice input where supported. It helps seniors who find typing hard make and use grocery lists. Target users are senior citizens and families; main use case: say items aloud to add them, tick them off in the shop and have the list read back. Where speech recognition is not supported or fails, typing works.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, speech_to_text (device speech service, which may need a network), flutter_tts, share_plus.

## SCREENS

1. List – current list in large type with tick boxes; a very large Speak button and a Type button; empty state with instructions.
2. Voice Add – listening screen showing the heard words live; the user confirms and the heard phrase is split into items ("milk, bread and two kilos of rice") with the chance to edit before adding.
3. Add by Typing – a simple text field with quick-add suggestions from past items.
4. Read My List – the list read aloud item by item.
5. Past Lists & Favourites – frequently bought items to add in one tap; saved lists to reuse.
6. Share List – send as text to family.
7. Settings – speech language, text size, voice speed, theme.

## NAVIGATION

List is home; Past Lists, Favourites and Settings via tabs. Back returns one level.

## UI/UX

Large simple style, light, dark and high-contrast. Primary green #43A047, accent orange #FB8C00, background #FFFFFF. Font Atkinson Hyperlegible (bundled). 96dp Speak button, items at least 24sp, ticked items struck through with a tick icon. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Speech result parsed into items by separators and quantities; confirm and edit step.
- Tick, remove and reorder; clear completed; favourites and history suggestions.
- Handle microphone permission, no speech service and offline cases with plain messages; persistence.

## DATA AND BACKEND

Local sqflite or shared_preferences; no account or cloud. Say clearly that speech recognition may use the device's speech service.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for phrase-to-items parsing, favourites suggestions, list operations and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 42. MY SPENDING BOOK

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 42. MY SPENDING BOOK

## APPLICATION PURPOSE

Build "My Spending Book", a Flutter app that records cash expenses with simple categories. It helps seniors keep track of everyday spending. Target users are senior citizens and families; main use case: write down each spend in a few taps and see the month's totals. Amounts are in Indian rupees (Rs).

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl, share_plus.

## SCREENS

1. Today – today's spending total, a big Add Spend button, and today's entries; empty state.
2. Add Spend – a large number pad for the amount, category buttons with icons (Groceries, Medicine, Transport, Household, Gifts, Temple or Charity, Other), optional note and date; validation.
3. This Month – total spent, a simple bar for each category and an optional monthly budget with a remaining amount.
4. All Entries – list by date with edit and delete (confirm); search by note.
5. Share Summary – the month's totals as text for family.
6. Settings – monthly budget, categories, text size, theme.

## NAVIGATION

Bottom tabs Today, Month, Entries, Settings; Add as a floating button. Back returns one level.

## UI/UX

Simple notebook style, light, dark and high-contrast. Primary green #2E7D32, accent amber #FFA000, background #FAF8F2. Font Atkinson Hyperlegible (bundled). Big digits, 72dp number keys, category icons with text. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Totals per day, month and category; budget remaining with a gentle warning at 80% and 100%.
- Undo after delete; edit past entries; search; share summary.
- Validation and persistence; money stored in whole rupees and paise.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank link, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for totals by period and category, budget warnings, undo logic and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 43. DAILY WELLNESS JOURNAL

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 43. DAILY WELLNESS JOURNAL

## APPLICATION PURPOSE

Build "Daily Wellness Journal", a Flutter app for recording mood, sleep and general wellbeing notes. It helps seniors notice how they feel over time and share notes with family or a doctor if they choose. Target users are senior citizens; main use case: spend one minute each day choosing mood, sleep and a few notes. The app is a diary, not a medical tool: it does not diagnose or advise, and it tells users to talk to a doctor about health concerns.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite with a key in flutter_secure_storage, local_auth (optional lock), flutter_local_notifications + timezone, fl_chart, share_plus, intl.

## SCREENS

1. Today – a gentle "How are you today?" card with big mood faces, a sleep question (hours and how rested), energy and appetite choices, optional note; Save; edit later.
2. Add Note – free text or an optional voice note typed by dictation.
3. Calendar – month view with the mood face for each logged day.
4. Trends – simple charts of mood and sleep over 7 and 30 days using only the user's entries.
5. Share Summary – choose a range and share the entries as text, with a preview.
6. Reminder – an optional daily nudge with a neutral message.
7. Settings – lock, reminder time, text size, theme, export, delete all with confirm.

## NAVIGATION

Bottom tabs Today, Calendar, Trends, Settings. Back returns one level; the lock screen appears first if enabled.

## UI/UX

Soft gentle style, light, dark and high-contrast. Primary soft teal #4DB6AC, accent peach #FFAB91, background #F6FBFA. Font Atkinson Hyperlegible (bundled). Big faces with text labels, no judgmental colours (no red for low days). Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- One entry per day with edit; averages and trends from entries only.
- Encrypted local storage; lock gating; share and export under user control.
- Reminder scheduling; validation and persistence.

## DATA AND BACKEND

Local encrypted storage only; no cloud, account or analytics; never log entries.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for entry repository, averages and trends, lock gating and share-text generation and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 44. HEARING-FRIENDLY ALERTS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 44. HEARING-FRIENDLY ALERTS

## APPLICATION PURPOSE

Build "Hearing-Friendly Alerts", a Flutter app that gives reminders using visual alerts and adjustable vibration. It helps seniors with hearing loss notice reminders without relying on sound. Target users are senior citizens with hearing difficulty and carers; main use case: create reminders and choose strong visual and vibration alerts. Vibration strength control depends on device support and the app says so.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences,

flutter_local_notifications + timezone, vibration, optional torch_light (slow camera-light pulses),

wakelock_plus.

## SCREENS

1. Reminders – list with time, repeat and alert style; empty state; Add Reminder.
2. Add/Edit Reminder – title, date and time, repeat (none, daily, weekly), alert style (full-screen colour alert, banner, vibration only, with light pulses), vibration pattern; validation.
3. Alert Screen – a full-screen, high-contrast message with the reminder title in giant text, Done and Remind Me Later buttons, and slow gentle colour pulsing (never more than 2 pulses per second).
4. Style Settings – choose alert colours and size, vibration pattern (short, long, strong, repeated) and intensity where supported, with a Test Alert button.
5. History – recent alerts and whether they were answered.
6. Settings – default style, snooze length, light pulses on or off with a warning for flicker sensitivity, text size, theme.

## NAVIGATION

Bottom tabs Reminders, Style, History, Settings; floating Add. Back returns one level.

## UI/UX

Bold clear style, light, dark and high-contrast. Primary orange #FF6F00, accent blue #1565C0, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Giant text, strong contrast, no reliance on sound, reduced-motion option that replaces pulsing with a static colour. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Reminders scheduled with high-priority notifications and full-screen intents; rescheduled after boot and restart.
- Vibration patterns generated from the chosen style; amplitude used only when the device supports it, otherwise duration and repeats.
- Pulse limit enforced at no more than 2 per second; answered tracking and snooze; validation and persistence.

## DATA AND BACKEND

Local storage only; no account or cloud. Test alerts and vibration on a physical device.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for pattern generation, pulse-rate limit, reminder scheduling and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 45. MY WALK LOG

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 45. MY WALK LOG

## APPLICATION PURPOSE

Build "My Walk Log", a Flutter app that records walking duration and personal walking goals. It helps seniors who like to walk keep a simple record and stay encouraged. Target users are senior citizens; main use case: start a timer when walking, stop it after, and see progress toward a weekly goal. Goals are chosen by the user; the app gives no medical advice and tells users to check with a doctor about activity levels.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, fl_chart,

flutter_local_notifications + timezone (optional reminder), wakelock_plus (optional), intl. No GPS

needed.

## SCREENS

1. Today – a big Start Walk button, today's minutes, the week's progress toward the goal and the current streak.
2. Walk Timer – a large elapsed time with Pause and Stop; the timer continues in the background; Save with a "how did it feel" choice (easy, comfortable, tiring) and an optional note.
3. Add Walk Manually – date, minutes and an optional note.
4. Goals – set a daily minutes target and weekly total; gentle messages as the user nears or reaches it.
5. History – list of walks with edit and delete (confirm); weekly and monthly totals and bar chart.
6. Settings – reminder time, goal values, text size, theme.

## NAVIGATION

Bottom tabs Today, History, Goals, Settings. Back returns one level; leaving a running walk keeps it running.

## UI/UX

Cheerful outdoors style, light, dark and high-contrast. Primary green #43A047, accent blue #29B6F6, background #F4FAF4. Font Atkinson Hyperlegible (bundled). Huge Start button, large numbers, progress as bar and text. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Timer based on start and end timestamps so it stays correct when the screen locks.
- Walk records, totals by day, week and month; goal progress; streak counted on days meeting the daily target.
- Validation (1 to 600 minutes) and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no location tracking, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for timer duration from timestamps, goal and streak logic, aggregation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 46. HOME SAFETY CHECKER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 46. HOME SAFETY CHECKER

## APPLICATION PURPOSE

Build "Home Safety Checker", a Flutter app with a checklist for gas, electrical, kitchen and fall hazards. It helps seniors and families spot and fix risks at home. Target users are senior citizens and family members; main use case: walk through the home with the checklist, note problems and track what has been fixed. The checklist is general guidance and not a professional inspection, and it tells users to call a qualified electrician or gas supplier for any fault.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, share_plus, url_launcher (dialer), intl.

## SCREENS

1. Home – the latest check with a safety score as a simple count (items fine, items to fix), a Start Check button and open to-do items; empty state.
2. Check Areas – Gas and Cooking, Electrical, Kitchen, Bathroom, Bedroom, Stairs and Floors, Lighting, Fire Safety, Medicines Storage.
3. Area Checklist – questions with Yes, No and Not Applicable (for example "Is the gas switched off at the regulator at night?", "Are cables free from damage?", "Are rugs fixed or removed?", "Is there a night light on the way to the bathroom?") with a short "why this matters" line.
4. To-Do List – items answered No become fix tasks with priority, who will help, due date and status; tap-to-call saved helpers such as an electrician.
5. Tips – short illustrated safety tips.
6. Recheck Reminder – a monthly nudge.
7. Settings – helpers' phone numbers, reminder, text size, theme.

## NAVIGATION

Bottom tabs Home, To-Do, Tips, Settings; Start Check opens areas. Back returns one level.

## UI/UX

Clear safety style, light, dark and high-contrast. Primary orange #EF6C00, accent teal #00796B, background #FFF9F2. Font Atkinson Hyperlegible (bundled). Big Yes and No buttons with text, icons for each area. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Checklist JSON (about 50 items) reviewed by the team; answers saved per check date.
- Fix tasks generated automatically from No answers; completion tracking; comparison with the previous check.
- Reminders; share the to-do list with family as text; validation and persistence.

## DATA AND BACKEND

Bundled JSON, local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for task generation from answers, comparison with the previous check, reminder scheduling and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 47. PRESCRIPTION ORGANIZER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 47. PRESCRIPTION ORGANIZER

## APPLICATION PURPOSE

Build "Prescription Organizer", a Flutter app that stores prescription photos and medicine information. It helps seniors and carers keep prescriptions, doctor details and medicine notes together. Target users are senior citizens and carers; main use case: photograph a prescription, record the medicines as written and find it at the next visit. The app gives no medical advice and does not check doses or interactions; information is entered as shown on the prescription, and photos stay on the device behind an optional lock.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite with a key in flutter_secure_storage, local_auth (optional lock), image_picker (camera or gallery), path_provider, image (compress), flutter_local_notifications + timezone, share_plus, intl.

## SCREENS

1. Prescriptions – list by date with doctor, thumbnail and number of medicines; search; empty state; Add Prescription.
2. Add/Edit Prescription – photo or photos, date, doctor and clinic, condition note (optional, user-typed), medicines list (name, strength, how to take as written, duration), refill date, notes; validation.
3. Prescription Detail – zoomable photo, medicines, refill reminder, share with family or doctor as text or image, delete with confirm.
4. Medicines – a combined list of current medicines across prescriptions with search.
5. Doctors – saved doctors with phone and clinic and tap-to-dial.
6. Refills – upcoming refill dates with reminders.
7. Settings – lock, auto-lock, refill reminder lead time, block screenshots, text size, theme, delete all.

## NAVIGATION

Bottom tabs Prescriptions, Medicines, Refills, Settings; floating Add. The lock screen appears first if enabled. Back returns one level.

## UI/UX

Clean trustworthy style, light, dark and high-contrast. Primary blue #1565C0, accent teal #00897B, background #F6F9FC. Font Atkinson Hyperlegible (bundled). Large photo previews, plain labels. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Photos compressed into the app folder; metadata in the encrypted database.
- Current medicine list built from prescriptions that are still within their duration; search; refill reminders rescheduled after boot and restart.
- Lock gating; sharing only when the user chooses; validation and persistence.

## DATA AND BACKEND

Local encrypted database and app-folder photos; no cloud, OCR service, account or analytics.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for current-medicine derivation, refill reminders, lock gating and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 48. FESTIVAL & BIRTHDAY CALENDAR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 48. FESTIVAL & BIRTHDAY CALENDAR

## APPLICATION PURPOSE

Build "Festival & Birthday Calendar", a Flutter app that keeps track of birthdays, festivals and family occasions. It helps seniors remember to greet and celebrate. Target users are senior citizens and families; main use case: see upcoming occasions, get reminders and send wishes in one tap. Assumption: many festival dates follow lunar or regional calendars, so the user enters festival dates and the team may include a sample list for the current year only after verifying it from an authoritative calendar.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, url_launcher (dialer and SMS composer), table_calendar, intl.

## SCREENS

1. Upcoming – the next occasions as large cards with the name, the date, days to go and age or years (for birthdays and anniversaries); empty state with a big Add button.
2. Add/Edit Occasion – type (Birthday, Anniversary, Festival, Family Event, Other), name, date (with optional year), repeat yearly, phone number, reminder days before and on the day; validation.
3. Occasion Detail – details with Call, Send Wishes and Edit; Send Wishes opens the SMS composer with a prepared greeting the user can change.
4. Calendar – month view with markers.
5. Festivals – the user's festival list and, if provided, the verified sample list with Add to My Calendar.
6. Greetings – a small list of editable greeting messages by occasion.
7. Settings – default reminders, reminder time, greeting templates, text size, theme.

## NAVIGATION

Bottom tabs Upcoming, Calendar, Festivals, Settings; floating Add. Back returns one level.

## UI/UX

Warm festive style, light, dark and high-contrast. Primary magenta #AD1457, accent gold #FFB300, background #FFF8F3. Font Atkinson Hyperlegible (bundled). Large cards, icons with text, never colour alone. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Yearly recurrence with leap-day handling; days-to-go and age calculation.
- Reminders on the day and before; rescheduled after edits, boot and restart.
- Prepared greeting messages; tap-to-call; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud; festival dates are user-entered or from a verified bundled list.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for yearly recurrence and leap days, age calculation, reminder dates and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 49. VOICE READING HELPER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 49. VOICE READING HELPER

## APPLICATION PURPOSE

Build "Voice Reading Helper", a Flutter app that reads entered text aloud using the device's text-to-speech. It helps seniors who find reading small print tiring. Target users are senior citizens and families; main use case: paste or type any text, such as a letter or message, and listen to it with clear controls.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, flutter_tts, share_plus,

file_picker (optional .txt import).

## SCREENS

1. Reader – a large text box and a giant Listen button, with Pause, Stop, Slower and Faster controls; the current sentence highlighted in large type as it is spoken.
2. Paste or Type – paste from the clipboard with one tap, type, or import a text file; Clear.
3. Saved Texts – titles and previews of texts saved for later; open and delete with confirm.
4. Voice Settings – language, voice choice, speed, pitch and volume, with a Test button.
5. Display Settings – text size from 24sp to 72sp, contrast theme and line spacing.
6. Help – what to do if no voice is installed or the volume is low.

## NAVIGATION

Reader is home; tabs Saved, Voice and Display. Back returns one level.

## UI/UX

Large simple style, light, dark and high-contrast. Primary blue #1565C0, accent orange #FB8C00, background #FFFFFF. Font Atkinson Hyperlegible (bundled). 96dp Listen button, clear icons with text labels. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Text split into sentences and spoken one by one so pause and resume are accurate and highlighting follows.
- Handles long text by chunking; no-voice and silent-volume cases explained.
- Saved texts and voice settings persist; validation of empty text.

## DATA AND BACKEND

Local storage only; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for sentence splitting and chunking, pause and resume position, settings persistence and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 50. MY DOCUMENTS GUIDE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 50. MY DOCUMENTS GUIDE

## APPLICATION PURPOSE

Build "My Documents Guide", a Flutter app with a checklist for organising important personal documents. It helps seniors and families know which papers exist, where they are kept and who knows about them. Target users are senior citizens and their families; main use case: tick off each document type, note where the original is kept and share the list with a trusted family member. Privacy rule: the app records only whether a document exists, where it is kept and who has been told - never document numbers or scans.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, local_auth (optional lock),

flutter_local_notifications + timezone, pdf and printing, share_plus, intl.

## SCREENS

1. Home – a progress summary (for example 12 of 20 documents located), the next suggested step and a Start button.
2. Checklist – groups with ticks: Identity, Home and Property, Money and Banking, Insurance, Health, Pension and Retirement, Family and Legal (such as will and nominee details), each with a short "why this matters" line.
3. Document Entry – Have It, Need to Find It or Not Applicable; where the original is kept; where a copy is kept; who knows where it is; expiry or review date; notes; warning not to enter numbers.
4. Family Sharing – choose what to include and share the checklist as text or a PDF with only locations and names, never numbers.
5. Review Reminders – a yearly reminder to check documents and any expiry dates.
6. Organising Tips – short guidance on folders, copies and safe places.
7. Settings – optional lock, reminder, text size, theme.

## NAVIGATION

Bottom tabs Home, Checklist, Tips, Settings. Back returns one level; the lock screen appears first if enabled.

## UI/UX

Calm organised style, light, dark and high-contrast. Primary navy #283593, accent teal #00ACC1, background #F5F7FB. Font Atkinson Hyperlegible (bundled). Large tick boxes with text status, grouped lists with icons. Senior-friendly: default text 20sp or larger and scalable, buttons 64dp or larger, high contrast, plain language, one main action per screen, confirmation before deleting, no time limits, no swipe-only actions, no ads or pop-ups, and easy for a family member to set up.

## FUNCTIONALITY

- Checklist JSON reviewed by the team and customisable with the user's own items.
- Progress counts; expiry and review reminders rescheduled after boot and restart.
- PDF and text export of locations only; optional lock; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no scans, numbers, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for progress counts, reminder dates, export content with no numbers and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---
