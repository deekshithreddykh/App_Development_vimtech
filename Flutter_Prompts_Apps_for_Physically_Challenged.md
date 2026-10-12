# Flutter Prompts - Apps for Physically Challenged Persons

One standalone prompt per page. Give each team only its own page.

Each prompt below is in its own box. Use the copy button on the box to copy just that prompt.

101. SPEAKEASY BOARD
102. QUICKPHRASE VOICE
103. ACCESSTRIP PLANNER
104. SIGNSTEPS
105. MYWAY ROUTINE
106. ONE-TOUCH EMERGENCY
107. SCREEN READER PRACTICE
108. EASYREAD MODE
109. CAPTION NOTES
110. ACCESSIBLE KEYBOARD PRACTICE
111. MOBILITY EQUIPMENT LOG
112. CHAIR EXERCISE CARDS
113. ACCESSIBLE HOME CHECKLIST
114. VISUAL DAILY TIMER
115. FOCUS-FRIENDLY TASKS
116. GESTURE LEARNING CARDS
117. PERSONAL ASSISTANCE CARD
118. MEDICAL INFORMATION CARD
119. ACCESSIBLE JOB SKILLS
120. INCLUSIVE LEARNING QUIZ
121. COLOR CONTRAST CHECKER
122. VOICE-CONTROL PRACTICE
123. DAILY INDEPENDENCE TRACKER
124. PUBLIC FACILITY CHECKLIST
125. EASY FORM ASSISTANT

---

## 101. SPEAKEASY BOARD

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 101. SPEAKEASY BOARD

## APPLICATION PURPOSE

Build "SpeakEasy Board", a Flutter communication-board app where the user taps picture or phrase buttons to communicate common needs and feelings aloud. It helps people who find speaking difficult or tiring to express themselves quickly. Target users are people with speech difficulties and their carers; main use case: tap tiles to speak a need ("I need water") or build a sentence from several tiles. Assumption: the source description is cut off; the board covers common needs, feelings, people and places.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, flutter_tts, image_picker

(optional own photos, stored locally), path_provider.

## SCREENS

1. Board – grid of large picture tiles with labels; sentence bar at the top; Speak, Backspace and Clear buttons; category tabs (Quick, Needs, Feelings, People, Food, Places, Actions).
2. Edit Board – unlocked by a long-press on the Edit button; add, edit, delete and drag-reorder tiles and categories.
3. Add/Edit Tile – label, spoken text, icon, emoji or own photo, colour, category; validation.
4. Favourites – pinned quick tiles (Yes, No, Help, Thank you, Stop).
5. Settings – grid size (2x2 to 5x5), tile size, voice, speech rate and pitch, speak on tap or add to sentence, hold-to-select delay, contrast theme.

## NAVIGATION

Board is home; Edit Board and Settings from the app bar. Back returns one level; edit changes confirm before discarding.

## UI/UX

Clear symbol-board style, light, dark and high-contrast themes. Primary blue #1565C0, accent amber #FFB300, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Category colours with text labels, tiles at least 72dp, minimal animation. Reusable PictureTile, SentenceBar, CategoryTab. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Tiles speak their spoken text through device text-to-speech; the sentence bar joins tiles and speaks them together.
- Optional hold-to-select delay (0-2 s) prevents accidental taps.
- Default board of about 60 tiles in JSON; user tiles and photos persist on the device.
- Missing TTS engine handled with a clear message and install guidance.

## DATA AND BACKEND

Local sqflite, shared_preferences and app-folder images; no account, cloud or analytics; photos never leave the device.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for sentence composition, tile and category repository, reordering and the hold-to-select logic and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 102. QUICKPHRASE VOICE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 102. QUICKPHRASE VOICE

## APPLICATION PURPOSE

Build "QuickPhrase Voice", a Flutter app that turns typed messages into speech using the phone's built-in text-to-speech. It helps people who cannot or prefer not to speak aloud to communicate in person. Target users are people with speech or hearing-related communication barriers; main use case: type a message, press Speak, or reuse a saved phrase.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, flutter_tts.

## SCREENS

1. Speak – large text box, big Speak and Stop buttons, Clear, recently spoken list; a Show Text button that displays the message in very large type to hand the phone to someone.
2. Saved Phrases – categorised list with pin, search, add, edit and delete; tap to speak.
3. History – recent messages; tap to speak again or save as a phrase; clear history with confirm.
4. Voice Settings – voice, language, speech rate, pitch, volume; Test voice button.
5. Settings – text size, theme (including high contrast), speak on Enter, auto-clear after speaking, history limit.

## NAVIGATION

Bottom tabs Speak, Phrases, History, Settings. Back from nested screens returns to the tab.

## UI/UX

Minimal communication style, light, dark and high-contrast themes. Primary teal #00796B, accent orange #FF7043, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Speak button at least 64dp, large input text, minimal clutter. Reusable PhraseTile, SpeakButton, BigTextView. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Speak, pause and stop via TTS with queueing; voice and language selection from installed voices.
- Phrase CRUD, pins and categories; history trimmed to a chosen limit.
- Show Text mode in landscape or portrait with auto-fit font size.
- No TTS voice installed or silent device volume detected and explained.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account, cloud or analytics.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for history limiting, phrase repository, search and the speak-queue behaviour and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 103. ACCESSTRIP PLANNER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 103. ACCESSTRIP PLANNER

## APPLICATION PURPOSE

Build "AccessTrip Planner", a Flutter app for preparing trip checklists covering ramps, lifts, transport arrangements and accessibility needs. It solves the problem of discovering access barriers only on arrival. Target users are travellers with mobility needs and their companions; main use case: create a trip, work through accessibility checklists and keep key contacts and notes together. Assumption: the source description is cut off; all information is entered by the user, and the app tells users to confirm details directly with providers.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, url_launcher (open the dialer), share_plus, flutter_local_notifications + timezone, intl.

## SCREENS

