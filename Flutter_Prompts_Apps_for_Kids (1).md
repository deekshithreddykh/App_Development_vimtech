# Flutter Prompts - Apps for Kids

One standalone prompt per page. Give each team only its own page.

1. ALPHABET ADVENTURE
2. COUNT & COLLECT
3. SHAPE DETECTIVE
4. ANIMAL SOUND SAFARI
5. TINY ART STUDIO
6. MONEY MASTER KIDS
7. LITTLE CHEF ACADEMY
8. GOOD HABITS HERO
9. EMOTION EXPLORER
10. MINI TRAFFIC SCHOOL
11. MEMORY MATCH WORLD
12. STORY SPINNER
13. WORD BUILDER JUNIOR
14. OPPOSITE WORLD
15. NATURE EXPLORER
16. SPACE MISSION KIDS
17. DAILY ENGLISH BUDDY
18. MY FIRST CLOCK
19. PUZZLE PATH
20. MUSICAL FINGERS
21. PATTERN GENIUS
22. WHAT'S MISSING?
23. POCKET SCIENCE LAB
24. MY DAILY MISSION
25. SIGN & LEARN KIDS

Each prompt below is in its own box. Use the copy button on the box to copy just that prompt.

---

## 1. ALPHABET ADVENTURE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 1. ALPHABET ADVENTURE

## APPLICATION PURPOSE

Build "Alphabet Adventure", a Flutter app where young children explore the letters A–Z by tapping big colourful letters, seeing a matching picture and hearing the letter sound and an example word. It solves the problem of dull, passive early-literacy practice by making letter recognition tactile and playful. Target users are pre-schoolers and early primary children (ages 3–6), often with a parent nearby. Main use case: open the app, pick a letter, see and hear it, then play a short quiz.

## TECHNOLOGY

Flutter, Dart, Android primary target. Packages: provider (state), shared_preferences (progress), flutter_tts (offline Android text-to-speech for letter and word pronunciation), built-in animations. Only free/open-source packages and CC0/own-drawn assets; emoji or Flutter-drawn graphics may stand in for pictures.

## SCREENS

1. Home – app title, three large buttons (Learn, Quiz, My Stars), settings icon. Shows total letters learned.
2. Letter Grid – 26 tappable tiles (A–Z); learned letters show a star; scrolling grid adapts to screen width.
3. Letter Detail – giant uppercase and lowercase letter, picture, example word (A – Apple). Tapping the letter speaks it; tapping the picture speaks the word; previous/next arrows and swipe move between letters. Marks the letter learned after it has been heard.
4. Quiz – Find the Letter – the app speaks a letter, the child picks the right tile from 3–4 options; 10 questions; happy/gentle-retry feedback; no harsh failure.
5. My Stars (Progress) – letters learned, quiz best score, star collection; empty state with encouragement.
6. Settings – sound on/off, speech speed, reset progress (behind a simple adult check such as "solve 3 + 4").

States: TTS unavailable (show message and still display text), empty progress, quiz result summary.

## NAVIGATION

Home → Letter Grid → Letter Detail (swipe within); Home → Quiz → Result → Home/Retry; Home → My Stars; Home → Settings. Android back returns one step; Quiz asks "Leave quiz?" before exiting. No dead ends.

## UI/UX

Bright, rounded, playful style; light theme. Primary orange #FF8A3D, accent teal #26C6DA, background cream #FFF8E7, surface white. Bundle a rounded child-friendly font (e.g. Baloo 2 or Fredoka, OFL licence) in assets. Very large text (letters 120 sp+), minimum 56 dp touch targets, 16–24 dp corner radii, consistent spacing. Bounce and sparkle animations on correct answers; each letter tile has its own colour. Reusable LetterTile, BigButton, StarBadge widgets.

## FUNCTIONALITY

- Letter data model: letter, example word, emoji/asset, colour. 26 entries in a local JSON asset.
- Tapping speaks letter and word using flutter_tts (en-US, slow rate).
- Learned state saved per letter; progress persists across restarts.
- Quiz: random 10 questions without repeats, distractors different from the answer, score and stars (9+ correct = 3 stars, 6+ = 2, else 1).
- Settings changes apply immediately.
- Errors: handle TTS init failure and corrupt saved data gracefully.

## DATA AND BACKEND

Fully local: JSON asset for content, shared_preferences for progress and settings. No backend, login or API keys needed. All features are real and working offline. Structure repositories so cloud sync could be added later.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 2. COUNT & COLLECT

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 2. COUNT & COLLECT

## APPLICATION PURPOSE

Build "Count & Collect", a Flutter game where children count groups of objects, choose the right number and earn stars that unlock new levels. It addresses early numeracy: connecting quantity with numerals through one-to-one counting. Target users are ages 4–7. Main use case: play a level of 5 counting questions, earn 1–3 stars, and unlock the next level.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, audioplayers (short cheer/pop sounds, CC0 files bundled by the team), optional flutter_tts to speak numbers. Free and open-source only; emoji or drawn shapes as objects.

## SCREENS

1. Home – Play, My Stars, Settings; total stars displayed.
2. Level Map – 10 levels on a winding path; locked levels greyed with a lock icon; completed levels show earned stars. Level ranges: L1 counts 1–3, L2 1–5, L3 1–7, L4 1–10 … L10 up to 20.
3. Gameplay – grid of identical objects (apples, balloons, fish); tapping an object highlights it and shows the running count (optional "tap to count" mode); answer choices as 3–4 number buttons; progress bar (question x/5); a correct answer shows a star flying into the star counter.
4. Level Result – 1–3 stars, correct count, Retry and Next buttons; unlock animation if a new level opens.
5. My Stars – total stars, stars per level, empty state.
6. Settings – sound, tap-to-count aid on/off, reset (adult check).

## NAVIGATION

Home → Level Map → Gameplay → Result → Level Map/Next level; Home → My Stars; Home → Settings. Back during gameplay shows a confirm dialog. Locked levels show a gentle "Earn more stars" message instead of opening.

## UI/UX

Cheerful, sunny style, light theme. Primary sky blue #42A5F5, accent yellow #FFCA28, background #E3F2FD, surface white. Fonts: Fredoka or Nunito bundled. Large number buttons (72 dp), clear contrast, soft shadows, 20 dp radii. Animations: objects pop in, stars fly to the counter. Reusable ObjectGrid, NumberChoiceButton, StarMeter.

## FUNCTIONALITY

- Question generator: picks object type and count within the level's range, builds 2–3 distinct distractors.
- Stars per level: 5/5 = 3, 4/5 = 2, 3/5 = 1, fewer = 0 (level not completed). Next level unlocks at 1+ star.
- Wrong answer: gentle shake; the question stays until answered or revealed after 2 tries (count shown).
- Progress, stars and unlocked levels persist.
- Optional speech of the chosen number.

## DATA AND BACKEND

Local only: question logic in Dart, level config in code or JSON, progress in shared_preferences. No backend, API or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (question generation, star scoring, unlock rules) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 3. SHAPE DETECTIVE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 3. SHAPE DETECTIVE

## APPLICATION PURPOSE

Build "Shape Detective", a Flutter hidden-object game in which children act as detectives who tap shapes hidden inside illustrated scenes (a house, robot, castle, rocket). It teaches shape recognition by linking basic geometric shapes to real objects. Target users are ages 4–7. Main use case: open a scene, read the mission ("Find 3 circles and 2 triangles"), tap matching shapes and complete the case.

## TECHNOLOGY

Flutter, Dart, Android. Scenes drawn with CustomPainter and composed shape widgets (no external image licences needed). Packages: provider, shared_preferences, optional audioplayers for feedback sounds. Free and open-source only.

## SCREENS

1. Home – Start Investigating, Shape Library, My Badges, Settings.
2. Case Select – 8–10 scenes as cards with difficulty and best stars; later cases unlock after earlier ones.
3. Scene Play – scene built from many shapes; mission bar at the top showing targets and found counts; tapping a correct shape circles it with a magnifier animation; wrong taps give a soft wobble; Hint button highlights one remaining target (limited to 3 per scene); timer optional.
4. Case Solved – stars (by hints used and wrong taps), detective badge, Next Case.
5. Shape Library – cards for circle, square, rectangle, triangle, oval, star, heart, diamond with a drawn example and real-world examples; tap to hear the name.
6. My Badges – earned badges, empty state.
7. Settings – sound, timer on/off, reset (adult check).

