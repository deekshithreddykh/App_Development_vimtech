# Flutter Prompts - Apps for Working Women

One standalone prompt per page. Give each team only its own page.

Each prompt below is in its own box. Use the copy button on the box to copy just that prompt.

51. DAYFLOW PLANNER
52. SALARY SPLIT SMART
53. SAFEJOURNEY COMPANION
54. MEALPREP MINUTE
55. CAREER LADDER MINI
56. OFFICE OUTFIT PLANNER
57. MEETING MINUTES POCKET
58. BREAKBUDDY
59. COMMUTE COST CALCULATOR
60. WORK EXPENSE POCKET
61. LEAVE BALANCE PLANNER
62. LUNCHBOX IDEA WHEEL
63. SHARED CHORE PLANNER
64. PERSONAL DOCUMENT VAULT
65. INTERVIEW OUTFIT & PREP
66. MEETING CONFIDENCE COACH
67. SKILL SPRINT 15
68. SUBSCRIPTION WATCH
69. SMART ERRAND ROUTE LIST
70. PERIOD & WELLNESS NOTES
71. PERSONAL SAFETY CARD
72. WORKWEAR BUDGET
73. DIGITAL RECEIPT KEEPER
74. WEEKEND RESET
75. ACHIEVEMENT PORTFOLIO

---

## 51. DAYFLOW PLANNER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 51. DAYFLOW PLANNER

## APPLICATION PURPOSE

Build "DayFlow Planner", a Flutter planner that organises office tasks, home responsibilities and personal time in one day view. It solves the problem of work, home and self-care competing in separate lists. Target users are working women; main use case: plan each day across three life areas, see the balance and keep personal time protected. Assumption: the source description is cut off after "in one"; it is read as "in one place".

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, table_calendar, intl.

## SCREENS

1. Today – timeline of items colour-coded by area (Office, Home, Personal) with tick-off, progress per area and a gentle overload banner; empty state with Add prompt.
2. Add/Edit Item – title, area, date, optional start time and duration, priority, repeat (none, daily, weekly), reminder, notes; validation and overlap warning.
3. Week – seven-day overview with hours per area and drag to move items between days.
4. Balance – donut and weekly bars of time by area with a minimum personal-time goal and progress.
5. Recurring – manage repeating routines such as school run or weekly review.
6. Settings – workday hours, personal-time goal, default reminders, theme.

## NAVIGATION

Bottom tabs Today, Week, Balance, Settings; floating Add. Back returns one level; unsaved edits confirm.

## UI/UX

Calm organised style, light and dark. Primary violet #6A4C93, accent coral #FF8A65, background #F8F6FB. Font Inter (bundled). Area colours with icons, 12dp radii. Reusable DayItemTile, AreaChip, BalanceDonut. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Items stored with area and optional time block; overlap detection.
- Repeat rules expand into daily instances; unfinished items offer Move to Tomorrow.
- Hours per area totals; personal-time goal check; reminders rescheduled after edit, boot and restart.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account, cloud, ads or analytics.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for recurrence expansion, overlap detection, area-hour totals and reminder scheduling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 52. SALARY SPLIT SMART

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 52. SALARY SPLIT SMART

## APPLICATION PURPOSE

Build "Salary Split Smart", a Flutter app that divides take-home salary into bills, savings, essentials and flexible spending. It solves the problem of money disappearing before the month ends. Target users are salaried women; main use case: enter take-home pay, set buckets and watch each bucket's remaining balance through the month. Assumption: the source description is cut off after "flexible"; it is read as "flexible spending". All figures are entered by the user and are estimates, not financial advice.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl,

flutter_local_notifications + timezone (optional).

## SCREENS

1. Home – take-home pay, four bucket cards (Bills, Savings, Essentials, Flexible) with allocated, spent and remaining amounts; empty state prompting setup.
2. Split Setup – take-home amount, percentage or fixed amount per bucket, remaining-to-allocate indicator, optional template (for example 50/30/20) with editable values; validation.
3. Fixed Bills – list of recurring bills (name, amount, due day) that are deducted from the Bills bucket first.
4. Add Spend – amount, bucket, category and note with a number pad; warning when a bucket goes over.
5. Month Review – each bucket's planned versus actual, savings rate and a bar chart; copy this month's split to the next.
6. Settings – currency, month start day, overspend alerts, theme, reset.

## NAVIGATION

Bottom tabs Home, Spend, Review, Settings; Setup and Fixed Bills from Home. Back confirms unsaved edits.

## UI/UX

Calm finance style, light and dark. Primary teal #00897B, accent rose #EC407A, background #F4F9F8. Font Manrope (bundled). Progress bars with text values, tabular numerals. Reusable BucketCard, AmountPad, SplitSlider. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Allocation totals must equal take-home pay (or show the unallocated remainder or over-allocation).
- Fixed bills reduce the Bills bucket; spends reduce their bucket; savings rate = savings allocated / take-home.
- Overspend alerts at 80% and 100%; month rollover with copied split; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank link, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for allocation totals and remainder, bucket balances, alert thresholds and month rollover and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 53. SAFEJOURNEY COMPANION

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 53. SAFEJOURNEY COMPANION

## APPLICATION PURPOSE

Build "SafeJourney Companion", a Flutter app for setting a journey check-in time and preparing trusted contacts for emergencies. It gives travellers a simple safety routine and a prompt to act if they do not check in. Target users are working women travelling alone; main use case: share journey details with trusted contacts, set a check-in time and mark Arrived Safely. Limits stated in the app: it cannot send alerts automatically if the phone is off or the user cannot respond, because background SMS sending is restricted on Android; on a missed check-in it prompts the user to contact people, and the user confirms every call or message.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone (check-in alarm), url_launcher (dialer and SMS composer),

share_plus, geolocator (optional one-time location link), wakelock_plus (optional).

## SCREENS