1. Trips – upcoming and past trips with checklist progress; empty state; New Trip.
2. New/Edit Trip – destination, dates, travellers, notes; template choice; validation.
3. Trip Checklist – sections Transport (accessible vehicle, boarding ramp or lift, assistance booked), Accommodation (step-free entrance, lift size, accessible bathroom, bed height), Venues, Equipment (charger, spares, repair kit) with tick, N/A and note per item; progress bar.
4. Add/Edit Item – title, section, notes, due date, reminder; validation.
5. Contacts & Notes – hotel, transport provider and emergency contacts with tap-to-dial; free notes.
6. Templates – default and custom checklists.
7. Settings – text size, theme, reminder time.

## NAVIGATION

Trips > Trip (tabs Checklist, Contacts, Notes) > Item; Templates and Settings from Trips. Back returns one level.

## UI/UX

Calm travel style, light, dark and high-contrast. Primary blue #0277BD, accent green #2E7D32, background #F5F9FC. Font Atkinson Hyperlegible (bundled). Large checkboxes, progress by text and bar. Reusable ChecklistTile, SectionHeader, ContactCard. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Trips from templates; per-section and overall progress; reminders for dated items.
- Tap-to-dial contacts via the dialer (no calls placed automatically).
- Share the checklist as plain text.
- Validation of dates; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no maps, booking APIs, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for template creation, progress calculation, reminder scheduling logic and the trip repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 104. SIGNSTEPS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 104. SIGNSTEPS

## APPLICATION PURPOSE

Build "SignSteps", a Flutter app for learning basic sign language with illustrated cards and short quizzes. It promotes communication and inclusion. Target users are learners of all ages and families; main use case: study a category of signs, then practise with quizzes. Assumption: the team chooses ONE sign language (American Sign Language by default) and states it in the app. Accuracy rule: never invent signs; use properly licensed sources reviewed by a qualified signer or Deaf community member, and mark unreviewed content as draft.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional audioplayers. Team-supplied openly licensed images or short GIFs credited in CREDITS.md.

## SCREENS

1. Home – categories (Alphabet, Numbers, Greetings, Everyday Words, Feelings), Quiz, Progress, About.
2. Category List – grid of sign cards with picture and word; search.
3. Sign Card – large illustration or GIF, English word, written description of handshape, location and movement, Flip, I Know It and Practise Again.
4. Quiz – "Which word is this sign?" and "Which sign means...?" with 3-4 choices; 10 questions; results.
5. Match Game – match 4 signs to words.
6. Progress – signs known per category, quiz bests, badges.
7. About & Credits – sign language used, review note, licences, a note that sign languages differ by country.

## NAVIGATION

Home > Category > Cards (swipe); Home > Quiz/Match > Result. Back returns one level.

## UI/UX

Inclusive high-contrast style, light and dark. Primary deep blue #1565C0, accent yellow #FFC107, background #F5F9FF. Font Atkinson Hyperlegible (bundled). Illustrations at least half the screen height, alt text on every image, no sound required. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Sign JSON (word, asset, description, source, licence, review status).
- Flip cards, known tracking, search, unambiguous quiz and match generators.
- Placeholder for missing assets; no camera recognition and no claim to grade signing.

## DATA AND BACKEND

Bundled JSON and assets with shared_preferences progress; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for quiz generation, known tracking, search and content parsing and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 105. MYWAY ROUTINE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 105. MYWAY ROUTINE

## APPLICATION PURPOSE

Build "MyWay Routine", a Flutter app that organises daily activities with customisable reminders and easy-to-use controls. It helps people who benefit from structure to follow their day with less effort. Target users are people with physical or cognitive access needs and their carers; main use case: set up a daily routine once and get clear, adjustable reminders. Assumption: the source description is cut off after "easy-to-".

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, vibration or HapticFeedback.

## SCREENS

1. Today – timeline of activities as large cards with icon, time and Done and Snooze buttons; progress summary; empty state.
2. Add/Edit Activity – title, icon, time, days of the week, notes, reminder style (sound, vibration, visual only), snooze minutes; validation.
3. Reminder Screen – full-screen alert with large Done and Later buttons and the activity icon.
4. Week – overview of each day's routine; copy a day to another day.
5. Templates – morning, meals, exercise, evening routines to start from.
6. Settings – button size, text size, default reminder style, theme, reset.

## NAVIGATION

Bottom tabs Today, Week, Templates, Settings; floating Add. Back returns one level.

## UI/UX

Calm, uncluttered style, light, dark and high-contrast. Primary blue #3F6AB5, accent green #43A047, background #F7F9FC. Font Atkinson Hyperlegible (bundled). Big icons with labels, 72dp action buttons, one-handed layout. Reusable ActivityCard, BigActionButton, TimelineRow. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Repeating schedules by weekday; reminders rescheduled after edit, boot and restart.
- Done and Snooze actions available from the notification; completion log per day.
- Copy day, template import; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for schedule generation by weekday, snooze logic, completion log and reminder scheduling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 106. ONE-TOUCH EMERGENCY

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 106. ONE-TOUCH EMERGENCY

## APPLICATION PURPOSE

Build "One-Touch Emergency", a Flutter app that opens emergency contact and assistance options quickly. It solves the problem of fumbling through menus in a stressful moment. Target users are people with mobility or dexterity difficulties and their families; main use case: tap one large button to call a saved contact, call the local emergency number or send a prepared help message. The app does not replace emergency services and cannot guarantee delivery of calls or messages; the emergency number is entered by the user because it differs by country.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, url_launcher (tel: and sms: links open the dialer or messaging app, which the user confirms), geolocator (optional location link, with a permission explanation).

## SCREENS

1. Home – very large buttons: Call Contact 1, Call Contact 2, Call Emergency Number, Send Help Message, Show Help Card.
2. Contacts Setup – name, phone number, relationship and order; at least one contact prompted on first run; validation.
3. Emergency Number Setup – the user enters the local emergency number; first-run prompt.
4. Help Message Setup – message text template and an include-location toggle.
5. Help Card – full-screen large text such as "I need help. Please call..." with a slow, gentle visual pulse and no rapid flashing.
6. Settings – button size, confirmation mode (confirm tap or press-and-hold for 1-2 s), haptics, theme, reset.

## NAVIGATION

Home is the only main screen; Setup screens and Settings from the app bar. Back returns one level; Android back from Home exits.

## UI/UX