## NAVIGATION

Home → Case Select → Scene Play → Case Solved → next case or Case Select; Home → Shape Library; Home → My Badges; Home → Settings. Back from a scene asks to confirm.

## UI/UX

Friendly detective theme, light theme. Primary indigo #5C6BC0, accent amber #FFB300, background #F3F4FF, surface white. Fonts: Fredoka/Baloo 2 bundled. Each shape has a consistent colour. Large tap targets (minimum 48 dp, enlarge hit areas of small shapes), clear contrast, magnifier animation, confetti on solving. Reusable MissionBar, ShapeWidget, SceneCanvas.

## FUNCTIONALITY

- Scene data model: list of shape objects (type, position as fractions of scene size, size, colour, isTarget). Hit testing uses geometry for each shape type and scales with screen size.
- Mission per scene (shape types and counts) validated against shapes actually placed.
- Hint logic, wrong-tap counting, star calculation, unlock logic.
- Progress, stars and badges persist.

## DATA AND BACKEND

Local only: scenes defined in Dart/JSON, progress in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (hit testing, mission validation, scoring) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 4. ANIMAL SOUND SAFARI

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 4. ANIMAL SOUND SAFARI

## APPLICATION PURPOSE

Build "Animal Sound Safari", a Flutter app where children go on a virtual safari, hear an animal sound and match it with the right animal picture (and the reverse). It builds listening skills and animal vocabulary. Target users are ages 3–7. Main use case: play a safari round of matching questions, then browse animals and replay sounds.

## TECHNOLOGY

Flutter, Dart, Android. Packages: audioplayers, provider, shared_preferences. About 16–20 short animal sounds as bundled audio files; the team must source CC0 or openly licensed sounds (e.g. Freesound CC0, Wikimedia Commons) and list each file's licence in a CREDITS.md. Animal pictures: free CC0 illustrations or emoji. Do not invent or fake audio; if a sound file is missing, show the animal's written sound (e.g. "Moo!") and note it in the report.

## SCREENS

1. Home – Start Safari, Animal Gallery, My Badges, Settings.
2. Game Mode Select – "Hear & Pick" (play sound, choose from 3–4 pictures) and "See & Pick" (show animal, choose from 3–4 sound buttons).
3. Safari Game – round of 8 questions, replay-sound button, progress track along a safari path, feedback animations.
4. Round Result – score, stars, new badge, Play Again.
5. Animal Gallery – grid of animals; tapping opens a card with big picture, name, habitat, sound button.
6. My Badges – safari ranks (Cub, Explorer, Ranger, Safari Master) with empty state.
7. Settings – volume, reset (adult check).

## NAVIGATION

Home → Mode Select → Game → Result → Home/Play Again; Home → Gallery → Animal card; Home → Badges; Home → Settings. Back works at every level; leaving a game asks for confirmation.

## UI/UX

Warm savanna style, light theme. Primary green #43A047, accent orange #FB8C00, background sand #FFF3E0, surface white. Fonts: Baloo 2 bundled. Large rounded picture cards (min 100 dp), tactile press animations, a moving jeep progress marker. Reusable AnimalCard, SoundButton, ProgressTrack.

## FUNCTIONALITY

- Animal model: id, name, emoji/image, sound asset, habitat, fun fact.
- Question generator without repeats, with plausible distractors from the same list.
- Audio plays reliably, stops before the next one starts, and handles failure gracefully.
- Scoring, badges (by total correct), persistence.

## DATA AND BACKEND

Local only: JSON for animals, bundled audio, progress in shared_preferences. No backend. Audio files must be supplied by the team (see above).

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (question generation, scoring, badge rules) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 5. TINY ART STUDIO

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 5. TINY ART STUDIO

## APPLICATION PURPOSE

Build "TinyArt Studio", a Flutter drawing and colouring app where children draw freehand, colour ready-made outline pictures, and save their artwork to a local gallery. It gives young children a safe, ad-free creative outlet. Target users are ages 4–9. Main use case: open the canvas, draw or colour, save, and revisit artwork in the gallery.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, path_provider (storage), shared_preferences or sqflite (artwork metadata), optional share_plus (share a saved image through the Android share sheet). Drawing with CustomPainter; export PNG with RepaintBoundary. Free and open-source only.

## SCREENS

1. Home – New Drawing, Colouring Pages, My Gallery, with thumbnails of the last 3 artworks.
2. Drawing Canvas – white canvas; toolbar with brush, eraser, 3 brush sizes, colour palette (12 colours), undo, redo, clear (with confirm), save.
3. Colouring Page Picker – 8–10 outline pictures (cat, house, fish, tree, rocket…) built from vector regions.
4. Colouring Page – tap a region to fill with the selected colour; palette; undo/redo; save.
5. My Gallery – grid of saved artworks; empty state ("Make your first picture!"); menu to delete (confirm dialog).
6. Artwork Viewer – full-screen image, delete, share.

States: saving indicator, save success message, save failure message, storage errors.

## NAVIGATION

Home → Canvas / Colouring Picker → Colouring Page; both → Gallery after saving (option to continue drawing); Home → Gallery → Viewer. Back from a canvas with unsaved changes asks "Save before leaving?".

## UI/UX

Creative, colourful, minimal-chrome style; light theme so the canvas stays neutral. Primary purple #7E57C2, accent pink #EC407A, background #FAF7FF, surface white. Fonts: Fredoka bundled. Large circular colour swatches (48 dp), chunky tool icons, clear selected state, 16 dp radii. Reusable ColorPalette, ToolButton, ArtworkThumbnail.

## FUNCTIONALITY

- Stroke model (points, colour, width) with undo/redo stacks; eraser.
- Region fill: each colouring page is a list of vector Path regions with outlines; hit-testing selects a region; fills tracked as a map.
- Save: render via RepaintBoundary.toImage to PNG in the app documents folder; metadata (id, title, date, type) stored locally.
- Gallery load, delete, optional share via the system sheet.
- Warn when saving an empty canvas; handle low-storage errors.

## DATA AND BACKEND

Local only: PNG files plus a metadata list. No accounts, cloud or API keys. Sharing uses the Android share sheet only; there are no network features.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (undo/redo, region fill state, metadata repository) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 6. MONEY MASTER KIDS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 6. MONEY MASTER KIDS

## APPLICATION PURPOSE

Build "Money Master Kids", a Flutter app where children learn coin and note values, count money, and practise buying items in a pretend shop, including receiving change. It teaches practical early financial literacy. Target users are ages 5–9. Main use case: learn the denominations, then play shop games and quizzes. Assumption: the default currency is the Indian Rupee (coins ₹1, 2, 5, 10; notes ₹10, 20, 50, 100), with currency definitions kept in one configuration file so another currency can be added.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional flutter_tts. Coins and notes are drawn with Flutter widgets (stylised, not photographs or reproductions of real currency). Whole-number amounts only, stored as integers. Free and open-source only.

## SCREENS

1. Home – Learn Money, Count Money, Pretend Shop, Quiz, My Progress, Settings.
2. Learn Money – scrollable cards for each coin and note with value and a short fact; tap to hear its value.
3. Count Money – a target amount is shown; the child taps coins/notes from a tray into a pile until the total matches; running total shown; Reset and Check buttons.
4. Pretend Shop – items with prices (toy, apple, pencil…); the child pays with notes and coins from a wallet; if overpaid, the child selects the correct change; success animation.
5. Quiz – "Which coin is worth ₹5?" and "How much is this?"; 10 per round; score screen.
6. My Progress – games played, best scores, badges (Saver, Shopper, Money Master).
7. Settings – currency (if more than one is provided), sound, reset (adult check).

States: insufficient payment message, wrong-amount message, empty progress.

## NAVIGATION

Home → each activity → result/summary → Home. Shop and Count screens confirm before exit if mid-task. Android back works everywhere.