1. Home – Start Journey button, current journey status with countdown, trusted contacts, emergency call button.
2. Trusted Contacts – name, phone and relationship; order of priority; validation.
3. Start Journey – from, to, vehicle or cab note (number and driver details typed by the user), expected arrival, check-in time and grace minutes; Share Details button to send a prepared text through the share sheet or SMS composer, with an optional location link.
4. Active Journey – large countdown, I Have Arrived, Extend Time, and Need Help buttons.
5. Missed Check-In – full-screen alarm prompt: Are you safe? with I'm Safe, Call Contact, Send Message and Call Emergency Number; escalation reminder repeats until answered.
6. Journey History – past journeys with outcomes; delete.
7. Settings – emergency number (entered by the user), grace period, alarm sound and vibration, message template, theme.

## NAVIGATION

Home > Start Journey > Active Journey > Missed Check-In or Arrived; Contacts and History from Home. Back from Active Journey does not cancel the journey; cancelling asks to confirm.

## UI/UX

Reassuring, clear style, light and dark. Primary deep blue #1A237E, accent orange #FF6F00, red #C62828 for the help actions with text, background #F6F7FB. Font Inter (bundled). Large buttons (72dp), calm colours, no clutter. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Check-in alarm scheduled with exact timing where permitted; fallback to inexact with a warning; rescheduled after reboot and restart.
- Escalation prompts at the check-in time and every few minutes after the grace period.
- Prepared message building with optional location; the user confirms sending; handle denied permissions.

## DATA AND BACKEND

Local sqflite and shared_preferences; no server, account or tracking. Test alarms and dialer on a physical device; do not place real emergency calls during testing.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for check-in time and grace logic, escalation scheduling, message building and the contacts repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 54. MEALPREP MINUTE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 54. MEALPREP MINUTE

## APPLICATION PURPOSE

Build "MealPrep Minute", a Flutter app for planning quick meals and organising ingredients into a checklist. It solves the problem of last-minute meal decisions and forgotten ingredients. Target users are busy working women; main use case: pick quick meals for the week and get one merged shopping and prep checklist. Assumption: the team writes about 30 quick recipes (under 30 minutes) in JSON and tests the quantities.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, share_plus, intl.

## SCREENS

1. Week Plan – days with breakfast, lunch and dinner slots; add a meal to a slot; empty state.
2. Recipe Library – quick recipes with time, servings and tags; search and filters (time, vegetarian, ingredient).
3. Recipe Detail – ingredients, steps, a servings scaler, Add to Plan and Favourite; custom recipe creation.
4. Ingredient Checklist – ingredients from all planned meals merged by name and unit, grouped by aisle, with tick-off and Have-At-Home toggle; share as text.
5. Prep Plan – a Sunday prep list: what to chop, cook or marinate ahead for the week.
6. Favourites – saved recipes.
7. Settings – default servings, diet filter, units, theme.

## NAVIGATION

Bottom tabs Plan, Recipes, Checklist, Settings; Detail from lists. Back returns one level.

## UI/UX

Fresh kitchen style, light and dark. Primary green #43A047, accent orange #FB8C00, background #F6FBF4. Font Nunito (bundled). Large recipe cards, tick boxes with text. Reusable MealSlot, RecipeCard, ChecklistRow. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Ingredient merge by normalised name and unit with quantity addition (and clear handling of unit mismatches).
- Servings scaling; checklist state saved; Have-At-Home items excluded from the shopping list.
- Custom recipes; search and filters; persistence.

## DATA AND BACKEND

Bundled JSON, sqflite and shared_preferences; no recipe APIs, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for ingredient merging and unit handling, servings scaling, filters and the plan repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 55. CAREER LADDER MINI

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 55. CAREER LADDER MINI

## APPLICATION PURPOSE

Build "Career Ladder Mini", a Flutter app for tracking skills, interview practice, learning goals and career milestones. It solves the problem of career progress being invisible and unplanned. Target users are working women planning growth; main use case: rate skills, set learning goals, log milestones and practise interview questions in one small app.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart,

flutter_local_notifications + timezone, share_plus, intl.

## SCREENS

1. Dashboard – skills snapshot, active goals with progress, next milestone and a practice streak; empty state.
2. Skills – list with self-rated level 1-5 and target level; add and edit; radar or bar chart of skills; history of rating changes.
3. Learning Goals – goal title, skill link, target date, steps and progress; mark complete.
4. Milestones – dated career events (promotion, certification, project delivered) in a timeline.
5. Interview Practice – question bank (about 40 general questions) with notes for your answer, a self-rating, favourites and a 2-minute timer.
6. Review – a quarterly review screen summarising growth in skills, goals done and milestones; share as text.
7. Settings – review reminder, categories, theme.

## NAVIGATION

Bottom tabs Dashboard, Skills, Goals, Practice, More (Milestones, Review, Settings). Back returns one level.

## UI/UX

Ambitious clean style, light and dark. Primary indigo #3F51B5, accent gold #FFB300, background #F6F7FC. Font Poppins (bundled). Progress bars and level dots with text values. Reusable SkillRow, GoalCard, MilestoneTile. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Skill level history and averages; goal progress from completed steps.
- Practice session selection and self-rating; streak counting.
- Review summary generator; reminders; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud; practice is self-assessed with no AI scoring.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for skill history and averages, goal progress, review summary generation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 56. OFFICE OUTFIT PLANNER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 56. OFFICE OUTFIT PLANNER

## APPLICATION PURPOSE

Build "Office Outfit Planner", a Flutter app for planning outfits for the workweek. It solves the daily "what shall I wear" delay and repeated outfits. Target users are working women; main use case: record wardrobe items, assemble outfits and assign them to weekdays.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, image_picker (optional item photos stored locally), path_provider, flutter_local_notifications + timezone, intl.

## SCREENS

1. Week – Monday to Friday cards showing the planned outfit, laundry warnings and a Plan Week button; empty state.
2. Wardrobe – items by category (tops, bottoms, dresses, outerwear, shoes, accessories) with photo or colour swatch; search and filters (colour, occasion, season); laundry status.
3. Add/Edit Item – name, category, colour, occasion tags, season, optional photo, last worn date; validation.
4. Outfit Builder – choose items to form an outfit; save outfits with a name and occasion; preview collage of photos or swatches.
5. Assign Outfit – pick a day and an outfit; warnings if an item is in the laundry or was worn in the last N days.
6. Laundry – items marked in the wash and mark clean.
7. Settings – repeat-wear threshold, evening reminder, theme.