Clear high-visibility style, light, dark and high-contrast. Primary red #C62828 for emergency actions, accent blue #1565C0, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Buttons at least 96dp tall with icon and text, confirm step to prevent accidental calls. Reusable EmergencyButton, ContactCard. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Tap or hold opens the dialer with the number pre-filled; the user presses call.
- Help message opens the messaging app with prepared text and an optional location link (user presses send).
- Help Card display; handle missing permissions and no-SIM/no-handler cases with clear messages.

## DATA AND BACKEND

Local storage only; no cloud, account or analytics. State that calls and messages must be tested on a physical device; do not place real emergency calls during testing.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for number validation, contact ordering, message building and permission-denied handling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 107. SCREEN READER PRACTICE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 107. SCREEN READER PRACTICE

## APPLICATION PURPOSE

Build "Screen Reader Practice", a Flutter app that teaches accessible navigation and screen-reader gestures through guided practice. It helps new users build confidence with TalkBack-style navigation and helps teachers demonstrate it. Target users are new screen-reader users, trainers and accessibility testers; main use case: complete short lessons and practise on a safe mock app. Assumption: the source description is cut off after "through". Limitation: gestures are interpreted by Android's own screen reader, so the app can confirm that actions occurred (an item was focused or activated) but cannot detect the gesture itself; when the screen reader is off it shows visual demonstrations and tells the user how to enable it.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts (optional coaching speech), android_intent_plus (open accessibility settings). Strong use of Flutter Semantics.

## SCREENS

1. Home – lessons, practice playground, progress, setup help.
2. Lessons – Introduction, Explore by Touch, Move Between Items, Activate Items, Scroll Lists, Text Fields, Headings and Reading Controls.
3. Lesson – steps with a short instruction, a practice area and success feedback when the expected action occurs; Repeat and Next.
4. Playground – mock app (list, buttons, toggle, slider, text field) with correct semantic labels; a free-practice mode.
5. Setup Help – how to turn the screen reader on and off, with a button opening accessibility settings.
6. Glossary – terms (focus, swipe, double-tap, heading, actions menu).
7. Settings – show captions, coaching speech, text size, theme.

## NAVIGATION

Home > Lessons > Lesson; Playground, Setup Help, Glossary from Home. Back returns one level and works with the screen reader active.

## UI/UX

Simple, predictable style, light, dark and high-contrast. Primary indigo #3949AB, accent teal #00ACC1, background #F6F7FC. Font Atkinson Hyperlegible (bundled). Logical focus order, every control labelled, no gesture-only actions, 48dp targets. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Lesson model (steps, expected action, hint, caption).
- Success detection via semantic actions and focus events; progress and badges saved.
- Detects whether an accessibility service is enabled and adapts the instructions.

## DATA AND BACKEND

Bundled JSON lessons and shared_preferences progress; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for lesson progression, expected-action matching, progress storage and semantics labels present on all controls and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 108. EASYREAD MODE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 108. EASYREAD MODE

## APPLICATION PURPOSE

Build "EasyRead Mode", a Flutter app that displays saved text in adjustable fonts, spacing and contrast. It makes reading comfortable for people with low vision, dyslexia or reading fatigue. Target users are readers who need customised text display; main use case: save a text and read it with personal display settings and optional read-aloud.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, flutter_tts, file_picker (import .txt), path_provider.

## SCREENS

1. Library – saved texts with title and preview; search; empty state; Add Text.
2. Add/Edit Text – title, typed or pasted text, or import a .txt file; validation; delete with confirm.
3. Reader – the text with a floating settings button and bottom bar for Read Aloud, text size and theme; scroll position remembered.
4. Display Settings – live-preview sliders for font size, line height, letter spacing, word spacing, margins and alignment; font choice (Atkinson Hyperlegible, a dyslexia-friendly option, Serif, Sans); colour themes (black on white, white on black, yellow on black, sepia); line-focus ruler.
5. Presets – save named display profiles and switch between them.
6. Settings – default preset, speech rate, theme.

## NAVIGATION

Library > Reader > Display Settings; Presets and Settings from Library. Back returns one level.

## UI/UX

Distraction-free reading style. Primary slate #37474F, accent amber #FFB300, background follows the chosen reading theme. Fonts bundled with licences credited (OFL). Interface elements stay readable whatever the reading theme. Reusable ReaderView, SettingSlider, PresetChip. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Settings apply instantly and are saved per preset.
- Text-to-speech with the current sentence highlighted; pause and resume.
- Line-focus ruler highlights a few lines at a time.
- Text import and size limits handled.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for preset repository, settings serialisation, text import limits and sentence splitting for read-aloud and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 109. CAPTION NOTES

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 109. CAPTION NOTES

## APPLICATION PURPOSE

Build "Caption Notes", a Flutter app that stores conversation notes and important written instructions. It helps people who rely on written communication keep a clear record of what was said or asked. Target users are people who are deaf or hard of hearing, or anyone who prefers written notes; main use case: type or dictate notes during a conversation and show them in large text to the other person. Assumption: notes are typed; optional dictation uses the device speech service, which may need a network.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, speech_to_text (optional),

share_plus, intl.

## SCREENS

1. Notes – list with type chip (Conversation, Instruction, Appointment, Quick Note), search and pinned notes; empty state.
2. Quick Note – fastest entry: a text box, optional dictation, Save.
3. Add/Edit Note – title, type, person or place, date, text, tags, pin; instruction notes can have a checklist; validation.
4. Note Detail – large-text view; Show to Someone mode with full-screen very large text; share as text; delete with confirm.
5. Search & Filter – by text, type, tag and date.
6. Settings – text size, theme, dictation language, default note type.

## NAVIGATION

Notes is home with a floating Quick Note button; Detail > Show mode. Back returns one level.

## UI/UX

Clean writing style, light, dark and high-contrast. Primary blue #1976D2, accent orange #FB8C00, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Large text, no sound dependence, strong contrast. Reusable NoteCard, TypeChip, BigTextView. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Note CRUD, pins, tags and full-text search.
- Optional dictation inserted at the cursor; permission and unavailable-service messages.
- Checklist notes with tick state; share as plain text.

## DATA AND BACKEND