## UI/UX

Friendly shop style, light theme. Primary green #2E7D32, accent gold #FFC107, background #F1F8E9, surface white. Fonts: Nunito/Fredoka bundled. Money visuals large and distinguishable by size, colour and number; 56 dp+ tap targets; clear total display; coin-drop animations. Reusable MoneyCoin, MoneyNote, PriceTag, WalletTray.

## FUNCTIONALITY

- Denomination model driven by the currency config.
- Amount generation within age-appropriate ranges (₹1–20, then ₹1–100).
- Payment check: total ≥ price; change = total − price; validate the child's selected change exactly.
- Quiz question generators; scoring; badge rules; persistence of progress.

## DATA AND BACKEND

Local only: configuration and item lists in JSON, progress in shared_preferences. No backend, no real payments, no credentials. State clearly in the app and documentation that all purchases are pretend.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (totals, change calculation, question generation, badge rules) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 7. LITTLE CHEF ACADEMY

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 7. LITTLE CHEF ACADEMY

## APPLICATION PURPOSE

Build "Little Chef Academy", a Flutter app where children learn common ingredients, kitchen tools and how simple dishes are prepared through step-by-step interactive recipes. It introduces food vocabulary, healthy eating and kitchen safety. Target users are ages 5–10, with an adult nearby. Main use case: explore ingredients, then "cook" a simple recipe by choosing ingredients and ordering steps. Assumption: recipes are no-heat or adult-assisted (fruit salad, sandwich, lemonade, yoghurt parfait, pizza toast); any step involving knives or heat shows an "Ask a grown-up" badge.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional flutter_tts and audioplayers. Emoji or CC0 illustrations for ingredients. Free and open-source only.

## SCREENS

1. Home – Ingredients, Recipes, Quiz, Kitchen Safety, My Chef Badges.
2. Ingredient Library – category tabs (Fruits, Vegetables, Dairy, Grains, Spices); search; cards with name and picture.
3. Ingredient Detail – picture, name, where it comes from, one fun fact, healthy/"sometimes" food tag.
4. Recipe List – 5 recipes with difficulty and time; completed ones marked.
5. Cook the Recipe – part 1: choose the correct ingredients from a shelf (wrong choices wobble back); part 2: put the steps in the right order by drag or tap; the bowl/plate fills as steps complete; grown-up badge on knife/heat steps; "dish ready" celebration.
6. Chef Quiz – "Which tool do we use to…?" and "Which is a vegetable?" questions.
7. Kitchen Safety – illustrated rules (wash hands, ask before using knives, hot things are hot).
8. My Chef Badges – badges by recipes completed.

## NAVIGATION

Home → each section; Recipe List → Cook → Complete → Recipe List; Library → Detail. Back works throughout; leaving a recipe mid-way asks for confirmation.

## UI/UX

Warm kitchen style, light theme. Primary tomato red #E53935, accent fresh green #7CB342, background #FFF8F0, surface white. Fonts: Baloo 2 bundled. Big picture cards, 20 dp radii, bouncy drag animations. Reusable IngredientCard, StepTile, SafetyBadge.

## FUNCTIONALITY

- Ingredient and recipe models loaded from local JSON (about 30 ingredients, 5 recipes).
- Ingredient-selection validation against the recipe's list; step-order validation with hints.
- Search and category filtering; quiz generator; badge rules; progress persistence.
- Content must be accurate and child-safe; avoid raw/undercooked or allergen-risky steps.

## DATA AND BACKEND

Local only: JSON content, shared_preferences for progress. No backend or credentials. Include a note for teachers that allergens are not modelled.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (ingredient validation, step ordering, search, badges) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 8. GOOD HABITS HERO

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 8. GOOD HABITS HERO

## APPLICATION PURPOSE

Build "Good Habits Hero", a Flutter app that guides children through timed challenges for brushing teeth, washing hands and tidying up, rewarding each completion with hero points and badges. It helps parents build healthy daily habits without nagging. Target users are ages 4–8 and their parents. Main use case: start a timed challenge, follow the animated steps, mark it done and watch the streak grow.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences (completion history), flutter_local_notifications plus timezone (daily reminders), audioplayers (tick/cheer sounds). Free and open-source only.

## SCREENS

1. Home – hero avatar and name, today's three challenge cards (Brush, Wash, Tidy) with done/not-done state, streak counter, points.
2. Brushing Challenge – 2-minute animated timer split into 4 quadrants (top-left, top-right, bottom-left, bottom-right) with prompts; pause/resume; "I did it!" at the end.
3. Handwashing Challenge – 20-second timer with 6 illustrated steps (wet, soap, palms, backs, between fingers, rinse).
4. Tidy-Up Challenge – checklist of 5 tidy tasks (toys in the box, books on the shelf…) with an optional "beat the clock" countdown.
5. Badges & Streaks – badge gallery (3-day streak, 7-day streak, 10 brushes…), locked/unlocked states.
6. Calendar History – month view showing days on which all challenges were completed.
7. Parent Settings (behind an adult check) – hero name, reminder times for morning and evening, sound, reset data.

States: notification permission denied message, empty history.

## NAVIGATION

Home → Challenge screens → Completion celebration → Home; Home → Badges; Home → Calendar; Home → Parent Settings. Back during a timer asks "Stop challenge?".

## UI/UX

Superhero-themed, light theme. Primary blue #1E88E5, accent red #E53935 and yellow #FDD835, background #EAF4FF. Fonts: Bangers or Baloo 2 for headings (bundled), Nunito for body. Large circular timer, big start buttons, cape/star motifs. Reusable ChallengeCard, CircularCountdown, BadgeTile.

## FUNCTIONALITY

- Timers with pause/resume that survive screen rotation and app backgrounding (use timestamps, not only tick counters).
- Completion log per day and challenge; streak calculation (consecutive days with at least one challenge); points and badge rules.
- Calendar rendering from history.
- Local reminders scheduled at parent-set times; request Android 13+ notification permission; reschedule when times change.

## DATA AND BACKEND

Local only: history in sqflite / shared_preferences. No backend. Reminder scheduling is a real device feature and must be tested on a device or emulator; state clearly if it could not be verified.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (streaks, badge rules, timer logic) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 9. EMOTION EXPLORER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 9. EMOTION EXPLORER

## APPLICATION PURPOSE

Build "Emotion Explorer", a Flutter app that helps children identify and name feelings (happy, sad, angry, scared, surprised, excited, tired, proud) using illustrated faces and short everyday situations. It supports early emotional literacy, which helps children talk about how they feel. Target users are ages 4–8 with a parent or teacher. Main use case: explore the faces, play the situation game, and do a daily feelings check-in. The app is educational only and makes no clinical or diagnostic claims.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite (check-in log), optional flutter_tts. Faces drawn with CustomPainter or emoji so they animate (blink, smile) without external licences. Free and open-source only.

## SCREENS

1. Home – Feelings Faces, Situation Game, Match the Face, How Do I Feel Today?, Calm Corner.
2. Feelings Faces – grid of 8 emotions; tapping opens a large animated face with its name (spoken), a short child-friendly description and a tip ("When I feel sad, I can ask for a hug").
3. Situation Game – a short scenario card with an illustration ("Your balloon floated away"); choose the matching feeling from 3–4 face buttons; gentle explanation after each answer (more than one feeling can be reasonable, so explanations are supportive rather than strictly right/wrong where appropriate).
4. Match the Face – drag emotion names to faces, or faces to names, in rounds of 4.
5. Daily Check-in – pick today's feeling, optional intensity (small/medium/big); saved to a calendar.
6. Feelings Calendar – month view with the face for each day; empty state.
7. Calm Corner – breathing animation (a balloon inflating for 4 seconds and deflating for 4), optional spoken prompts.
8. Settings – sound, reset history (adult check).

## NAVIGATION

Home → each section; Check-in → Calendar; games → Result → Home. Android back works everywhere.

## UI/UX