## NAVIGATION

Bottom tabs Week, Wardrobe, Outfits, Settings. Back returns one level; unsaved edits confirm.

## UI/UX

Stylish clean style, light and dark. Primary plum #7B1FA2, accent rose gold #E8A598, background #FBF7FA. Font Poppins (bundled). Photo grids, rounded 16dp cards, colour names with swatches. Reusable ItemTile, OutfitCard, DayCard. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Item and outfit CRUD; last-worn updated when a planned day passes or is marked worn.
- Warnings for laundry and recent repeats; filter combinations.
- Evening reminder to check tomorrow's outfit; persistence of photos in the app folder.

## DATA AND BACKEND

Local sqflite, app-folder photos and shared_preferences; no account, cloud or social sharing.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for repeat-wear and laundry warnings, filters, outfit repository and last-worn updates and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 57. MEETING MINUTES POCKET

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 57. MEETING MINUTES POCKET

## APPLICATION PURPOSE

Build "Meeting Minutes Pocket", a Flutter app that captures meeting notes, decisions and action items. It solves the problem of decisions and follow-ups being forgotten. Target users are working women in teams; main use case: take structured notes in a meeting and track the resulting actions.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, share_plus, intl.

## SCREENS

1. Meetings – recent and upcoming meetings with open-action counts; search; empty state; New Meeting.
2. New/Edit Meeting – title, date and time, attendees (names), agenda, template; validation.
3. Minutes Editor – sections Notes, Decisions, and Action Items (task, owner name, due date); quick-add buttons for each; autosave draft.
4. Meeting Detail – formatted minutes; Share as text; duplicate for a recurring meeting.
5. Action Tracker – all actions across meetings with filters by owner, status and due date; mark done.
6. Templates – weekly team, project review, one-to-one, client call.
7. Settings – default reminder for due actions, theme.

## NAVIGATION

Bottom tabs Meetings, Actions, Templates, Settings; floating New Meeting. Back confirms unsaved drafts.

## UI/UX

Professional organised style, light and dark. Primary blue #1E88E5, accent amber #FFB300, background #F5F8FC. Font Inter (bundled). Clear section headers, check boxes, owner chips. Reusable MinutesSection, ActionRow, MeetingCard. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Structured minutes saved per meeting; action items with owner text and due dates.
- Reminders before due dates; overdue highlighting.
- Plain-text and shareable formatting; duplicate and carry unfinished actions into a new meeting; search.

## DATA AND BACKEND

Local sqflite and shared_preferences; no calendar sync, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for action filters and overdue logic, minutes text formatting, carry-forward and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 58. BREAKBUDDY

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 58. BREAKBUDDY

## APPLICATION PURPOSE

Build "BreakBuddy", a Flutter app that schedules short screen and movement breaks. It helps desk workers reduce eye strain and sitting time. Target users are working women at a desk; main use case: start a work session, get break prompts and follow a quick stretch or eye-rest exercise. Prompts are general wellbeing tips, not medical advice.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences,

flutter_local_notifications + timezone, fl_chart, wakelock_plus.

## SCREENS

1. Home – work-session toggle, time to next break, today's breaks taken and a quick Take a Break Now button.
2. Schedule – break types (eye rest 20-20-20, stand and stretch, walk, water) with intervals, active hours and quiet hours; validation.
3. Break Session – a guided card with a short illustrated exercise and a visual countdown; Done and Snooze.
4. Exercise Library – illustrated desk stretches (neck, shoulders, wrists, back, eyes) with steps.
5. History – breaks taken versus planned per day and week; chart.
6. Settings – sound, vibration, snooze length, theme.

## NAVIGATION

Bottom tabs Home, Library, History, Settings; notifications open the Break Session. Back returns one level.

## UI/UX

Light refreshing style, light and dark. Primary teal #00ACC1, accent coral #FF7043, background #F2FAFC. Font Nunito Sans (bundled). Big Done button, calm animations with a reduced-motion option. Reusable BreakCard, ExerciseTile, CountdownRing. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Interval scheduling within active hours; rescheduled after edits, boot and restart; Android 13+ permission.
- Done and Snooze from the notification; history aggregation.
- Exercise library from JSON reviewed by the team; persistence.

## DATA AND BACKEND

Local storage only; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for scheduling within active hours, snooze logic, history aggregation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 59. COMMUTE COST CALCULATOR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 59. COMMUTE COST CALCULATOR

## APPLICATION PURPOSE

Build "Commute Cost Calculator", a Flutter app that compares estimated commuting costs by transport type. It helps a working woman choose the most affordable way to travel to work. Target users are daily commuters; main use case: enter costs for each option and compare daily, monthly and yearly cost and time. All figures are entered manually; the app has no fare or map services.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, fl_chart, intl.

## SCREENS

1. Compare – cards or bars for each transport type with cost per day, month and year and travel time, with Cheapest and Fastest tags; empty state.
2. Setup – commute name, working days per month and trips per day.
3. Option Editor – bus or metro (fare per trip or pass price), own two-wheeler or car (distance, mileage, fuel price, parking, maintenance per km), cab or auto (fare per trip), walking or cycling; travel time; validation.
4. Pass Break-Even – pass price versus pay-per-ride.
5. Saved Commutes – saved comparisons such as Home to Office.
6. Settings – currency, distance units, theme.

## NAVIGATION

Bottom tabs Compare, Saved, Settings; Option Editor from Compare. Back confirms unsaved edits.

## UI/UX

Practical travel style, light and dark. Primary blue #1565C0, accent green #2E7D32, background #F3F6FB. Font Work Sans (bundled). Mode icons with text labels, big totals. Reusable OptionCard, CostBar, ModeIcon. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Vehicle cost per trip = distance / mileage x fuel price + parking + distance x maintenance rate.
- Day, month and year totals; cheapest and fastest ranking; pass break-even trips.
- Empty-field and zero-division handling; persistence.

## DATA AND BACKEND

Local storage only; no maps, fare APIs, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for per-trip cost, totals, break-even and ranking and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 60. WORK EXPENSE POCKET

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 60. WORK EXPENSE POCKET