Local sqflite and shared_preferences; no cloud or account. Say clearly if dictation sends audio to a device service.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for search and filters, checklist state, note repository and text sharing format and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 110. ACCESSIBLE KEYBOARD PRACTICE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 110. ACCESSIBLE KEYBOARD PRACTICE

## APPLICATION PURPOSE

Build "Accessible Keyboard Practice", a Flutter app for practising typing with adjustable text size and keyboard guidance. It helps people with limited dexterity or low vision build typing accuracy and confidence at their own pace. Target users are people learning or relearning to type on a phone; main use case: complete short typing lessons on an adjustable practice keyboard.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, flutter_tts (optional),

HapticFeedback.

## SCREENS

1. Home – continue lesson, free typing, progress, keyboard settings.
2. Lessons – letter groups, common words, short phrases and sentences, numbers, with completion marks.
3. Practice – target text with the next character highlighted, typed text, and a custom on-screen keyboard that highlights the next key; Backspace, Space and optional Hint.
4. Free Typing – a text field using the system keyboard to practise with the real keyboard; accuracy summary afterwards.
5. Result – accuracy, characters per minute (shown only if the user wants), mistakes by key; Retry and Next.
6. Progress – lessons done, accuracy trend chart.
7. Keyboard Settings – key size, spacing, layout (QWERTY or ABC), contrast theme, next-key highlight, tap-hold delay to ignore accidental touches, sound and haptic feedback.

## NAVIGATION

Home > Lessons > Practice > Result; Free Typing, Progress and Keyboard Settings from Home. Back confirms exit mid-lesson.

## UI/UX

Calm training style, light, dark and high-contrast. Primary teal #00796B, accent amber #FFA000, background #F5FAF9. Font Atkinson Hyperlegible (bundled). Keys at least 56dp (adjustable up to 96dp), no time pressure by default. Reusable KeyButton, TargetText, ResultCard. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Custom keyboard that reads settings live; hold delay filters accidental taps.
- Comparison of typed and target text with per-character correctness; speed only if enabled.
- Lesson content in JSON; progress and settings saved.

## DATA AND BACKEND

Local storage only; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for text comparison and accuracy, lesson progression, hold-delay filtering and progress storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 111. MOBILITY EQUIPMENT LOG

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 111. MOBILITY EQUIPMENT LOG

## APPLICATION PURPOSE

Build "Mobility Equipment Log", a Flutter app that tracks maintenance for wheelchairs, walkers and other assistive devices. It solves the problem of forgotten checks and repair history, which affect safety and cost. Target users are equipment users and carers; main use case: register equipment, schedule routine checks and log every maintenance task and repair. The app does not give medical or technical repair advice and tells users to follow the manufacturer's manual and a qualified technician.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, share_plus, intl.

## SCREENS

1. Equipment – list of devices with next due task and status; empty state; Add Equipment.
2. Add/Edit Equipment – type (wheelchair, walker, cane, scooter, other), name, purchase date, supplier and contact phone, warranty end date, notes; validation.
3. Equipment Detail – next tasks, maintenance history, total costs, issues list.
4. Maintenance Schedule – recurring tasks (for example tyre check, brake check, battery charge, cleaning, technician service) with interval days and reminders.
5. Add Log Entry – date, task, cost, vendor, notes; marking a scheduled task done resets its next due date.
6. Issues – report an issue with date and notes; mark resolved.
7. Settings – currency, reminder time, theme, CSV export.

## NAVIGATION

Equipment > Detail > Schedule/Log/Issues; Settings from the app bar. Back returns one level.

## UI/UX

Dependable utility style, light, dark and high-contrast. Primary blue #1565C0, accent orange #EF6C00, background #F4F7FB. Font Atkinson Hyperlegible (bundled). Status by icon and text, large tap areas. Reusable EquipmentCard, TaskRow, StatusChip. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Next due = last done + interval; overdue detection; reminders rescheduled on edit, completion and restart.
- Cost totals per device and year; warranty expiry flag; CSV export.
- Tap-to-dial supplier via the dialer.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for next-due calculation, overdue detection, cost totals and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 112. CHAIR EXERCISE CARDS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 112. CHAIR EXERCISE CARDS

## APPLICATION PURPOSE

Build "Chair Exercise Cards", a Flutter app that displays optional seated movement routines with clear illustrations. It gives people who prefer or need seated activity simple guidance for gentle movement. Target users are wheelchair users, older adults and people with limited standing ability; main use case: pick a routine, follow each illustrated card at their own pace. The app is not medical advice: it shows a safety notice at first launch, says to stop if there is pain or discomfort and to ask a health professional, and exercise content must be reviewed by a qualified physiotherapist before release.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite, flutter_tts (optional spoken cues). Illustrations drawn with Flutter or CC0/original art with alt text.

## SCREENS

1. Safety Notice – shown on first launch and in Settings; must be acknowledged.
2. Home – featured routine, categories, My Routines, activity log.
3. Categories – Warm-up, Arms and Shoulders, Hands and Wrists, Gentle Torso, Breathing, Cool-down.
4. Exercise Card – illustration, numbered steps, repetitions or duration, easier and gentler options, safety tips.
5. Routine Player – one card at a time with a visual countdown or repetition counter, Pause, Previous and Next, rest between cards; spoken cues optional.
6. My Routines – create and reorder custom routines from cards.
7. Activity Log – optional record of completed routines.
8. Settings – text size, speech cues, rest length, theme.

## NAVIGATION

Home > Category > Card; Home > Routine Player; My Routines and Log from Home. Back asks to confirm exit mid-routine.

## UI/UX

Calm encouraging style, light, dark and high-contrast. Primary green #43A047, accent teal #00ACC1, background #F4FAF4. Font Atkinson Hyperlegible (bundled). Large illustrations, text instructions as well as images, no flashing, no pressure messages. Reusable ExerciseCard, StepList, CountdownRing. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Exercise JSON (title, category, steps, reps or seconds, alternatives, safety tip).
- Routine player with timestamp-based timers; custom routines and log.
- Safety notice acknowledgement stored.

## DATA AND BACKEND

Bundled JSON and local storage; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for routine sequencing, timer logic, routine repository and acknowledgement gating and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 113. ACCESSIBLE HOME CHECKLIST

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 113. ACCESSIBLE HOME CHECKLIST

## APPLICATION PURPOSE