Soft, warm, reassuring style, light theme. Primary soft purple #9575CD, accent coral #FF8A65, background #FFF8F5, surface white. Each emotion has its own colour. Fonts: Nunito/Baloo 2 bundled. Calm animations, no flashing or startling effects, large touch targets, high contrast. Reusable FaceWidget, EmotionCard, ScenarioCard.

## FUNCTIONALITY

- Emotion and scenario data in local JSON (at least 8 emotions, 24 scenarios).
- Scenario game with accepted-answer lists per scenario, supportive feedback and score.
- Matching game logic; daily check-in storage (one entry per day, editable); calendar view.
- Breathing timer with animation controller; persistence.

## DATA AND BACKEND

Local only: check-in entries stay on the device. No accounts, analytics or cloud. Mention in the documentation that the app is not a mental-health tool and that teachers should review the scenario content.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (scenario answer validation, check-in storage, calendar mapping) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 10. MINI TRAFFIC SCHOOL

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 10. MINI TRAFFIC SCHOOL

## APPLICATION PURPOSE

Build "Mini Traffic School", a Flutter app that teaches children common road signs and safe pedestrian behaviour through lessons, a crossing simulator and quizzes. It addresses child road safety, which is best learned before children walk alone. Target users are ages 5–10. Main use case: learn signs, practise crossing a street safely in the simulator, and earn a Mini Licence. Assumption: signs follow widely recognised international shapes and colours; because rules vary by country, the app shows a note to parents that local rules take priority.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional flutter_tts and audioplayers. Signs and the street scene are drawn with CustomPainter/widgets (do not copy official sign artwork). Animations use AnimationController. Free and open-source only.

## SCREENS

1. Home – Learn Signs, Cross Safely, Sign Quiz, My Licence, Settings.
2. Sign Library – tabs Stop/Prohibition, Warning, Information; 20 signs as cards; tapping opens the sign with meaning and a kid-friendly tip.
3. Safety Lessons – swipeable illustrated lessons: Stop, Look, Listen, Think; use the zebra crossing; hold hands; stay on the footpath; never run onto the road.
4. Crossing Simulator – animated street with moving vehicles and a traffic light; the child taps "Go" only when it is safe; the pedestrian walks across; unsafe moves trigger a friendly "Stop and look again!" message; 5 rounds with increasing difficulty.
5. Sign Quiz – "What does this sign mean?" and "Which sign means…?"; 10 questions; results.
6. My Licence – progress toward the Mini Licence (lessons viewed, simulator score, quiz score); a certificate card is shown when the requirements are met.
7. Settings – sound, reset (adult check).

## NAVIGATION

Home → each section; Library → Sign detail; Simulator/Quiz → Result → Home. Back asks confirmation inside the simulator and quiz.

## UI/UX

Friendly town-street style, light theme. Primary traffic blue #1976D2, accent safety yellow #FFC107, with red and green reserved for traffic-light meaning, background #F2F7FC. Fonts: Nunito/Baloo 2 bundled. Large signs, clear contrast, no colour-only cues (add icons/text), smooth vehicle animation. Reusable SignWidget, LessonCard, TrafficLight.

## FUNCTIONALITY

- Sign model: id, shape, colours, symbol, name, meaning, category; rendered programmatically.
- Simulator state machine: light state, vehicle positions, safe-to-cross check, scoring and feedback.
- Quiz generator, Mini Licence rules (e.g. all lessons viewed, simulator 4/5, quiz 8/10), persistence.
- Content reviewed for accuracy; state the region assumption in the documentation.

## DATA AND BACKEND

Local only: signs and lessons in JSON/Dart, progress in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (safe-to-cross rules, licence requirements, quiz generation) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 11. MEMORY MATCH WORLD

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 11. MEMORY MATCH WORLD

## APPLICATION PURPOSE

Build "Memory Match World", a Flutter card-flipping game where children find matching pairs of pictures across themed worlds (Animals, Fruits, Vehicles, Space, Ocean). It trains visual memory and concentration in a calm, non-competitive way. Target users are ages 4–8. Main use case: choose a world and grid size, flip cards to find all pairs, and beat their own best score.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional audioplayers. Card faces use emoji or CC0 illustrations; the flip uses a 3D Transform animation. Free and open-source only.

## SCREENS

1. Home – Play, Best Scores, Settings.
2. World Select – 5 themed worlds as large cards; Ocean and Space unlock after earning stars in the first worlds.
3. Difficulty Select – Easy (2×2 or 2×3), Medium (3×4), Hard (4×4); best moves shown per option.
4. Game Board – responsive card grid; flip animation; moves counter; optional timer; pause menu (resume, restart, quit).
5. Win Screen – stars (by moves), new-best highlight, Play Again, Next World.
6. Best Scores – table by world and difficulty; empty state.
7. Settings – sound, timer on/off, card-back style, reset (adult check).

## NAVIGATION

Home → World Select → Difficulty → Game → Win → Home/Replay. Pause menu and Android back both open the pause menu rather than quitting at once. No dead ends.

## UI/UX

Colourful world-map style, light theme. Primary teal #00897B, accent orange #FF7043, background #E0F7F4. Each world has its own card-back colour/pattern. Fonts: Fredoka bundled. Cards scale to fill the available space, minimum 64 dp; flip and match-glow animations; no harsh failure sounds. Reusable MemoryCard, WorldTile, StatsBar.

## FUNCTIONALITY

- Shuffled deck from the chosen world's picture set (pairs = rows × columns ÷ 2), seeded so tests are reproducible.
- Game state machine: at most two cards face-up, match check with a short delay, input locked during the delay, matched cards stay revealed.
- Moves, optional timer, star rules (e.g. moves ≤ pairs×1.5 = 3 stars), best-score saving per world and difficulty, world unlock rules.

## DATA AND BACKEND

Local only: picture sets in code/JSON, scores in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (deck generation, match state machine, scoring, unlocks) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 12. STORY SPINNER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 12. STORY SPINNER

## APPLICATION PURPOSE

Build "Story Spinner", a Flutter app where children pick a character, a place and a goal, then the app assembles a short, illustrated, read-aloud story. It encourages imagination and early reading. Target users are ages 4–9, ideally with a parent. Main use case: choose the story ingredients, press "Spin!", read or listen to the story, and save favourites. Assumption: stories are generated offline from a template library (no AI service is needed); the generator is written behind an interface so an LLM could be plugged in later.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite (saved stories), flutter_tts (read aloud). Illustrations composed from emoji or CC0 art. Free and open-source only.

## SCREENS

1. Home – Spin a Story, My Stories, Settings.
2. Choose Character – grid of 8–12 characters (dragon, robot, princess, fox…); choose one (optionally a friend).
3. Choose Place – grid of 8 places (forest, castle, moon, ocean, school…).
4. Choose Goal – 6 goals (find a lost toy, make a new friend, bake a cake, learn to fly…) plus a "Surprise me" spinner wheel.
5. Story Reader – 5–6 pages, each with a composed illustration and 2–4 short sentences; Next/Previous; Read Aloud with highlighting of the current sentence; Save to My Stories; The End page with Spin Again.
6. My Stories – list of saved stories with title and thumbnail; open or delete; empty state.
7. Settings – text size, voice speed, reading level (simple/longer), reset saved stories (adult check).

## NAVIGATION

Home → Character → Place → Goal → Reader → Home/My Stories; Home → My Stories → Reader. A step indicator shows progress; back returns to the previous choice with the selection kept.

## UI/UX

Storybook style, light theme. Primary violet #7B5EA7, accent gold #FFC145, background parchment #FFF9ED. Fonts: a clear storybook-friendly font such as Andika or Baloo 2 (bundled, OFL). Large readable text (24 sp+ by default), generous spacing, page-turn animation. Reusable ChoiceTile, StoryPage, SpinWheel.

## FUNCTIONALITY

- Story engine: a template per goal with slots (character, friend, place), a beginning/middle/end structure, and several interchangeable sentence variants so repeated spins differ.
- Grammar handling for a/an, pronouns (he/she/they/it) and plurals per character.
- Title generation, page splitting, TTS reading with pause/resume, favourites storage.
- Content is child-safe, with gentle conflict and a positive ending.

## DATA AND BACKEND