## APPLICATION PURPOSE

Build "Work Expense Pocket", a Flutter app that records work-related spending and its reimbursement status. It solves the problem of paying out of pocket and losing track of what is owed back. Target users are working women who claim expenses; main use case: log each expense with a receipt photo and follow it from pending to reimbursed.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, image_picker (optional receipt photo stored locally), path_provider, share_plus, fl_chart, intl.

## SCREENS

1. Dashboard – amount owed back (not yet reimbursed), totals by status, recent expenses; empty state.
2. Add/Edit Expense – amount, date, category (Travel, Meals, Supplies, Client, Other), vendor, project or claim label, optional receipt photo, notes, status; validation.
3. Expenses – list with filters by status, category, date and project; search.
4. Claims – group expenses into a claim batch with a claim name, submitted date and status (Draft, Submitted, Approved, Reimbursed, Rejected).
5. Claim Detail – expenses in the claim, total, status history and Share Summary as text.
6. Reports – monthly spend by category, outstanding amount ageing (0-30, 31-60, over 60 days).
7. Settings – currency, categories, reminder for old unreimbursed claims, CSV export.

## NAVIGATION

Bottom tabs Dashboard, Expenses, Claims, Reports; floating Add. Back returns one level.

## UI/UX

Tidy business style, light and dark. Primary indigo #303F9F, accent teal #00ACC1, background #F5F6FB. Font Inter (bundled). Status chips with icon and text, tabular numbers. Reusable ExpenseTile, StatusChip, ClaimCard. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Status flow per expense or claim with dates; outstanding amount = approved or submitted but not yet reimbursed.
- Ageing buckets; reminders for old claims; CSV export; photos in the app folder.
- Validation and persistence.

## DATA AND BACKEND

Local sqflite, app-folder photos and shared_preferences; no employer system, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for outstanding totals, ageing buckets, status transitions and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 61. LEAVE BALANCE PLANNER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 61. LEAVE BALANCE PLANNER

## APPLICATION PURPOSE

Build "Leave Balance Planner", a Flutter app that calculates leave days from manually entered balances. It helps a working woman plan time off without exceeding her balance. Target users are employees; main use case: enter current balances per leave type, plan upcoming leave and see what remains. Policies differ by employer, so all balances, accrual and holiday dates are entered by the user and the app does not claim to match any company's rules.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, table_calendar,

flutter_local_notifications + timezone, intl.

## SCREENS

1. Overview – balance per leave type (Casual, Sick, Annual, Other) with taken, planned and remaining; empty state prompting setup.
2. Leave Types – add or edit a type with opening balance, optional monthly accrual and carry-forward limit; validation.
3. Plan Leave – leave type, start and end dates, half-day option, note; shows working days used and the balance after the leave; warning if negative.
4. Calendar – leave days, weekends and holidays marked; month view.
5. Holidays & Weekends – the user's weekly off days and a list of holiday dates.
6. History – taken and planned leave with edit and delete; status Planned, Taken or Cancelled.
7. Settings – year start month, reminders for upcoming leave, theme.

## NAVIGATION

Bottom tabs Overview, Calendar, History, Settings; floating Plan Leave. Back returns one level.

## UI/UX

Calm planning style, light and dark. Primary teal #00796B, accent amber #FFA000, background #F4F9F8. Font Nunito Sans (bundled). Balance bars with numbers, leave types with colour and text. Reusable BalanceCard, LeaveRow, DayCell. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Working days = days between the dates minus weekly off days and holidays (half-day counts 0.5).
- Remaining = opening + accrued - taken - planned; carry-forward cap at year end.
- Overlap detection between leaves; reminders; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no employer link, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for working-day counting with holidays and half days, balance and accrual, overlap detection and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 62. LUNCHBOX IDEA WHEEL

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 62. LUNCHBOX IDEA WHEEL

## APPLICATION PURPOSE

Build "Lunchbox Idea Wheel", a Flutter app that suggests meals from ingredients already available and lets the user spin a wheel to decide. It solves the daily lunchbox decision. Target users are working women packing lunch; main use case: select what is in the kitchen, see matching ideas and spin when undecided. Assumption: about 50 simple lunchbox recipes written by the team in JSON.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite, intl.

## SCREENS

1. Home – ingredient chips with autocomplete, time filter, a Show Ideas button and a Spin the Wheel button; empty state.
2. Ideas – ranked meal cards with match percentage, time and missing ingredients.
3. Spin Wheel – an animated wheel of the top matches (or favourites) that lands on one idea; Spin Again and Accept.
4. Recipe Detail – ingredients (have or missing), steps, packing tips; Favourite; Add Missing to List.
5. Pantry – saved staples always counted as available.
6. Shopping List – missing items with check-off.
7. Settings – vegetarian filter, excluded ingredients, theme.

## NAVIGATION

Bottom tabs Home, Pantry, Favourites, List; Settings from the app bar. Back keeps the ingredient state.

## UI/UX

Playful food style, light and dark. Primary orange #F57C00, accent green #7CB342, background #FFF9F0. Font Nunito (bundled). Colourful wheel segments with text labels, big cards. Reusable IdeaCard, WheelWidget, IngredientChip. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Ingredient normalisation and match score = matched required ingredients / total required.
- Wheel selection weighted by match, with the animation ending exactly on the chosen segment.
- Pantry staples, filters, shopping list; persistence.

## DATA AND BACKEND

Bundled JSON and local storage; no recipe APIs, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for normalisation, match scoring, weighted wheel selection and filters and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 63. SHARED CHORE PLANNER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 63. SHARED CHORE PLANNER

## APPLICATION PURPOSE

Build "Shared Chore Planner", a Flutter app that divides household tasks among family members or housemates. It solves unfair or forgotten chores. Target users are families and flatmates; main use case: list chores, assign them fairly and tick them off. Assumption: single-device use (one phone is passed around or shared by showing the schedule); there is no sync between phones, and the schedule can be shared as text or an image.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, share_plus, intl.

## SCREENS