Build "Accessible Home Checklist", a Flutter app for reviewing doorways, lighting, bathroom access and other home accessibility features. It helps people and carers spot barriers and prioritise changes. Target users are people with mobility, vision or balance needs, carers and occupational-therapy clients; main use case: walk through each room, record findings and produce an action list. Assumption: the source description is cut off after "other home". Reference values (for example door width) are editable guideline defaults; users must confirm them against local standards or with a qualified professional.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, share_plus, intl.

## SCREENS

1. Assessments – saved home reviews with completion percentage; empty state; New Assessment.
2. New Assessment – name, address note, date.
3. Room List – Entrance, Doorways, Living Areas, Kitchen, Bathroom, Bedroom, Lighting, Floors and Stairs, Safety and Emergency with progress.
4. Room Checklist – items with Yes, No and Not Applicable, an optional measurement field (door width, step height) with unit, and a note.
5. Action List – every "No" item as an action with priority (High, Medium, Low), status and note.
6. Summary – counts, completion and actions by priority; Share as text.
7. Settings – units (cm or inches), editable guideline values, theme.

## NAVIGATION

Assessments > Rooms > Checklist; Action List and Summary from the assessment. Back returns one level.

## UI/UX

Clear practical style, light, dark and high-contrast. Primary teal #00796B, accent orange #EF6C00, background #F4F9F8. Font Atkinson Hyperlegible (bundled). Large Yes/No/NA controls with text labels. Reusable CheckItem, RoomCard, PriorityChip. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Checklist JSON (about 60 items); measurement comparison against editable guideline values, flagged for the user to review.
- Automatic action list from "No" and flagged items; progress and priority counts.
- Text report sharing; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account, cloud or photos required.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for guideline comparison, action-list generation, progress counts and the assessment repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 114. VISUAL DAILY TIMER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 114. VISUAL DAILY TIMER

## APPLICATION PURPOSE

Build "Visual Daily Timer", a Flutter app that shows task time as a visual countdown instead of relying on sound. It helps people who are deaf, hard of hearing or easily startled by sound, and anyone who benefits from seeing time pass. Target users are people who need visual time cues and their carers; main use case: pick a task, start the visual timer, or run a sequence of tasks as a visual schedule.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences,

flutter_local_notifications + timezone, HapticFeedback or vibration, wakelock_plus.

## SCREENS

1. Timer – very large visual countdown (shrinking disc, draining bar or hourglass) with minutes left in text, task name and icon; Start, Pause, Reset.
2. Tasks – saved tasks with icon, colour and duration; Add, edit and delete.
3. Visual Schedule – an ordered sequence of tasks with the current one highlighted; Next advances; shows the whole sequence at a glance.
4. Add/Edit Task – name, icon, colour, duration, alert type; validation.
5. Alert – end-of-time screen with a large visual cue (colour change and icon) and optional vibration; Done and Add 5 minutes.
6. Settings – visual style, alert type (visual, vibration, both, sound optional), reduced motion, keep screen on, theme.

## NAVIGATION

Bottom tabs Timer, Schedule, Tasks, Settings. Back from the timer keeps it running; Reset confirms.

## UI/UX

Calm, clear style, light, dark and high-contrast. Primary blue #1E88E5, accent amber #FFB300, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Colour changes always paired with shape or text; no rapid flashing. Reusable VisualTimer, TaskTile, ScheduleStep. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Timer uses end-timestamp logic so it stays correct when backgrounded or the screen locks.
- End alert via local notification with vibration; reduced-motion switches animation to a static fill.
- Schedule sequencing, extend time, task CRUD and persistence.

## DATA AND BACKEND

Local storage only; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for remaining-time calculation, schedule sequencing, task repository and alert settings and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 115. FOCUS-FRIENDLY TASKS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 115. FOCUS-FRIENDLY TASKS

## APPLICATION PURPOSE

Build "Focus-Friendly Tasks", a Flutter app that breaks daily tasks into small, manageable steps. It helps people for whom large tasks feel overwhelming, including people with fatigue, pain or attention difficulties. Target users are people who benefit from step-by-step guidance and their carers; main use case: create a task, list its small steps, then work through them one at a time in a distraction-free view. Assumption: steps are written by the user or chosen from templates; there is no AI generation.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone.

## SCREENS

1. Tasks – active tasks with a step progress bar; Add Task; empty state.
2. Add/Edit Task – title, optional due date and reminder, a step list with add, reorder and delete, optional minutes per step; validation.
3. Focus Mode – only the current step shown in large text with a big Done button, Skip, Back and "Take a break"; a quiet progress indicator.
4. Templates – ready step lists (for example tidy a room, prepare a meal, make a phone call) to copy and edit.
5. Completed – finished tasks with dates.
6. Settings – calm mode (hide counters and celebrations), text size, reminders, theme.

## NAVIGATION

Tasks > Add/Edit; Tasks > Focus Mode; Templates and Completed from Tasks. Back returns one level; leaving Focus Mode saves progress.

## UI/UX

Low-clutter calm style, light, dark and high-contrast. Primary soft blue #5C85D6, accent green #66BB6A, background #F8FAFD. Font Atkinson Hyperlegible (bundled). One main action per screen, generous spacing, gentle feedback, no timers shown unless enabled. Reusable StepCard, ProgressDots, BigDoneButton. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Task and step models; completion state per step; reorder steps.
- Focus Mode resumes where the user left off; optional per-step timer.
- Template copying; reminders; completed archive; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for step progression and resume, template copying, reminder scheduling and task repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 116. GESTURE LEARNING CARDS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 116. GESTURE LEARNING CARDS

## APPLICATION PURPOSE

Build "Gesture Learning Cards", a Flutter app for learning common gestures and their meanings. It helps learners, including people new to a culture or language, understand everyday non-verbal communication. Target users are learners of all ages and support staff; main use case: study illustrated gesture cards by category and test understanding in a short quiz. Assumption: gestures mean different things in different cultures, so each card has a cultural note, and potentially offensive gestures are left out; content is reviewed before release. This app covers general gestures, not a formal sign language.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional flutter_tts.

## SCREENS