Local only: character/place/goal/template data in JSON, saved stories on device. No backend or credentials. Clearly document the generator interface for future AI integration; do not claim AI generation.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (story generation across all combinations, grammar helpers, saved-story storage) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 13. WORD BUILDER JUNIOR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 13. WORD BUILDER JUNIOR

## APPLICATION PURPOSE

Build "Word Builder Junior", a Flutter game where children see a picture and arrange scrambled letter tiles to spell the word. It builds spelling and early reading skills. Target users are ages 5–8. Main use case: pick a level, spell pictured words, collect them in a word book.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts (pronounce the word), optional audioplayers. Pictures are emoji or CC0 art. Free and open-source only.

## SCREENS

1. Home – Play, My Word Book, Settings.
2. Level Select – 3-letter (cat, sun), 4-letter (frog, milk) and 5-letter (apple, horse) levels as packs of 10 words; progress shown on each pack.
3. Game – picture, empty letter slots, scrambled tile tray (including 1–2 extra distractor letters on higher levels); letters placed by drag or tap; tap a placed letter to remove it; Hint (reveals one letter) and Listen (speaks the word); Check happens automatically when all slots are filled.
4. Word Complete – celebration, the word spoken, Next Word.
5. Pack Result – stars by hints used and mistakes.
6. My Word Book – collected words with pictures; tap to hear; empty state.
7. Settings – sound, speech, uppercase/lowercase tiles, reset (adult check).

## NAVIGATION

Home → Level Select → Game → Word Complete → next word → Pack Result → Level Select; Home → Word Book. Back from a game returns to Level Select after confirmation.

## UI/UX

Bright wooden-blocks style, light theme. Primary blue #3F8EFC, accent lime #9BE564, background #EEF6FF. Fonts: a clear, child-friendly letterform font (e.g. Andika) bundled. Tiles 56 dp+; wrong placement shakes and returns; correct word triggers a pop. Reusable LetterTile, LetterSlot, PictureCard.

## FUNCTIONALITY

- Word list (about 90 words, 30 per length) with picture and category, in local JSON.
- Scramble that never equals the original order; distractor letters on later packs.
- Drag/tap placement logic, auto-check, hint tracking, stars, word-book unlocking, persistence.
- Handle repeated letters correctly.

## DATA AND BACKEND

Local only: JSON word list, progress in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (scrambling, repeated letters, auto-check, hints, stars) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 14. OPPOSITE WORLD

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 14. OPPOSITE WORLD

## APPLICATION PURPOSE

Build "Opposite World", a Flutter app that teaches common opposite word pairs (big/small, hot/cold, up/down, happy/sad, fast/slow, open/closed, full/empty, day/night and more) using paired illustrations, interactive animations and games. It strengthens vocabulary and comparison concepts. Target users are ages 4–7. Main use case: explore pairs, then play matching and quiz games.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts, optional audioplayers. Illustrations are emoji or simple drawn widgets scaled/coloured to show the contrast. Free and open-source only.

## SCREENS

1. Home – Learn Pairs, Match Opposites, Quiz, My Progress.
2. Learn Pairs – swipeable cards (20 pairs): each shows two panels with the words and visuals; tapping a panel speaks the word; a small interaction demonstrates the idea (a slider resizing an object for big/small, a thermometer for hot/cold).
3. Match Opposites – drag a word/picture to its opposite across two columns, in rounds of 4 pairs.
4. Quiz – "What is the opposite of HOT?" with 3 picture options; 10 questions.
5. Result – stars and encouragement, Play Again.
6. My Progress – pairs learned (stars on seen pairs), best quiz score, badges; empty state.
7. Settings – sound, speech, reset (adult check).

## NAVIGATION

Home → each activity → Result → Home. Back works everywhere; leaving a game asks for confirmation.

## UI/UX

Split-world style (a sunny half and a night half), light theme with contrasting panels. Primary orange #FB8C00, secondary indigo #5C6BC0, background #FFF7EB. Fonts: Baloo 2 bundled. Large panels, clear colour/shape contrast, smooth morph animations. Reusable PairCard, OppositeSlider, DraggableWord.

## FUNCTIONALITY

- Pair data model: word A, word B, visual A, visual B, interaction type, in local JSON.
- Matching logic with drag targets and correct/incorrect feedback; quiz generator with distractors that are not synonyms of the answer.
- Learned tracking, scoring, badges, persistence.

## DATA AND BACKEND

Local only: JSON content, progress in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (match validation, quiz generation, scoring) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 15. NATURE EXPLORER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 15. NATURE EXPLORER

## APPLICATION PURPOSE

Build "Nature Explorer", a Flutter app where children browse a catalogue of plants, animals, birds, insects and habitats, read simple facts, and collect discoveries in their own Explorer Book. It nurtures curiosity about the natural world. Target users are ages 5–10. Main use case: browse a category, open an entry, learn facts, collect it, and test knowledge in a quiz. Assumption: content is a bundled offline catalogue of about 40 entries; any images must be CC0/openly licensed with credits in CREDITS.md, and emoji is the fallback.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional flutter_tts. Free and open-source only. Facts must be accurate and simply worded; the team should verify them against a reliable source (e.g. a national geographic or museum site) and record the source in the documentation.

## SCREENS

1. Home – Fact of the Day, categories (Animals, Birds, Insects, Plants, Habitats), My Explorer Book, Quiz.
2. Category List – entries as picture cards with a search bar and filter chips (e.g. habitat, diet).
3. Entry Detail – image, name, a "quick facts" panel (habitat, diet or growth, size), a fun fact, a Listen button, and Add to Explorer Book.
4. My Explorer Book – collected entries grouped by category, collection progress (e.g. 12/40); empty state.
5. Nature Quiz – 10 questions generated from entries ("Which animal lives in the desert?"); results.
6. Settings – text size, sound, reset (adult check).

## NAVIGATION

Home → Category → Detail → Explorer Book; Home → Book; Home → Quiz → Result. Search results and filters keep state when going back.

## UI/UX

Fresh outdoor style, light theme. Primary leaf green #4CAF50, accent sun yellow #FFC83D, background #F4FBF0. Fonts: Nunito/Baloo 2 bundled. Large photo cards, rounded 16 dp corners, soft parallax in the detail header, readable fact panels. Reusable NatureCard, FactPanel, CollectionProgress.

## FUNCTIONALITY

- Entry model: id, category, name, image, habitat, diet, size, fun fact, tags.
- Search by name or tag, category filtering, collection add/remove, daily fact (rotates by date), quiz generation, progress persistence.
- Handle missing images with the emoji fallback.

## DATA AND BACKEND

Local only: bundled JSON and assets, collection state in shared_preferences. No backend, API or credentials. State clearly that content is a fixed offline catalogue, not live data.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (search, filtering, daily fact, quiz generation, collection) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 16. SPACE MISSION KIDS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 16. SPACE MISSION KIDS

## APPLICATION PURPOSE

Build "Space Mission Kids", a Flutter app where children explore the Sun, the eight planets, the Moon and Pluto through an animated solar-system view and swipeable information cards, then earn astronaut ranks by completing missions (quizzes). It makes astronomy approachable for young learners. Target users are ages 6–10. Main use case: tap a planet, read its card, play the space quiz, and rank up.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional flutter_tts, optional audioplayers. The solar system and planets are drawn with CustomPainter and AnimationController (no image licences needed). Free and open-source only. Planet data must be checked against NASA's public planetary fact sheets and the source noted in the documentation.

## SCREENS

1. Home – Explore the Solar System, Planet Cards, Space Quiz, Weight on Planets, My Rank.
2. Solar System View – animated orbits (not to scale, labelled as such); tap a planet to open its card; pinch/drag to move.
3. Planet Cards – swipeable PageView for 10 bodies: picture, name, size comparison to Earth, distance from the Sun, length of day and year, number of moons, a fun fact, a Listen button.
4. Weight on Planets – child enters a weight (validated number, 1–200 kg); results are shown for each planet with a bar visual.
5. Space Quiz (Missions) – 5 missions of 5 questions; completing missions raises rank (Cadet, Pilot, Commander, Captain).
6. My Rank – current rank, missions completed, planets visited; empty state.
7. Settings – sound, text size, reset (adult check).