1. This Week – each person's chores for the week with ticks and a progress bar; empty state.
2. Members – add, edit and remove people (name, colour, optional availability days).
3. Chores – list with name, frequency (daily, weekly, monthly or one-off), effort points (1-5) and assigned person; add and edit; validation.
4. Assign – manual assignment, Rotate (cycle through people each period) or Balance (assign the next chore to the person with the fewest points).
5. Fairness – chart of effort points per person for the week and month.
6. Chore Detail – history of who did it and when; skip or swap.
7. Settings – week start day, reminders, theme.

## NAVIGATION

Bottom tabs Week, Chores, Fairness, Members; Settings from the app bar. Back returns one level.

## UI/UX

Friendly household style, light and dark. Primary teal #26A69A, accent coral #FF7043, background #F3FAF9. Font Nunito (bundled). Person colour chips with initials, big tick boxes. Reusable ChoreTile, MemberChip, FairnessBar. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Weekly instances generated from frequencies; rotation and balancing algorithms.
- Completion log; swap and skip; points totals; reminders to assignees (text list as the person is not identified by device).
- Export schedule as text; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no accounts, cloud or sync.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for rotation, balancing, weekly instance generation and points totals and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 64. PERSONAL DOCUMENT VAULT

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 64. PERSONAL DOCUMENT VAULT

## APPLICATION PURPOSE

Build "Personal Document Vault", a Flutter app that organises document details and expiry reminders locally. It solves the problem of scattered papers and missed renewals. Target users are working women; main use case: record each document's type, where it is kept and its expiry date and get reminders. Privacy rule: the app stores only the type, a label, where the original is kept, the expiry date, and an optional short reference such as the last four characters - never full document numbers or scans - and warns the user not to enter them.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, flutter_secure_storage (database key), local_auth (optional app lock), flutter_local_notifications + timezone, intl. Reminders must be rescheduled after reboot.

## SCREENS

1. Vault – documents grouped by category (Identity, Travel, Finance, Insurance, Property, Education, Other) with status chips; search; empty state.
2. Add/Edit Document – type, label, category, where kept (for example "blue file, top shelf"), issue and expiry dates, reminder offsets, notes; validation and privacy hint.
3. Document Detail – days left, renewal checklist, Mark Renewed with new dates, delete with confirm.
4. Expiring Soon – documents expiring in 90 days sorted by date.
5. Lock Setup – turn on the biometric or device-credential lock and an auto-lock delay.
6. Settings – default reminders, reminder time (notification text kept discreet), block screenshots, theme.

## NAVIGATION

Bottom tabs Vault, Expiring, Settings; floating Add. The lock screen appears first if enabled. Back returns one level.

## UI/UX

Secure calm style, light and dark. Primary navy #283593, accent teal #00ACC1, background #F5F6FB. Font Inter (bundled). Status by icon and text, discreet visuals. Reusable DocCard, StatusChip, LockGate. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Status from expiry date (expired, soon, valid); multiple reminders; reschedule on edit, renewal, boot and restart.
- Lock and unlock flow with a fallback when no device lock exists; screenshot blocking option.
- Renewal history; validation and persistence.

## DATA AND BACKEND

Local encrypted database key in secure storage; no scans, full numbers, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for status calculation, reminder dates, lock gating logic and the document repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 65. INTERVIEW OUTFIT & PREP

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 65. INTERVIEW OUTFIT & PREP

## APPLICATION PURPOSE

Build "Interview Outfit & Prep", a Flutter app for preparing interview checklists and practising questions. It helps a candidate arrive organised and confident. Target users are working women interviewing for jobs; main use case: create an interview, work through the outfit and preparation checklists and rehearse questions. Practice is self-assessed; there is no AI scoring.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, share_plus, intl.

## SCREENS

1. Interviews – upcoming and past interviews with a readiness percentage; empty state; Add Interview.
2. Add/Edit Interview – company, role, date and time, format (in person, phone, video), location or link text, interviewer names, notes; validation.
3. Checklists – for each interview: Outfit (clothes ready, shoes, bag, grooming, backup items), Documents (CV copies, certificates, ID, portfolio), Research (company, role, questions to ask) and Logistics (route, travel time, arrival plan, charger and water).
4. Question Bank – about 40 common questions by category with a space for your answer, a self-rating and favourites.
5. Practice Session – random questions with an optional 2-minute timer and a reveal of the saved answer; session summary.
6. Day-Before Plan – a night-before and morning-of timeline checklist with reminders.
7. Settings – default reminders, theme.

## NAVIGATION

Bottom tabs Interviews, Questions, Practice, Settings. Back returns one level.

## UI/UX

Confident clean style, light and dark. Primary indigo #3949AB, accent rose #EC407A, background #F6F7FC. Font Poppins (bundled). Progress rings with percentages, calm tick animations. Reusable ChecklistGroup, QuestionCard, ReadinessRing. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Checklist templates copied per interview; readiness = ticked items / total.
- Reminders for the day-before plan and the interview time; practice selection favouring low-rated questions.
- Answer notes, favourites, text sharing; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences, bundled JSON; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for readiness calculation, template copying, practice selection weighting and reminder scheduling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 66. MEETING CONFIDENCE COACH

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 66. MEETING CONFIDENCE COACH

## APPLICATION PURPOSE

Build "Meeting Confidence Coach", a Flutter app for practising introductions, presentations and workplace conversations. It helps a user speak up with confidence. Target users are working women building speaking confidence; main use case: prepare a short script, rehearse it with a timer, record and listen back, and rate her own delivery. The app gives structure and self-review, not automated speech scoring.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, record and audioplayers

(optional local audio recording and playback), path_provider, flutter_tts (optional model pronunciation), intl.

## SCREENS

1. Home – today's practice suggestion, practice streak and quick Start Practice.
2. Scenarios – Introduce Yourself, Share an Update, Ask a Question in a Meeting, Disagree Politely, Present an Idea, Handle a Tough Conversation, Negotiate a Request.
3. Script Builder – templates with prompts (for example Who I am, what I do, one strength) to fill in; edit, save and reorder scripts.
4. Rehearse – large text script, a target-time timer, optional audio recording with a microphone permission explanation; Pause, Restart and Finish.
5. Review – play the recording, then self-rate delivery (pace, clarity, volume, structure, eye contact) with notes; compare with the last attempt.
6. Tips Library – short cards on opening strongly, handling nerves and structuring a talk.
7. Progress – attempts, average self-ratings and streak.
8. Settings – default target time, recording on or off, delete all recordings, theme.