1. Home – categories (Greetings, Agreement and Disagreement, Requests, Attention, Feelings), Quiz, Progress.
2. Category List – gesture cards as a grid with picture and name; search.
3. Gesture Card – large illustration, meaning, when it is used, a cultural note, and a similar-gesture tip; Flip, I Know It, Practise Again.
4. Quiz – "What does this gesture mean?" with 3-4 choices; 10 questions; results.
5. Match Game – match gesture pictures to meanings.
6. Progress – gestures known per category and quiz bests.
7. Settings – text size, speech, theme, reset.

## NAVIGATION

Home > Category > Cards; Home > Quiz/Match > Result. Back returns one level.

## UI/UX

Friendly clear style, light, dark and high-contrast. Primary purple #6A1B9A, accent orange #FB8C00, background #FAF6FC. Font Atkinson Hyperlegible (bundled). Large drawn illustrations with alt text that describes hand position and movement. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Gesture JSON (name, meaning, usage, cultural note, asset, review status).
- Flip, known tracking, search, quiz and match generators with unambiguous answers.
- Progress persistence.

## DATA AND BACKEND

Bundled JSON and original or openly licensed assets credited in CREDITS.md; shared_preferences progress; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for quiz generation, known tracking, search and content parsing and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 117. PERSONAL ASSISTANCE CARD

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 117. PERSONAL ASSISTANCE CARD

## APPLICATION PURPOSE

Build "Personal Assistance Card", a Flutter app for preparing a customisable card that describes the assistance a person prefers. It helps users explain their needs calmly to staff, drivers or helpers without repeating themselves. Target users are people who sometimes need assistance and their carers; main use case: build a card once, then show or share it when needed. Everything on the card is typed by the user and optional.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, share_plus, path_provider;

RepaintBoundary for exporting the card as an image.

## SCREENS

1. My Cards – saved cards (for example Travel, Appointments, Workplace); empty state; New Card.
2. Card Editor – card title, optional name, "How I communicate", "Assistance I may need" (preset checkboxes such as help with doors, stairs, reading, carrying, boarding, plus custom items), "How best to help" (do and do not), equipment I use, contact person, extra notes; validation.
3. Card Display – large-text full-screen card to show to someone; adjustable text size and contrast.
4. Share – export as an image or plain text through the share sheet, with a preview.
5. Presets – starting templates to copy and edit.
6. Settings – default text size, theme, reset.

## NAVIGATION

My Cards > Editor/Display; Share from Display; Presets and Settings from My Cards. Back confirms unsaved edits.

## UI/UX

Respectful calm style, light, dark and high-contrast. Primary blue #1976D2, accent teal #00ACC1, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Strong contrast on the card, plain wording, balanced layout. Reusable CardPreview, ChecklistField, ShareSheetButton. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Card CRUD with sections that can be hidden or shown; duplicate a card.
- Auto-fit large display; image export through RepaintBoundary.
- Preset templates; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud. Information is only shared when the user chooses Share.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for card repository, section visibility, text export format and preset copying and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 118. MEDICAL INFORMATION CARD

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 118. MEDICAL INFORMATION CARD

## APPLICATION PURPOSE

Build "Medical Information Card", a Flutter app that stores optional emergency information for the user to share when needed. It helps responders and carers get key details quickly. Target users are people who want a ready summary of their own information; main use case: enter details once, protect them with a lock and show or share the card on request. All fields are optional; the app is not a medical record, may be out of date, and does not replace Android's built-in emergency information.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, flutter_secure_storage (encrypted storage), local_auth (biometric or device PIN lock), share_plus, intl. Never write personal data to logs or analytics.

## SCREENS

1. Card – the formatted card (name, blood group, conditions, allergies, medications, doctor, emergency contacts, notes); Show Large and Share buttons; empty state prompting setup.
2. Edit Information – sections with optional fields; contact entries with tap-to-dial; save with validation.
3. Lock Setup – enable a device-credential or biometric lock; choose which fields (if any) are visible without unlocking.
4. Share Preview – include-field toggles and a preview of exactly what will be shared as text; Share.
5. Privacy Notice – how data is stored, what is shared, and the reminder to keep information updated; shown on first launch.
6. Settings – auto-lock delay, block screenshots on the card screen, theme, delete all data with confirm.

## NAVIGATION

Card is home; Edit, Lock Setup and Share Preview from the Card. Back returns one level; the app locks after the auto-lock delay.

## UI/UX

Clear trustworthy style, light, dark and high-contrast. Primary red #C62828 for emergency accents, accent blue #1565C0, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Large readable text, labelled sections, minimal decoration. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Encrypted storage of all fields; lock and unlock flow with fallback when no lock is set.
- Per-field share control; share as text.
- Optional screenshot blocking; delete-all.

## DATA AND BACKEND

Local encrypted storage only; no cloud, account or analytics. State that the lock depends on the device's security setup.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for field visibility and share-text generation, lock gating logic, secure-storage repository and delete-all and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 119. ACCESSIBLE JOB SKILLS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 119. ACCESSIBLE JOB SKILLS

## APPLICATION PURPOSE

Build "Accessible Job Skills", a Flutter app that teaches basic digital, office and workplace skills with accessible lessons. It helps people with disabilities build confidence for work. Target users are job seekers and new employees; main use case: complete short lessons with quizzes at their own pace using adjustable text and read-aloud. Assumption: the team writes about 8 original lessons per track (24 total) in JSON and has them reviewed; workplace-rights content is general and tells users that laws vary by country.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite, flutter_tts.

## SCREENS

1. Home – continue learning, tracks, progress.
2. Tracks – Digital Skills (email, video calls, spreadsheet basics, file management, online safety), Office Skills (communication, time management, teamwork, etiquette), Workplace Know-How (asking for adjustments,

workplace safety basics, preparing for work).

3. Lesson List – lessons with completion ticks.
4. Lesson – short sections with plain text and simple illustrations; Read Aloud, text size and contrast controls; Previous and Next.
5. Quiz & Result – 3-5 questions per lesson, simple layout, retry allowed, explanations.
6. Progress – lessons completed per track and badges.
7. Settings – text size, speech rate, theme, reduced motion.

## NAVIGATION

Home > Track > Lesson > Quiz > Result; Progress from Home. Back returns one level.