## NAVIGATION

Home → Solar System → Planet Card; Home → Planet Cards (same pager); Home → Weight; Home → Quiz → Result → My Rank. Back works throughout.

## UI/UX

Deep-space style, dark theme (justified by the subject) with high-contrast text. Primary deep navy #0B1D3A, accent comet orange #FF9800, secondary cyan #4DD0E1, surface #14284B. Fonts: Baloo 2 or Nunito for body, a rounded display font for titles, bundled. Gentle star-field animation (provide a reduced-motion setting), large cards, 16 dp radii. Reusable PlanetWidget, InfoCard, RankBadge.

## FUNCTIONALITY

- Planet data model loaded from JSON, with surface gravity used for the weight calculator (weight on planet = weight × gravity ratio).
- Orbit animation with relative (not scale-accurate) speeds; tap hit-testing on moving planets.
- Quiz generation from the data, rank rules, visited tracking, persistence.
- Number input validation and error messages.

## DATA AND BACKEND

Local only: bundled JSON data, progress in shared_preferences. No backend or API keys. State clearly that orbit visuals are illustrative.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (weight calculation, quiz generation, rank rules, input validation) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 17. DAILY ENGLISH BUDDY

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 17. DAILY ENGLISH BUDDY

## APPLICATION PURPOSE

Build "Daily English Buddy", a Flutter app that helps young learners practise everyday English vocabulary and short sentences (greetings, family, food, school, colours, numbers, daily routines) with pictures, spoken audio and simple exercises. It supports children who are learning English at home or at school. Target users are ages 5–9 learners with an adult helper. Main use case: pick a topic, learn the words, build sentences, and take a short quiz. Assumption: pronunciation uses device text-to-speech; the app does not grade the child's speech.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, flutter_tts (English voice, adjustable rate). Pictures are emoji or CC0 art. Free and open-source only.

## SCREENS

1. Home – Word of the Day, Topics, Practice, My Progress.
2. Topics – 6 topic cards (Greetings, Family, Food, School, Colours & Numbers, My Day) with progress rings.
3. Word Cards – swipeable cards with picture, word and example sentence; tap to hear the word, double-tap or a button to hear the sentence; Mark as Known.
4. Sentence Builder – scrambled word chips are arranged into a sentence ("I like apples"); picture clue; check and hint buttons; the finished sentence is spoken.
5. Quiz – listen-and-choose (hear a word, pick the picture) and fill-in-the-blank questions; 10 per round.
6. Result – stars, new words learned, Retry.
7. My Progress – words known per topic, streak, badges; empty state.
8. Settings – speech speed, slow-voice mode, reset (adult check).

## NAVIGATION

Home → Topics → Word Cards / Sentence Builder / Quiz (per topic) → Result; Home → Practice (mixed topics); Home → Progress. Back works everywhere.

## UI/UX

Friendly classroom style, light theme. Primary blue #2979FF, accent sunshine #FFB300, background #F3F8FF. Fonts: Andika or Nunito bundled. Big picture cards, clear pronunciation buttons (48 dp+), cheerful feedback. Reusable WordCard, SentenceChip, TopicTile.

## FUNCTIONALITY

- Content model: topic, word, picture, example sentence (about 100 words, 40 sentences) in local JSON.
- TTS service with failure handling; sentence-building validation (accept the single correct order, with an alternate-orders list where grammar allows).
- Quiz generator, known-word tracking, daily word by date, streaks, persistence.

## DATA AND BACKEND

Local only: JSON content, progress in shared_preferences. No backend or credentials. Document that the device must have an English TTS voice installed.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (sentence validation, quiz generation, progress tracking) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 18. MY FIRST CLOCK

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 18. MY FIRST CLOCK

## APPLICATION PURPOSE

Build "My First Clock", a Flutter app with a large interactive analog clock that children can drag to learn how the hour and minute hands show time. It covers o'clock, half past, quarter past and quarter to, then five-minute intervals. Target users are ages 5–8. Main use case: explore the clock, then practise setting and reading times in short games.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional flutter_tts to speak times. The clock face is drawn with CustomPainter; hands are moved with GestureDetector pan events. Free and open-source only.

## SCREENS

1. Home – Learn, Set the Time, Read the Clock, My Day, My Stars.
2. Learn the Clock – a big clock with draggable hands; the digital time and the words ("half past 3") update live; a lesson mode introduces o'clock, half past, quarter past, quarter to in sequence with example prompts; tap to hear the time.
3. Set the Time – the app shows or speaks a time (digital or words); the child drags the hands; Check confirms; hints show the target hand position; levels: hours → half hours → quarters → five minutes.
4. Read the Clock – a clock face is shown; choose the matching time from 3–4 options; 10 questions.
5. My Day – match daily activities (wake up, lunch, bedtime) to clock times or to parts of the day.
6. Result – stars and level unlock.
7. My Stars – progress per level; empty state.
8. Settings – 12/24-hour digital display, sound, hand-snapping on/off, reset (adult check).

## NAVIGATION

Home → each activity → Result → Home/Next level. Back confirms during a game. Level locks show a friendly message.

## UI/UX

Clear educational style, light theme. Primary sky blue #29B6F6, accent coral #FF7043, background #FFFDF5. The hour hand is short and thick and the minute hand long and thin, in different colours (text labels too, not colour alone). Fonts: Fredoka for numerals, bundled. Large clock (at least 80% screen width), numbers 1–12, minute ticks. Reusable AnalogClock, HandPainter, DigitalTimeLabel.

## FUNCTIONALITY

- Angle ↔ time conversions; the hour hand moves proportionally when the minute hand moves; wrap-around at 12 handled; snapping to 5-minute marks by level.
- Time-to-words generator ("quarter to 5"), question generators with valid distractors, answer checking with tolerance, stars, unlock logic, persistence.

## DATA AND BACKEND

Local only: logic in Dart, progress in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (angle/time conversion, time-to-words, answer tolerance, question generation) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 19. PUZZLE PATH

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 19. PUZZLE PATH

## APPLICATION PURPOSE

Build "Puzzle Path", a Flutter app with a collection of simple puzzles arranged along a path of levels: sliding-picture puzzles, mazes, odd-one-out and picture jigsaws. It develops problem-solving, spatial reasoning and logic. Target users are ages 5–9. Main use case: pick a puzzle type, solve levels of rising difficulty, and earn stars.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional audioplayers. Puzzle images are drawn with Flutter or emoji-based scenes (no photo licences needed). Free and open-source only.

## SCREENS

1. Home – Puzzle Types, My Stars, Settings.
2. Puzzle Type Select – four cards: Slide It, Maze Runner, Odd One Out, Jigsaw.
3. Level Path – per type, 10 levels on a path with locks and stars.
4. Slide It – 3×3 sliding puzzle (2×2 on easy levels) with a picture; tap a tile to slide; move counter; hint shows the target picture.
5. Maze Runner – generated maze (5×5 up to 10×10); drag or swipe the character to the star; a faint hint path option.
6. Odd One Out – a grid of 4–6 pictures where one differs (by shape, colour or category); tap the odd one.
7. Jigsaw – 2×2 up to 3×3 pieces dragged into place with snapping.
8. Level Result – stars by moves/time/hints, Next Level, Retry.
9. My Stars / Settings – totals per type, sound, reset (adult check).

## NAVIGATION

Home → Type Select → Level Path → Puzzle → Result → Level Path/Next. Pause and back open a pause menu (resume, restart, quit).

## UI/UX

Adventure-trail style, light theme. Primary emerald #26A69A, accent amber #FFB74D, background #F0FAF8. Each puzzle type has its own accent colour. Fonts: Fredoka bundled. Large draggable pieces, clear snap/feedback animation, no punishing timers by default. Reusable PuzzleTile, LevelNode, HintButton.

## FUNCTIONALITY

- Sliding puzzle: shuffle by performing random valid moves from the solved state, so every puzzle is solvable; win detection.
- Maze: recursive-backtracker generation (always solvable) with a pathfinding hint; collision handling.
- Odd-one-out generator with rules ensuring exactly one different item; jigsaw snap logic.
- Stars, unlock rules, hints, persistence.