## NAVIGATION

Bottom tabs Home, Scenarios, Progress, Tips; Script Builder and Rehearse from Scenarios. Back confirms exit mid-rehearsal.

## UI/UX

Encouraging confident style, light and dark. Primary purple #6A1B9A, accent orange #FF8F00, background #FAF6FC. Font Poppins (bundled). Large script text, calm timer ring, no pressure messaging. Reusable ScenarioCard, ScriptEditor, RatingRow. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Script storage; timer based on elapsed time; recording saved in the app folder with delete option.
- Self-rating history and comparison; streak; tips from reviewed JSON.
- Permission handling for the microphone; persistence.

## DATA AND BACKEND

Local sqflite, shared_preferences and app-folder audio; recordings never leave the device; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for timer logic, rating history comparison, script repository and recording-permission handling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 67. SKILL SPRINT 15

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 67. SKILL SPRINT 15

## APPLICATION PURPOSE

Build "Skill Sprint 15", a Flutter app delivering short 15-minute daily lessons in Excel, communication and digital skills. It helps busy women build job skills in small daily steps. Target users are working women; main use case: complete one lesson a day, practise, and keep a learning streak. Assumption: the source description is cut off after "digital"; it is read as "digital skills". The team writes about 8 original lessons per track (24 total) in JSON and has them reviewed.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences,

flutter_local_notifications + timezone. A small formula evaluator written in Dart for the Excel practice.

## SCREENS

1. Home – today's lesson card, streak, weekly progress; all-done state.
2. Tracks – Excel, Communication, Digital Skills with progress bars.
3. Lesson List – lessons with completion ticks and estimated minutes.
4. Lesson Player – swipeable cards (explanation, example, tip) with a progress bar and an approximate 15-minute indicator; bookmark.
5. Formula Practice (Excel track) – a mini grid of sample data and a task (for example "total column B"); the user types a formula supporting SUM, AVERAGE, MIN, MAX, COUNT, IF and basic arithmetic, and the app checks the result with hints.
6. Quiz & Result – 4-5 questions per lesson; pass at 70%; explanations.
7. Progress – streak, lessons completed, badges, bookmarks.
8. Settings – daily reminder time, preferred track, theme.

## NAVIGATION

Bottom tabs Home, Tracks, Progress; Settings from Home. Lesson > Practice or Quiz > Result > Home. Back confirms mid-lesson.

## UI/UX

Focused learning style, light and dark. Primary green #2E7D32, accent magenta #D81B60, background #F6FBF6. Font Nunito Sans (bundled). 18sp lesson text, spreadsheet cells in a monospace font, high contrast. Reusable LessonCard, MiniGrid, QuizOption. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Lesson JSON model; daily lesson = next unfinished lesson in the preferred track.
- Formula evaluator parses and calculates supported functions and cell ranges safely; wrong formulas give friendly hints.
- Quiz scoring, streak, badges, reminders; persistence.

## DATA AND BACKEND

Bundled JSON and local progress; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for formula evaluator (SUM, AVERAGE, IF, ranges, errors), daily lesson selection, quiz scoring and streak logic and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 68. SUBSCRIPTION WATCH

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 68. SUBSCRIPTION WATCH

## APPLICATION PURPOSE

Build "Subscription Watch", a Flutter app that tracks subscriptions, their costs and renewal dates. It solves the problem of forgotten recurring payments. Target users are working women; main use case: list every subscription, see the monthly and yearly total and get reminded before renewals. The app only records and reminds; it never cancels or pays anything.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, intl.

## SCREENS

1. Overview – monthly and yearly totals, donut by category, next three renewals; empty state.
2. Subscriptions – list with cost, cycle, next renewal and status; search and filters.
3. Add/Edit Subscription – name, cost, billing cycle (weekly, monthly, quarterly, yearly), next renewal date, category, payment method note, free-trial end date, notes, reminder lead days; validation.
4. Renewals – a calendar and list of upcoming renewals by date.
5. Review – for each subscription, mark Keep, Review or Cancel with a usage rating; potential savings from items marked Cancel.
6. Settings – currency, default reminder days, theme.

## NAVIGATION

Bottom tabs Overview, List, Renewals, Review; Settings from the app bar. Back returns one level.

## UI/UX

Clean money-aware style, light and dark. Primary purple #7B1FA2, accent green #2E7D32 for savings, background #FAF6FC. Font DM Sans (bundled). Cycle and status chips with text. Reusable SubTile, RenewalRow, SavingsBanner. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Costs normalised to monthly and yearly; next-renewal roll-forward after the date passes.
- Free-trial end reminders; reminders rescheduled on edit, boot and restart.
- Savings from Cancel marks; search and filters; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank or email access, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for cost normalisation, renewal roll-forward, savings totals and reminder scheduling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 69. SMART ERRAND ROUTE LIST

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 69. SMART ERRAND ROUTE LIST

## APPLICATION PURPOSE

Build "Smart Errand Route List", a Flutter app that groups errands by area for easier trip planning. It solves the problem of zig-zagging across town for small tasks. Target users are busy working women; main use case: add errands with their areas, group them into efficient trips and tick them off on the way. Assumption: no routing service is used; the user labels areas and may enter an area order, and a stop with an address can open the phone's map app.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, url_launcher (open the map app from an address), share_plus, intl.

## SCREENS