## UI/UX

Clear supportive style, light, dark and high-contrast. Primary indigo #3949AB, accent green #2E7D32, background #F6F7FC. Font Atkinson Hyperlegible (bundled). One column, large text, plain language, captions for any images. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Lesson JSON model; quiz scoring; progress and badges.
- Read-aloud with section highlighting; adjustable display settings saved.
- No time limits.

## DATA AND BACKEND

Bundled JSON content with local progress; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for quiz scoring, progress tracking, content parsing and settings persistence and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 120. INCLUSIVE LEARNING QUIZ

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 120. INCLUSIVE LEARNING QUIZ

## APPLICATION PURPOSE

Build "Inclusive Learning Quiz", a Flutter app that offers configurable quizzes with simple layouts and accessible controls. It lets learners, teachers and carers run quizzes that suit different abilities. Target users are learners with physical, visual or cognitive access needs and their educators; main use case: choose a quiz, adjust accessibility options and answer at a comfortable pace. Teachers can also create their own quizzes.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, flutter_tts, file_picker and share_plus (optional JSON import and export of quizzes).

## SCREENS

1. Quiz Library – bundled sample quizzes and custom quizzes with search; empty state; Create Quiz.
2. Quiz Player – one question per screen, large answer buttons (2-4 options), progress text, Read Aloud, Skip and Previous; no time limit by default.
3. Result – score, per-question review with explanations; Retry and Home.
4. Quiz Editor – quiz title, questions with type (multiple choice or true/false), options, correct answer and explanation; reorder and delete; validation (at least two options, one correct).
5. Accessibility Settings – text size, contrast theme, number of options shown, spoken questions and options, optional timer, answer confirmation (tap-to-select then Confirm), reduced motion.
6. History – past attempts and scores.

## NAVIGATION

Library > Player > Result; Library > Editor; Settings and History from Library. Back confirms exit mid-quiz.

## UI/UX

Simple uncluttered style, light, dark and high-contrast. Primary blue #1E88E5, accent amber #FFB300, background #FFFFFF. Font Atkinson Hyperlegible (bundled). Answers at least 64dp tall with text labels, no colour-only feedback. Reusable AnswerButton, QuestionCard, ProgressText. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Quiz JSON model with import and export validation.
- Player applies accessibility settings live; Confirm step prevents accidental answers.
- Scoring, history and quiz CRUD; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for scoring, quiz validation and import, editor validation and history repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 121. COLOR CONTRAST CHECKER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 121. COLOR CONTRAST CHECKER

## APPLICATION PURPOSE

Build "Color Contrast Checker", a Flutter app that checks text and background colour contrast for accessible designs. It helps designers, developers and people choosing readable colours meet accessibility guidelines. Target users are designers, developers and students; main use case: enter two colours and see the contrast ratio and pass or fail results at once.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite (saved palettes),

flutter_colorpicker (optional picker), share_plus. The calculation is a pure-Dart service.

## SCREENS

1. Checker – foreground and background colour inputs (hex field, RGB sliders and a picker), Swap button, live text and button previews, contrast ratio and results.
2. Results Detail – WCAG 2.1 pass or fail for normal text AA (4.5:1) and AAA (7:1), large text AA (3:1) and AAA (4.5:1), and user-interface components (3:1).
3. Suggestions – nearest lighter or darker foreground or background colours that reach AA or AAA, applied with one tap.
4. Saved Palettes – save, name, edit and delete colour pairs with their ratio.
5. Colour Vision Preview – simulate common colour vision types (protanopia, deuteranopia, tritanopia) on the pair.
6. About WCAG – short plain explanation of the rules and what the ratios mean.
7. Settings – theme, default result level, share format.

## NAVIGATION

Bottom tabs Checker, Palettes, Learn; Suggestions and Colour Vision from the Checker. Back returns one level.

## UI/UX