## DATA AND BACKEND

Local only: generators in Dart, progress in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (puzzle solvability, maze generation and pathfinding, odd-one-out uniqueness, scoring) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 20. MUSICAL FINGERS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 20. MUSICAL FINGERS

## APPLICATION PURPOSE

Build "Musical Fingers", a Flutter app that lets children play a virtual piano and drum pads, record short tunes, and follow lit-up keys to learn simple songs. It encourages musical exploration and rhythm. Target users are ages 4–10. Main use case: tap keys and pads to make music, record and replay, and try the song tutor.

## TECHNOLOGY

Flutter, Dart, Android. Audio: low-latency playback with audioplayers (low-latency mode) or flutter_soloud. Piano notes may be synthesised at runtime (generate PCM/WAV in Dart for each note frequency) so no sample files are required; drum sounds use short bundled CC0 samples (the team must source them and list licences in CREDITS.md) or a synthesised fallback. Packages: provider, shared_preferences / path_provider (saved recordings). Free and open-source only.

## SCREENS

1. Home – Piano, Drums, My Recordings, Song Tutor, Settings.
2. Piano – one octave and a half (C4–F5) of white and black keys; multi-touch so chords work; optional note names on keys; octave shift; Record button.
3. Drum Pads – 8 coloured pads (kick, snare, hi-hat, clap, tom, crash…) in a grid; multi-touch; pad glow on tap; Record button.
4. Recorder / Playback bar – records timestamped taps, plays them back with highlighted keys/pads, Save with a name.
5. My Recordings – list with play, rename, delete; empty state.
6. Song Tutor – 3 easy songs (e.g. Twinkle Twinkle, Jingle Bells, Happy Birthday); the next key lights up; the child taps it; a wrong key is gently ignored; a stars screen at the end. (Use public-domain melodies only.)
7. Settings – volume, note labels on/off, key size.

## NAVIGATION

Home → Piano / Drums / Tutor / Recordings; Recorder returns to the instrument after saving; Recordings → Playback. Back works everywhere; leaving a recording asks to save or discard.

## UI/UX

Playful music-studio style, dark-neutral instrument surface with bright pads (dark theme justified for key contrast), or light theme with strong outlines; choose one and apply it consistently. Primary purple #6A1B9A, accent pink #FF4081, background #1F1633, pad colours from a rainbow set. Fonts: Fredoka bundled. Keys at least 48 dp wide, instant visual feedback, no delay on tap. Reusable PianoKey, DrumPad, RecorderBar.

## FUNCTIONALITY

- Note frequency table and tone synthesis with a short attack/decay envelope to avoid clicks; sound pooling for rapid repeated taps.
- Multi-touch handling with Listener pointer events; key press/release visuals.
- Recording: list of (instrument, note/pad, time offset), saved as JSON; playback with timing; song tutor sequence engine with progress.
- Handle audio initialisation failures and report any latency limitations honestly.

## DATA AND BACKEND

Local only: recordings as JSON files, settings in shared_preferences. No backend or credentials. Latency depends on the device; the team should test on a physical Android device where possible and report the result.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (note frequencies, recorder timing model, tutor sequence, recording serialisation) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 21. PATTERN GENIUS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 21. PATTERN GENIUS

## APPLICATION PURPOSE

Build "Pattern Genius", a Flutter game where children find what comes next in colour, shape and number patterns. It builds logical thinking and early algebraic reasoning. Target users are ages 5–9. Main use case: choose a pattern type, solve questions of rising difficulty, and earn Genius badges.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional audioplayers. Shapes and colours drawn with Flutter widgets. Free and open-source only.

## SCREENS

1. Home – Colour Patterns, Shape Patterns, Number Patterns, My Badges, Settings.
2. Level Select – per type, 8 levels (AB, ABB, ABC, AABB … for colours/shapes; +1, +2, +5, ×2 and descending for numbers).
3. Pattern Game – a row of pattern items with a blank ("?"); 3–4 answer choices; drag or tap to fill the blank; 8 questions per level; a progress bar.
4. Explain Screen – after each answer, a short animation highlights the repeating unit or the rule ("add 2 each time").
5. Level Result – stars and unlock.
6. My Badges – Genius badges per type; empty state.
7. Settings – sound, colour-blind-friendly mode (adds patterns/labels to colours), reset (adult check).

## NAVIGATION

Home → Level Select → Game → Explain (inline) → Result → Level Select/Next. Back confirms during a level.

## UI/UX

Bold geometric style, light theme. Primary indigo #3949AB, accent magenta #D81B60, with a distinct, colour-blind-safe palette for pattern colours; background #F5F6FF. Fonts: Fredoka bundled. Big pattern tiles (64 dp+), crisp shapes, smooth snap animation. Reusable PatternRow, ShapeTile, AnswerChoice.

## FUNCTIONALITY

- Pattern generator per type and level: repeating units (colour/shape) and arithmetic/geometric rules (numbers); shows enough repeats so the answer is unambiguous.
- Distractor generator (plausible but wrong, never equal to the answer).
- Rule explanation text per generator; scoring, stars, unlocks, badge rules, persistence.

## DATA AND BACKEND

Local only: generators in Dart, progress in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (pattern generation correctness, unique answer, distractors, scoring) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 22. WHAT'S MISSING?

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 22. WHAT'S MISSING?

## APPLICATION PURPOSE

Build "What's Missing?", a Flutter game in which a group of objects is shown briefly, then hidden, and one is removed; the child must spot which object is missing. It trains short-term visual memory and attention. Target users are ages 4–8. Main use case: play levels with more objects and shorter viewing times, and collect stars.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional audioplayers. Objects are emoji or drawn icons in themed sets (toys, fruits, animals, school items). Free and open-source only.

## SCREENS

1. Home – Play, My Stars, Settings.
2. Level Select – 12 levels: 3 objects up to 8, viewing time decreasing from 8 to 3 seconds; locks and stars.
3. Memorise Phase – objects displayed on a tray/table with a countdown ring and the prompt "Remember them!"; a Ready button to skip ahead.
4. Recall Phase – the tray is covered, then reappears with one object missing; below, an option row shows all objects of the set (the missing one plus distractors); the child taps the missing object; instant feedback with a replay of the original tray.
5. Level Result – 5 rounds per level; stars by correct answers; Retry/Next.
6. My Stars – progress per level; empty state.
7. Settings – memorising time (easy/normal/hard), object set, sound, reset (adult check).

## NAVIGATION

Home → Level Select → Memorise → Recall → (next round) → Result → Level Select/Next. Back opens a confirm dialog during play.

## UI/UX

Magic-show style, light theme with a stage feel. Primary purple #8E24AA, accent gold #FFC107, background #FBF3FF. Fonts: Fredoka bundled. Objects at least 64 dp with generous spacing, an animated cloth cover, a gentle reveal animation. Reusable ObjectTray, CountdownRing, OptionRow.

## FUNCTIONALITY

- Round generator: choose N unique objects from the selected set, randomly remove one, produce options (the missing object plus 2–3 distractors that were not in the tray or were, per difficulty, so the question is unambiguous).
- Timers using elapsed-time logic, skipping, scoring (stars: 5/5 = 3, 4/5 = 2, 3/5 = 1), unlocks, accessibility setting for longer viewing time, persistence.

## DATA AND BACKEND

Local only: object sets in code/JSON, progress in shared_preferences. No backend or credentials.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (round generation, option uniqueness, scoring, unlock rules) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 23. POCKET SCIENCE LAB

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 23. POCKET SCIENCE LAB

## APPLICATION PURPOSE

Build "Pocket Science Lab", a Flutter app that guides children and a supervising adult through simple, safe experiments using household items (sink or float, rainbow in a glass, balloon static, magnet hunt, plants and light, salt crystals and similar). It makes science hands-on and explains why each result happens. Target users are ages 6–12 with an adult present. Main use case: pick an experiment, gather materials, follow the steps, learn the explanation and record the result in a lab journal. Assumption: the app contains only low-risk experiments (no open flame, no strong chemicals, no sharp tools) and shows a safety banner on every experiment.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite (journal), optional flutter_tts. Step illustrations are drawn with Flutter widgets or emoji/CC0 art. Free and open-source only. Experiment content must be verified for safety and accuracy by a teacher before release, and this must be noted in the documentation.