1. Errands – list grouped by area with priority and estimated time; empty state; Add Errand.
2. Add/Edit Errand – title, area (choose or create), optional address, priority, estimated minutes, preferred day, notes; validation.
3. Trip Planner – select errands (or auto-select today's), arrange areas in the order entered by the user, and see the grouped plan with total estimated time and a "can't fit before" warning against the available hours.
4. Trip Mode – a step-by-step list of stops by area with tick-off, Open in Maps (if an address exists) and Skip or Move to Tomorrow.
5. Areas – add, rename, delete and order areas.
6. History – completed errands and trips.
7. Settings – available hours, default estimate, theme.

## NAVIGATION

Bottom tabs Errands, Trip, History, Settings; floating Add. Back returns one level.

## UI/UX

Practical organised style, light and dark. Primary teal #00897B, accent orange #FF7043, background #F3F9F8. Font Work Sans (bundled). Area colour chips with text, large tick boxes. Reusable ErrandTile, AreaHeader, StopCard. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Grouping by area with area order; trip time = sum of estimates plus a user-set travel allowance per area change.
- Move or skip errands; open the map for a stop's address with a geo or maps URL.
- Share the plan as text; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no maps SDK, routing API, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for grouping and ordering, trip-time calculation, move or skip logic and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 70. PERIOD & WELLNESS NOTES

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 70. PERIOD & WELLNESS NOTES

## APPLICATION PURPOSE

Build "Period & Wellness Notes", a Flutter app for optional, private cycle and wellness tracking stored locally. It helps a user keep her own notes and see her own patterns. Target users are women who want a private diary; main use case: log periods and optional daily notes, and see simple history. The app is a personal diary, not a medical tool: predictions are simple averages of the user's own entries, it is not for contraception or diagnosis, and it tells users to ask a health professional about health concerns. Privacy is central.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite with an encryption key held in flutter_secure_storage (or an encrypted store), local_auth (app lock), flutter_local_notifications + timezone, table_calendar,

fl_chart, intl.

## SCREENS

1. Lock – biometric or device-credential unlock if enabled; otherwise opens directly.
2. Calendar – month view with logged period days, optional symptom markers and a soft estimate of the next period (hidden until at least 3 cycles are logged).
3. Log Day – period on or off, flow level, optional symptoms and mood from the user's own list, notes; edit past days.
4. History – cycle lengths and period lengths from the user's entries with simple averages; chart.
5. Insights – the user's most-logged symptoms per cycle day, shown as plain counts.
6. Reminders – optional, with discreet notification wording.
7. Privacy – plain explanation of local storage, an export to a file the user chooses, and Delete All Data with confirm.
8. Settings – lock, auto-lock, block screenshots, custom symptom list, theme.

## NAVIGATION

Bottom tabs Calendar, History, Insights, Settings; Log Day from the calendar. Back returns one level; the app locks after the delay.

## UI/UX

Gentle private style, light and dark. Primary rose #AD1457, accent teal #00897B, background #FFF8FA. Font Nunito (bundled). Soft colours, symptom markers with text, neutral app icon and name option so it is discreet. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Cycle length from consecutive period starts; average and range; estimate shown as a window, never as a guarantee.
- Encrypted local storage; lock gating; export and delete-all.
- Reminders with neutral text such as "Reminder"; validation and persistence.

## DATA AND BACKEND

Local encrypted storage only; no cloud, account, analytics or sharing. Never write health data to logs.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for cycle statistics and the estimate window, lock gating, encryption repository and delete-all and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 71. PERSONAL SAFETY CARD

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 71. PERSONAL SAFETY CARD

## APPLICATION PURPOSE

Build "Personal Safety Card", a Flutter app that keeps emergency contacts and useful safety instructions accessible. It helps users act quickly in an unsafe situation and share key details with people who can help. Target users are working women; main use case: prepare the card once, then open it fast to call someone or show instructions. The app does not replace emergency services; helpline numbers are editable, with 112 pre-filled as a default for India and other numbers added by the user after verifying them.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, url_launcher (dialer and SMS composer), local_auth (optional lock), share_plus.

## SCREENS

1. Card – large buttons for each emergency contact and helpline with tap-to-dial, a Send Help Message button (opens the SMS composer with a prepared text), and the user's safety notes below.
2. Contacts – name, phone, relationship and order; at least one prompted on first run; validation.
3. Helplines – editable list (general emergency, police, women's helpline, local numbers) with notes; the user verifies and edits the numbers.
4. Safety Instructions – the user's own short instructions (what to do, who to tell, where to go) plus starter tips such as sharing a journey with someone.
5. Show Card – full-screen large text of key information (name, contacts, instructions) to show someone.
6. Settings – optional lock, confirmation or press-and-hold before calling, message template, theme.

## NAVIGATION

Card is home; other screens from the app bar or tabs. Back returns one level.

## UI/UX

Clear reassuring style, light and dark. Primary deep red #B71C1C for emergency actions, accent blue #1565C0, background #FFFFFF. Font Inter (bundled). Very large buttons (80dp), high contrast, hold-to-call option to avoid accidental calls. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Tap or hold opens the dialer with the number pre-filled; the user presses call.
- Prepared SMS opened with the user's text; handle missing handlers and permissions.
- Optional app lock; validation and persistence.

## DATA AND BACKEND

Local storage only; no cloud, account or tracking. Test on a physical device; do not place real emergency calls during testing.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for contact ordering and validation, message building, lock gating and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 72. WORKWEAR BUDGET

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 72. WORKWEAR BUDGET

## APPLICATION PURPOSE

Build "Workwear Budget", a Flutter app for setting spending limits for clothing and accessories. It helps keep wardrobe spending intentional. Target users are working women; main use case: set a budget, record purchases and see how much of each limit remains. Figures are entered by the user.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl,

flutter_local_notifications + timezone (optional).

## SCREENS

1. Home – total budget remaining for the period, category bars (Clothing, Footwear, Bags and Accessories, Jewellery, Alterations) and recent purchases; empty state.
2. Set Budget – period (month, quarter or season), total limit and optional category limits; warning when category limits exceed the total; validation.
3. Add Purchase – item, amount, category, date, store and an optional "planned or impulse" flag; warning if it exceeds a limit.
4. Wishlist – items wanted with price and priority; move to purchases when bought; shows affordability against the remaining budget.
5. History – purchases by period with filters; edit and delete.
6. Insights – spending by category, planned versus impulse split and cost-per-wear estimate if wears are entered.
7. Settings – period start, alert thresholds (80% and 100%), currency, theme.

## NAVIGATION

Bottom tabs Home, Wishlist, History, Insights; Set Budget and Settings from Home. Back returns one level.

## UI/UX

Elegant calm style, light and dark. Primary plum #6A1B9A, accent gold #FFB300, background #FBF7FC. Font Poppins (bundled). Progress bars with numbers, soft cards. Reusable BudgetBar, PurchaseTile, WishlistRow. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Remaining = limit - spent per category and overall; alerts at thresholds.
- Wishlist affordability = price vs remaining budget; period rollover.
- Cost per wear = price / wears; filters; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank link, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for budget remaining and alerts, wishlist affordability, period rollover and cost-per-wear and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 73. DIGITAL RECEIPT KEEPER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 73. DIGITAL RECEIPT KEEPER

## APPLICATION PURPOSE

Build "Digital Receipt Keeper", a Flutter app that saves receipt photos and organises them by category. It solves the problem of lost receipts needed for returns, warranties and expenses. Target users are working women; main use case: photograph a receipt, tag the details and find it later by search or category. Photos stay on the device.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, image_picker (camera or gallery), path_provider, image (resize and compress), share_plus, local_auth (optional lock), intl.

## SCREENS

1. Receipts – grid or list with thumbnail, merchant, amount and date; search; filters by category, month and tag; empty state; Add Receipt.
2. Add/Edit Receipt – photo from camera or gallery with a preview, merchant, amount, date, category, optional warranty end date and return-by date, tags, notes; validation.
3. Receipt Detail – full-screen photo with zoom, details, reminders for return or warranty dates, share, delete with confirm.
4. Categories – add, rename and delete categories.
5. Reports – monthly totals by category; chart; CSV export.
6. Settings – photo quality, optional lock, reminder lead days, theme, delete all.

## NAVIGATION

Bottom tabs Receipts, Reports, Settings; floating Add. Back returns one level.

## UI/UX

Tidy organised style, light and dark. Primary teal #00897B, accent amber #FFA000, background #F4F9F8. Font DM Sans (bundled). Photo thumbnails with rounded corners, labelled filters. Reusable ReceiptTile, CategoryChip, ZoomImage. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Photos compressed and copied into the app folder; thumbnails cached.
- Search by merchant, tag and notes; filter combinations; totals by category and month.
- Return-by and warranty reminders; CSV export of details (not photos); validation and persistence.

## DATA AND BACKEND

Local sqflite and app-folder images; no cloud, OCR service, account or analytics.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for search and filters, totals, reminder dates and the receipt repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 74. WEEKEND RESET

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 74. WEEKEND RESET

## APPLICATION PURPOSE

Build "Weekend Reset", a Flutter app that prepares a simple checklist for the coming workweek. It helps a user start Monday organised and calm. Target users are working women; main use case: run through a short reset checklist on Sunday and capture the week's key priorities.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences,

flutter_local_notifications + timezone, intl.

## SCREENS

1. Reset – this weekend's checklist grouped as Home, Work, Food, Self-care and Family with progress; empty state with a default list.
2. Checklist Editor – add, edit, reorder and hide items; item groups and repeat each week; validation.
3. Week Preview – the next seven days with the user's own notes for each day and the top three priorities of the week.
4. Prep – quick toggles: bag packed, outfits chosen, meals planned, laundry done, calendar reviewed.
5. Reflection – a short optional prompt (what went well, what to let go) saved per week.
6. History – past weekends' completion percentages and reflections.
7. Settings – reset reminder day and time, template items, theme.

## NAVIGATION

Bottom tabs Reset, Preview, History, Settings. Back returns to the tab.

## UI/UX

Calm restful style, light and dark. Primary soft teal #4DB6AC, accent peach #FFAB91, background #F6FBFA. Font Nunito Sans (bundled). Gentle progress bars, uncluttered layout. Reusable ChecklistGroup, PriorityRow, ReflectionCard. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- Weekly checklists generated from a template and reset each weekend; carry-over option for unfinished items.
- Progress per group and overall; weekly priorities and day notes saved; reminder scheduling.
- Reflections and history; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for weekly reset and carry-over, progress calculation, reminder scheduling and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 75. ACHIEVEMENT PORTFOLIO

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 75. ACHIEVEMENT PORTFOLIO

## APPLICATION PURPOSE

Build "Achievement Portfolio", a Flutter app for recording completed projects, certificates and career accomplishments. It solves the problem of forgetting wins and evidence when updating a CV or preparing for a review. Target users are working women; main use case: log achievements with details and evidence, then export a portfolio summary.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, image_picker (certificate images), file_picker (optional PDF reference), pdf and printing (export a portfolio PDF), share_plus, intl.

## SCREENS

1. Portfolio – achievements by year with type chips (Project, Certificate, Award, Promotion, Learning, Other); search; empty state; Add Achievement.
2. Add/Edit Achievement – title, type, date, description, measurable result, skills used, links as text, optional certificate image or file; validation.
3. Achievement Detail – full details and evidence; edit and delete with confirm.
4. Skills View – achievements grouped by skill with counts.
5. Export – choose date range and types, preview, and create a PDF or plain-text portfolio to share.
6. Insights – achievements per year, type breakdown and top skills; chart.
7. Settings – types list, export template (name and headline typed by the user), theme.

## NAVIGATION

Bottom tabs Portfolio, Skills, Insights, Settings; floating Add. Back returns one level.

## UI/UX

Polished confident style, light and dark. Primary navy #1A237E, accent gold #FFB300, background #F6F7FC. Font Poppins (bundled). Timeline layout with year headings, certificate thumbnails. Reusable AchievementCard, TypeChip, ExportPreview. Designed for busy daily use: quick-add in a few taps, readable text scaling, 48dp+ touch targets, discreet notification wording for private data, and full offline use.

## FUNCTIONALITY

- CRUD with type and skill filters; full-text search.
- Evidence files copied into the app folder; PDF generation with a clean layout; text export.
- Aggregations by year, type and skill; validation and persistence.

## DATA AND BACKEND

Local sqflite, app-folder files and shared_preferences; no account or cloud; sharing only when the user presses Share.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for filters and search, aggregations, export text and PDF generation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---