Tool-like clear style, light and dark. Primary indigo #3F51B5, accent green #00C853 for pass and red #D32F2F for fail (always with icon and text), background #F6F7FB. Font Inter (bundled). Hex values in a monospace font, large preview area. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Relative luminance from sRGB linearisation; ratio = (L1 + 0.05) / (L2 + 0.05).
- Hex parsing with validation (3, 6 digits, optional #); alpha ignored with a note.
- Suggestion search adjusting lightness until a target ratio is met; colour-vision matrices applied to the pair.
- Palette persistence and sharing as text.

## DATA AND BACKEND

Local storage only; no network, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for known ratios (black on white is 21:1), hex parsing, threshold results and suggestion search and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 122. VOICE-CONTROL PRACTICE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 122. VOICE-CONTROL PRACTICE

## APPLICATION PURPOSE

Build "Voice-Control Practice", a Flutter app that teaches supported phone voice commands through guided examples. It helps people who rely on or want to try voice control to learn commands step by step. Target users are people with limited hand mobility and their helpers; main use case: learn command groups, then rehearse them in guided scenarios. Limitation: voice-control commands vary by device, Android version and language, so the team must check the command lists against official Android Voice Access documentation and the app tells users commands may differ; the app cannot control the phone itself.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts, speech_to_text (optional practice matching, which may use the device speech service and a network), android_intent_plus (open accessibility settings).

## SCREENS

1. Home – command categories, guided practice, setup guide, progress.
2. Setup Guide – how to turn on voice control on Android and how to start and stop listening, with a button to open accessibility settings.
3. Categories – Navigation, Opening Apps, Scrolling and Selecting, Typing and Editing, Calls and Messages, Device Settings.
4. Command Card – the command phrase, what it does, an example sentence, a tip, and a Hear It button.
5. Guided Practice – a scenario ("Open the camera") with steps; the user says the command, the optional speech check compares what was heard to the target phrase, or the user taps "I did it"; supportive feedback.
6. Progress – commands practised and confidence by category.
7. Settings – language, show captions, speech check on or off, speech rate, theme.

## NAVIGATION

Home > Category > Card > Practice; Setup Guide and Progress from Home. Back returns one level.

## UI/UX

Calm instructional style, light, dark and high-contrast. Primary teal #00796B, accent orange #FB8C00, background #F4FAF9. Font Atkinson Hyperlegible (bundled). Command text very large, microphone state shown by icon and text, captions for all spoken feedback. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Command JSON (phrase, effect, example, category, notes).
- Phrase matching with tolerance (case, filler words) for the optional speech check; manual completion always available.
- Permission handling for the microphone; progress persistence.

## DATA AND BACKEND

Bundled JSON and shared_preferences; no account or cloud. State clearly if speech recognition needs a network.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for phrase matching tolerance, practice progression, progress storage and microphone-permission handling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 123. DAILY INDEPENDENCE TRACKER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 123. DAILY INDEPENDENCE TRACKER

## APPLICATION PURPOSE

Build "Daily Independence Tracker", a Flutter app for tracking personally chosen independent-living goals. It helps users and supporters see progress in everyday skills such as preparing a meal, using public transport or managing laundry. Target users are people building independence and their carers or therapists; main use case: pick goals, log how each day went and see progress over time. The wording is strengths-based and never compares the user with others.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, share_plus, intl.

## SCREENS

1. Today – chosen goals with a quick log button and a quiet summary; empty state prompting the first goal.
2. Add/Edit Goal – name, icon, optional steps, optional reminder; validation.
3. Log Entry – support level for the day (needed full help, needed prompts, did it independently, did not try today), a short note and an optional mood icon.
4. Goal Detail – trend chart of support levels, history list, notes, and milestones such as "first independent day".
5. Weekly Summary – goals practised, independent days and highlights; share as text with a supporter.
6. Settings – reminders, week start, theme, reset.

## NAVIGATION

Bottom tabs Today, Goals, Summary, Settings; Detail from Goals. Back returns one level.

## UI/UX

Warm encouraging style, light, dark and high-contrast. Primary green #43A047, accent blue #1E88E5, background #F5FAF5. Font Atkinson Hyperlegible (bundled). Positive wording, no red failure states, support levels shown by text and icon. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Daily entry per goal with an editable past day; support level scale 0-3.
- Trend calculation (rolling 7-day average); milestone detection.
- Weekly aggregation and text summary; reminders; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud; sharing happens only when the user presses Share.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for trend averaging, milestone detection, weekly summary text and the log repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 124. PUBLIC FACILITY CHECKLIST

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 124. PUBLIC FACILITY CHECKLIST

## APPLICATION PURPOSE

Build "Public Facility Checklist", a Flutter app for recording accessibility details about places the user visits. It builds a personal, reliable record of which places work for their needs. Target users are people with mobility or access needs and their companions; main use case: after or during a visit, tick the access features and add notes, then search past places by feature. All details are user-reported.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, image_picker (optional photos stored locally), path_provider, share_plus, intl.

## SCREENS

1. Places – saved places with type icon and a feature summary; search and filters; empty state; Add Place.
2. Add/Edit Place – name, type (restaurant, shop, hospital, office, transport station, other), address note, visit date, overall comfort rating 1-5; validation.
3. Access Checklist – step-free entrance, ramp, lift, accessible toilet, accessible parking, wide doors, seating, clear signage, helpful staff, each Yes, No or Not Checked, with a note.
4. Place Detail – checklist results, notes, photos, visit history; edit and delete with confirm.
5. Search & Filter – for example places with a lift and an accessible toilet; filter by type and rating.
6. Share – formatted summary as plain text.
7. Settings – theme, text size, checklist items (add or hide), reset.

## NAVIGATION

Places > Detail > Edit; Search and Settings from Places; floating Add. Back returns one level.

## UI/UX

Clear practical style, light, dark and high-contrast. Primary blue #0277BD, accent green #2E7D32, background #F4F8FB. Font Atkinson Hyperlegible (bundled). Yes and No shown by icon and text, large tap areas. Reusable PlaceCard, FeatureRow, RatingRow. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Place CRUD; multi-feature filters; comfort-rating sort.
- Optional photos copied into the app folder; share summary text.
- Custom checklist items; validation and persistence.

## DATA AND BACKEND

Local sqflite and app-folder photos; no maps or location services, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for feature filtering, summary text generation, custom checklist items and the place repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 125. EASY FORM ASSISTANT

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 125. EASY FORM ASSISTANT

## APPLICATION PURPOSE

Build "Easy Form Assistant", a Flutter app that explains common form fields in plain language and provides a checklist before the user submits a form. It helps people who find forms hard because of reading, dexterity, memory or confidence difficulties. Target users are people filling in forms and their helpers; main use case: choose a type of form, read what each section means and run the pre-submission checklist. Assumption: the source description is cut off after "before"; the guidance is general, not legal advice, and no personal data is entered or stored.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, flutter_tts, share_plus.

## SCREENS

1. Home – form types, field explainer, my checklists, progress.
2. Form Types – Job Application, Bank Account, Benefits or Support Application, Medical Registration, Rental Application, School or Course Enrolment.
3. Form Guide – for one type: documents to gather, section-by-section explanations and common mistakes to avoid.
4. Field Explainer – searchable A-Z of fields (full name, date of birth, address history, identity document, signature, declaration, income, reference, consent) with plain wording and "why it is asked".
5. Pre-Submission Checklist – ticks such as all required fields complete, spelling checked, dates in the right format, documents attached, signature added, copy kept; progress bar.
6. My Checklists – custom checklists based on a form type, with notes.
7. Settings – text size, read aloud, theme.

## NAVIGATION

Home > Form Types > Guide > Checklist; Field Explainer and My Checklists from Home. Back returns one level.

## UI/UX

Calm plain-language style, light, dark and high-contrast. Primary blue #1565C0, accent teal #26A69A, background #F5F9FC. Font Atkinson Hyperlegible (bundled). Short sentences, large checkboxes, a Read Aloud button on every guide. Accessibility: Semantics labels on every control, logical TalkBack focus order, text scaling to 200% without overflow, contrast of at least 4.5:1, 48dp+ touch targets, no colour-only cues, respect system reduced-motion.

## FUNCTIONALITY

- Form-type and field JSON authored and reviewed by the team.
- Search, per-checklist progress, read aloud with section highlighting.
- Checklist copying and notes; persistence; share as text.

## DATA AND BACKEND

Bundled JSON and local storage; no personal details, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for search, checklist progress, checklist copying and content parsing and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---