## SCREENS

1. Home – Experiment of the Day, categories (Water, Air, Plants, Magnets, Materials), Lab Journal, Safety Rules.
2. Experiment List – about 12 experiments as cards with time, difficulty and materials count; category filter and search.
3. Experiment Detail – a prominent "Ask a grown-up" safety banner, a materials checklist (tickable), a "What will happen?" prediction prompt (child picks from 3 options), and Start button.
4. Step-by-Step Mode – one step per screen with illustration, short text, an optional timer (e.g. "wait 5 minutes"), and Previous/Next.
5. Why It Works – simple explanation, comparison with the prediction, and a 3-question mini quiz.
6. Lab Journal – completed experiments with date, the child's prediction result, a short note and a star rating; empty state.
7. Safety Rules – illustrated rules for working safely.
8. Settings – text size, sound, reset journal (adult check).

## NAVIGATION

Home → List → Detail → Steps → Why It Works → Journal; Home → Journal; Home → Safety. Leaving step mode asks for confirmation; Android back works throughout.

## UI/UX

Friendly laboratory style, light theme. Primary teal #00ACC1, accent lab orange #FF9100, background #F0FBFD. Fonts: Nunito/Baloo 2 bundled. Large step text (20 sp+), a conspicuous safety banner in a warning colour with an icon, tick animations, 16 dp radii. Reusable ExperimentCard, SafetyBanner, StepView, ChecklistTile.

## FUNCTIONALITY

- Experiment model: title, category, difficulty, duration, materials, steps (text, illustration, optional timer), explanation, quiz, safety notes, in local JSON.
- Checklist state, prediction capture, timers (continue when the screen is locked using elapsed-time logic), mini-quiz scoring, journal CRUD, search and filtering, daily experiment by date.

## DATA AND BACKEND

Local only: JSON content, journal in sqflite / shared_preferences. No backend or credentials. No photos are stored (no camera permission required).

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (content parsing, timers, quiz scoring, journal repository, filtering) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 24. MY DAILY MISSION

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 24. MY DAILY MISSION

## APPLICATION PURPOSE

Build "My Daily Mission", a Flutter app that turns a child's daily routine (morning, school, evening) into a list of "missions" they tick off to earn points, streaks and badges, while a parent can customise the missions. It builds responsibility and independence without conflict. Target users are ages 4–10 and their parents. Main use case: the child opens today's missions, completes them, and watches progress and badges grow. This app differs from a single-topic hygiene app: it supports any routine task chosen by the family. Assumption: one child profile per device.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite (missions and completions), shared_preferences (profile and settings), flutter_local_notifications plus timezone (optional reminders), fl_chart or custom painted bars (weekly report). Free and open-source only.

## SCREENS

1. Welcome / Profile Setup (first launch) – child's first name or nickname (no surname, photo or other personal data), avatar choice, age band (4–6 or 7–10) that loads a starter mission set.
2. Today (Home) – missions grouped Morning / Afternoon / Evening, each with icon, name and a tick control; progress bar; points and streak; a celebration when all are done.
3. Mission Complete – a small animation with points awarded; undo option within a short time.
4. Parent Area (adult check) – mission manager list; add/edit/delete mission (name, icon, time of day, days of week, points).
5. Add/Edit Mission – form with validation (name required, max length).
6. Badges – gallery (First Mission, 3-day streak, 7-day streak, 50 missions, All Done Week…) with locked/unlocked states and progress.
7. Weekly Report – bar chart of completion per day, totals, best streak; empty state.
8. Settings – reminder times, sound, edit profile, reset data (adult check).

States: empty mission list (prompts to add missions), notification permission denied.

## NAVIGATION

Bottom navigation: Today, Badges, Report, Parent Area. Setup runs once and then goes to Today. Back from nested screens returns to the tab; Android back from a tab exits only from Today.

## UI/UX

Sunny, achievement style, light theme. Primary orange #FB8C00, accent blue #1E88E5, background #FFF9F0, surface white. Fonts: Baloo 2 headings, Nunito body, bundled. Large tick targets (56 dp), icons for non-readers, badge shine animation, consistent card style. Reusable MissionTile, BadgeTile, ProgressBarCard, StreakChip.

## FUNCTIONALITY

- Mission repository (CRUD) with recurrence by weekday; per-day completion records; points rules; streak calculation (a day counts when all missions due that day are complete; handle days with no missions and midnight rollover).
- Badge unlock engine evaluated after each completion; weekly aggregation; optional reminders scheduled per time block.
- Starter mission sets per age band (e.g. make the bed, pack the school bag, read for 10 minutes).

## DATA AND BACKEND

Local only: sqflite and shared_preferences; no accounts, cloud or analytics; only a first name or nickname is stored. Design repositories behind interfaces so a synced backend could be added later (and would require a privacy review).

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (streaks, recurrence, badge engine, repository CRUD, weekly aggregation) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 25. SIGN & LEARN KIDS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 25. SIGN & LEARN KIDS

## APPLICATION PURPOSE

Build "Sign & Learn Kids", a Flutter app that introduces children to basic sign-language signs and everyday gestures (fingerspelling, greetings, family, feelings, everyday words) through illustrated flashcards and simple practice games. It promotes inclusion and early communication skills. Target users are ages 5–10 with a parent or teacher. Main use case: browse a category, study the cards, then practise with matching and quiz games. Assumption: because the source gives no specific language, the team chooses ONE sign language (American Sign Language by default) and states it clearly in the app. Accuracy rule: do not invent or guess signs. All sign images and descriptions must come from a reliable, properly licensed source and be reviewed by a qualified signer or a Deaf community member before release. Until reviewed, mark content as "draft – to be verified" in the project documentation.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional audioplayers. Illustrations: team-supplied images or short GIFs with a clear open licence (credit in CREDITS.md) or original drawings created with a signer's guidance. Free and open-source only.

## SCREENS

1. Home – categories (Alphabet, Greetings, Family, Feelings, Everyday Words), Practice, My Progress, About & Credits.
2. Category List – sign cards as a grid with a picture and the word; search.
3. Sign Card (Flashcard) – large illustration, the English word, a short text description of handshape, location and movement, a "Flip" to show the word or the picture, and I Know It / Practise Again buttons.
4. Practice – Match – match 4 sign pictures to their words (drag or tap).
5. Practice – Quiz – "Which word is this sign?" with 3–4 choices; 10 questions; results.
6. My Progress – signs known per category, quiz bests, badges; empty state.
7. About & Credits – the sign language used, the accuracy and review note, content sources and licences, and a respectful note that sign languages differ by country.
8. Settings – text size, reset progress (adult check).

## NAVIGATION

Home → Category → Sign Card (swipe between cards); Home → Practice → Result; Home → Progress; Home → About. Back works everywhere.

## UI/UX

Clear, inclusive, high-contrast style, light theme. Primary deep blue #1565C0, accent warm yellow #FFC107, background #F5F9FF. Fonts: Atkinson Hyperlegible or Nunito, bundled. Very large illustrations (at least 50% of screen height on cards), generous spacing, text alternatives for every image (semantic labels), no colour-only cues. Reusable SignCard, CategoryTile, MatchTile.

## FUNCTIONALITY

- Sign model: id, category, word, image/GIF asset, description, source and licence field, review-status field (draft or reviewed), in local JSON.
- Flashcard flipping, known-tracking, search, match and quiz generators with unambiguous answers, scoring, badges, persistence.
- Handle missing assets with a clear placeholder and log them for the team.

## DATA AND BACKEND

Local only: bundled JSON and assets, progress in shared_preferences. No backend or credentials. No camera or gesture recognition is included, and the app must not claim to recognise or grade the child's signing.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for key logic (content parsing, match/quiz generation, progress tracking, search) and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---
