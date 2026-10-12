# Flutter Prompts - Apps for Auto Drivers

One standalone prompt per page. Give each team only its own page.

Each prompt below is in its own box. Use the copy button on the box to copy just that prompt.

76. AUTOHISAB
77. MILEAGE MATE
78. AUTOCARE CALENDAR
79. RIDETALK KANNADA
80. DAILY TARGET METER
81. FARE SPLIT CALCULATOR
82. CNG & PETROL COST COMPARE
83. TRIP EXPENSE DIARY
84. AUTO DOCUMENT CHECKLIST
85. VEHICLE LOAN EMI HELPER
86. MAINTENANCE MONEY BOX
87. BREAKTIME DRIVER
88. TRAFFIC SIGN TUTOR
89. ACCIDENT ACTION GUIDE
90. PASSENGER LOST & FOUND
91. UPI PAYMENT CHECKER
92. SHIFT COMPARISON
93. DAILY CASH RECONCILER
94. TYRE CARE GUIDE
95. ENGINE WARNING GUIDE
96. RAINY RIDE CHECKLIST
97. DRIVER HEALTH BREAKS
98. LOCAL LANDMARK CARDS
99. PASSENGER FEEDBACK NOTES
100. DAILY TRIP COUNTER

---

## 76. AUTOHISAB

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 76. AUTOHISAB

## APPLICATION PURPOSE

Build "AutoHisab", a Flutter app for auto-rickshaw drivers to record trips, fares and expenses and see daily net earnings. It solves the problem of not knowing what was really earned after fuel, parking and other costs. Target users are auto drivers; main use case: tap in each fare as it is earned, add expenses during the day and read the net total at the end. Amounts are in Indian rupees (Rs).

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl, share_plus (CSV export). Fully offline.

## SCREENS

1. Today – gross fares, expenses, net earnings, trip count and a list of today's entries; big Add Trip and Add Expense buttons; empty state.
2. Add Trip – fare amount with a number pad, payment mode (Cash or UPI), optional distance and note; validation (amount greater than zero).
3. Add Expense – amount, category (Fuel, Parking, Toll, Repair, Food, Other) and note.
4. Day Log – entries for any chosen date with edit and delete (confirm); date picker.
5. Reports – weekly and monthly gross, expense and net totals; bar chart; best day.
6. Settings – business-day start hour (so night shifts past midnight stay in one day), default categories, theme, CSV export, reset with confirm.

## NAVIGATION

Bottom tabs Today, Log, Reports, Settings. Add screens open as full-screen sheets. Back returns to the tab; unsaved entries confirm.

## UI/UX

Simple, sunlight-readable style, light and dark. Primary green #2E7D32, accent amber #FFB300, background #F7FAF4. Font Noto Sans (bundled). Very large numbers, big buttons, number-pad entry with minimal typing. Reusable AmountPad, SummaryCard, EntryTile. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Net = sum of fares - sum of expenses for the business day.
- Cash and UPI totals shown separately; entries editable and deletable.
- Weekly and monthly aggregation; CSV export.
- Validation, undo for the last deleted entry, persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account, cloud, ads or analytics; no payment integration.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for business-day assignment, net calculation, aggregation and the entry repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 77. MILEAGE MATE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 77. MILEAGE MATE

## APPLICATION PURPOSE

Build "Mileage Mate", a Flutter app that calculates kilometres per litre (or per kg for CNG), fuel cost per kilometre and mileage trends. It solves the problem of not knowing whether the vehicle's fuel efficiency is getting worse. Target users are auto drivers; main use case: log each fill-up with the odometer reading and see mileage and running cost per kilometre. Assumption: the source description is cut off after "mileage"; trends are included.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl. Fully offline.

## SCREENS

1. Home – latest mileage, average mileage, cost per km, and last fill-up; Add Fill-up button; empty state.
2. Add Fill-up – date, odometer (km), fuel quantity, price per unit or total amount, full-tank toggle; validation (odometer must be higher than the last reading).
3. History – fill-ups with the mileage computed for each full-tank interval; edit and delete with confirm.
4. Stats – mileage trend line chart, cost-per-km trend, best and worst intervals.
5. Settings – fuel type (Petrol, CNG in kg, LPG in litres), units label, currency, theme, reset.

## NAVIGATION

Bottom tabs Home, History, Stats, Settings; floating Add Fill-up. Back returns one level.

## UI/UX

Practical dashboard style, light and dark. Primary teal #00796B, accent orange #FB8C00, background #F4F9F8. Font Noto Sans (bundled). Big values, simple charts with text labels. Reusable StatTile, FillUpRow, TrendChart. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Mileage = distance between two full-tank fill-ups / fuel added at the later fill-up; partial fills accumulate until the next full tank.
- Cost per km = fuel cost over the interval / distance.
- Average over all intervals and over the last five; warnings for odometer errors.
- Persistence and validation.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for full-tank interval mileage with partial fills, cost per km, odometer validation and averages and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 78. AUTOCARE CALENDAR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 78. AUTOCARE CALENDAR

## APPLICATION PURPOSE

Build "AutoCare Calendar", a Flutter app that tracks servicing, oil changes, tyre checks and insurance expiry dates and reminds the driver in time. It solves the problem of missed servicing and lapsed insurance, which cost money and safety. Target users are auto drivers and small fleet owners; main use case: set up recurring tasks once and log each completion.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, table_calendar, intl. Reminders must be rescheduled after reboot.

## SCREENS

1. Dashboard – overdue, due soon and upcoming tasks with days or kilometres left; empty state with starter tasks.
2. Calendar – month view with task and expiry markers; day list.
3. Add/Edit Task – type (Service, Oil Change, Tyre Check, Insurance Expiry, Other), interval by days or kilometres, last done date and odometer, reminder lead time; validation.
4. Task Detail – next due, history of completions, Mark Done.
5. Log Service – date, odometer, cost, garage, note; completing a task resets its next due.
6. Settings – default lead times, reminder time, current odometer, theme.

## NAVIGATION

Bottom tabs Dashboard, Calendar, History, Settings; floating Add. Back returns one level.

## UI/UX

Clear maintenance style, light and dark. Primary blue #1565C0, accent red #E53935 for overdue and amber #FFA000 for soon, background #F4F7FB. Font Noto Sans (bundled). Status by icon and text, large tap areas. Reusable TaskCard, DueChip, ServiceRow. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Next due = last done + interval (days) or odometer + interval (km), whichever applies; the current odometer is updated by the user.
- Overdue and due-soon detection; reminders by date; reschedule on edit, completion, boot and restart.
- Service history and cost totals; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for next-due by date and by kilometres, overdue detection, reminder scheduling and repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 79. RIDETALK KANNADA

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 79. RIDETALK KANNADA

## APPLICATION PURPOSE

Build "RideTalk Kannada", a Flutter phrasebook that displays useful passenger phrases in Kannada, English and Hindi. It solves the problem of language gaps between drivers and passengers. Target users are auto drivers and passengers; main use case: find a phrase, show it large to the passenger and optionally play it aloud. Assumption: the team writes about 100 phrases in Kannada script, Hindi script and English with Roman transliteration, and has native speakers review them before release.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences (favourites), flutter_tts (uses installed Kannada and Hindi voices when available). Bundle Noto Sans Kannada and Noto Sans Devanagari fonts (OFL). Fully offline.

## SCREENS

1. Home – categories, search, favourites, recently used.
2. Categories – Greetings, Where To, Directions (left, right, straight, stop here), Fare and Meter, Payment and UPI, Waiting and Luggage, Politeness, Small Talk, Problems and Safety.
3. Phrase List – phrases in the chosen languages with transliteration; search across all languages; favourite toggle.
4. Phrase Display – very large text of the phrase in the chosen language for showing to a passenger; Play button; swipe to the next phrase.
5. Favourites – saved phrases for quick access.
6. Settings – displayed languages, show transliteration, text size, speech on or off, theme.

## NAVIGATION

Home > Category > Phrase List > Phrase Display; Favourites and Settings from Home. Back returns one level.

## UI/UX

Friendly, high-contrast style, light and dark. Primary orange #E65100, accent deep green #1B5E20, background #FFF8F0. Fonts Noto Sans Kannada and Noto Sans Devanagari (bundled). Large script text, language labels, 56dp touch targets. Reusable PhraseCard, LanguageTabs, BigPhraseView. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Phrase JSON (id, category, Kannada, Hindi, English, transliterations).
- Search across all languages and transliteration; favourites and recents.
- Text-to-speech with a clear message if no voice for the language is installed; text never fails to display.

## DATA AND BACKEND

Bundled JSON and local storage; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for multi-language search, favourites storage, content parsing and missing-voice handling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 80. DAILY TARGET METER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 80. DAILY TARGET METER

## APPLICATION PURPOSE

Build "Daily Target Meter", a Flutter app where the driver sets a daily earning target and sees progress after each trip. It solves the problem of not knowing how far through the day's goal they are. Target users are auto drivers; main use case: set a target, add each fare and watch the meter fill. Assumption: the target can be measured on gross fares or on net earnings after expenses, chosen in settings.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl,

flutter_local_notifications + timezone (optional evening summary).

## SCREENS

1. Meter – large circular or horizontal meter with earned, target and remaining amounts; Add Fare button with number pad; Add Expense (for net mode); encouraging text when close.
2. Set Target – daily target amount, weekday-specific targets option, gross or net mode; validation.
3. Today's Entries – fares and expenses with edit and delete.
4. History – past days with target met or not, amount earned, and streak of target days.
5. Insights – weekly average, best weekday, bar chart against target.
6. Settings – business-day start hour, reminder, theme, reset.

## NAVIGATION

Meter is home; bottom tabs Meter, History, Insights, Settings. Back returns one level.

## UI/UX

Motivating dashboard style, light and dark. Primary green #388E3C, accent amber #FFC107, background #F6FAF4. Font Noto Sans (bundled). Huge numbers, meter colours paired with percentages, simple celebration at 100%. Reusable TargetMeter, AmountPad, DayRow. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Progress = earned / target (gross) or (earned - expenses) / target (net); can exceed 100%.
- Target per weekday and history of targets; streak of days meeting the target.
- Weekly averages and best weekday; reminders optional; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for progress in gross and net mode, weekday targets, streak logic and history aggregation and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 81. FARE SPLIT CALCULATOR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 81. FARE SPLIT CALCULATOR

## APPLICATION PURPOSE

Build "Fare Split Calculator", a Flutter app that calculates fare shares for a shared journey. It solves the arguments and mental maths when several passengers share one auto. Target users are drivers and passengers; main use case: enter the total fare and the passengers, pick a split method and show each person's share. The app is a calculator only: fares are entered by the user and shared-ride rules vary by city.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, intl, share_plus. Fully offline.

## SCREENS

1. Calculator – total fare, number of passengers or named passengers, split method selector, results list with each share and the total.
2. Split by Distance – drop-off points with distance from the start for each passenger, so longer riders pay more of the shared stretch.
3. Custom Shares – set each person's percentage or fixed amount; remaining amount indicator.
4. Result – large display of shares and a rounding option (exact, nearest Rs 1, Rs 5 or Rs 10) with the difference shown; Share as text.
5. Recent Splits – saved calculations to review.
6. Settings – default rounding, currency, theme.

## NAVIGATION

Bottom tabs Calculator, Recent, Settings. Back returns one level.

## UI/UX

Clean calculator style, light and dark. Primary indigo #3949AB, accent amber #FFB300, background #F6F7FB. Font Noto Sans (bundled). Very large result digits, number pad, high contrast for daylight. Reusable ShareRow, MethodChip, NumberPad. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Equal split = total / n with remainder handled so shares add up to the total.
- Distance split: each segment's cost divided among the passengers still riding that segment.
- Custom split validation (shares must total 100% or the fare); rounding with the difference shown.
- Saved history; validation and persistence.

## DATA AND BACKEND

Local shared_preferences or sqflite; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for equal split with remainders, segment-based distance split, custom share validation and rounding and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 82. CNG & PETROL COST COMPARE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 82. CNG & PETROL COST COMPARE

## APPLICATION PURPOSE

Build "CNG & Petrol Cost Compare", a Flutter app that compares estimated running costs using entered fuel prices and mileage. It helps a driver decide between fuel types or judge whether a conversion is worth it. Target users are auto drivers and owners; main use case: enter prices and mileage for each fuel and see cost per kilometre and per month. Assumption: the source description is cut off after "and"; mileage and daily distance are the other inputs, and all prices are entered by the user because they change.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, fl_chart, intl. Fully offline.

## SCREENS

1. Compare – side-by-side cards for each fuel (Petrol, CNG, LPG) with price, mileage, cost per km, daily and monthly cost, and the cheapest highlighted.
2. Fuel Inputs – price per litre or kg and mileage in km per litre or kg for each fuel; daily distance and working days per month; validation.
3. Conversion Payback – optional conversion cost entered by the user, monthly saving and months to recover the cost.
4. Scenarios – save named comparisons (for example "Current prices", "If CNG rises").
5. What If – change a price with a slider and watch the comparison update.
6. Settings – currency, units, theme, reset.

## NAVIGATION

Bottom tabs Compare, Scenarios, Settings; Conversion Payback and What If from Compare. Back returns one level.

## UI/UX

Clear comparison style, light and dark. Primary teal #00897B, accent orange #FF7043, background #F3F9F8. Font Noto Sans (bundled). Big cost-per-km numbers, bars with text values. Reusable FuelCard, CostBar, ScenarioTile. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Cost per km = price / mileage; monthly cost = cost per km x daily km x days.
- Cheapest fuel flagged; payback months = conversion cost / monthly saving (hidden if there is no saving).
- Saved scenarios and slider-driven what-if; input validation and zero-division handling.

## DATA AND BACKEND

Local storage only; no live price feed, account or cloud. State that prices are the user's own entries.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for cost per km, monthly cost, payback calculation and scenario repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 83. TRIP EXPENSE DIARY

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 83. TRIP EXPENSE DIARY

## APPLICATION PURPOSE

Build "Trip Expense Diary", a Flutter app for recording parking, tolls, repairs and other operating costs. It solves the problem of small expenses being forgotten and undercounted. Target users are auto drivers; main use case: add each expense in seconds and review the month's costs by category.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl, share_plus. Fully offline.

## SCREENS

1. Diary – today's expenses with the total and quick-add buttons for common categories; empty state.
2. Add Expense – amount with a number pad, category (Parking, Toll, Repair, Fuel, Fine, Food, Other), date, payment mode, optional note; validation.
3. Expense List – entries by date with filters by category and month; edit and delete with confirm; search notes.
4. Reports – monthly total, category donut and daily bar chart; top categories.
5. Categories – add, rename and hide categories.
6. Settings – currency, default categories, theme, CSV export, reset.

## NAVIGATION

Bottom tabs Diary, List, Reports, Settings; floating Add. Back returns one level.

## UI/UX

Simple ledger style, light and dark. Primary slate #455A64, accent orange #F57C00, background #F5F6F7. Font Noto Sans (bundled). Big number pad, category icons with text, high contrast. Reusable ExpenseTile, CategoryChip, AmountPad. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Expense CRUD with quick-add favourites; totals by day, month and category.
- Filters, search and CSV export; validation (amount > 0).
- Persistence and undo for deletion.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for totals by category and month, filters, CSV format and the expense repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 84. AUTO DOCUMENT CHECKLIST

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 84. AUTO DOCUMENT CHECKLIST

## APPLICATION PURPOSE

Build "Auto Document Checklist", a Flutter app that tracks the driver's licence, vehicle registration, insurance, permit and other required documents. It solves the problem of expired or missing papers during checks. Target users are auto drivers; main use case: tick off the documents carried and track every expiry date with reminders. Privacy rule: the app stores only document type, a short optional reference (such as the last four characters), the expiry date and notes - never full document numbers or scans.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, intl. Reminders must be rescheduled after reboot.

## SCREENS

1. Checklist – documents with a "carrying today" tick and a status chip (Valid, Due Soon, Expired, Missing); progress such as 5 of 6 ready; empty state with starter documents.
2. Add/Edit Document – type (Driving Licence, Registration Certificate, Insurance, Permit, Pollution Certificate, Fitness Certificate, Other), short reference (optional), issue and expiry dates, reminder offsets, notes; validation and privacy hint.
3. Document Detail – days left, history of renewals, Mark Renewed with the new expiry.
4. Expiry Calendar – dates by month with the nearest expiry highlighted.
5. Settings – default reminders (60, 30, 7 days), reminder time, theme.

## NAVIGATION

Bottom tabs Checklist, Calendar, Settings; floating Add. Back returns one level.

## UI/UX

Clear compliance style, light and dark. Primary blue #1565C0, accent red #D32F2F for expired and amber #FFA000 for soon, background #F3F6FB. Font Noto Sans (bundled). Status by icon and text; big tick boxes. Reusable DocTile, StatusChip, ProgressBanner. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Status from expiry date (Expired, within 30 days, valid); missing if not recorded.
- Daily "carrying" ticks reset each morning; multiple reminders per document; reschedule on edit, renewal, boot and restart.
- Renewal updates expiry and keeps history; validation.

## DATA AND BACKEND

Local sqflite and shared_preferences; no scans, full numbers, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for status calculation, daily tick reset, reminder dates and the renewal flow and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 85. VEHICLE LOAN EMI HELPER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 85. VEHICLE LOAN EMI HELPER

## APPLICATION PURPOSE

Build "Vehicle Loan EMI Helper", a Flutter app that estimates monthly instalments and total loan payments. It helps a driver understand the real cost of a vehicle loan before or during borrowing. Target users are auto drivers and owners; main use case: enter the loan amount, interest rate and tenure and see the instalment, total interest and repayment schedule. The app is an estimator only; actual lender terms, fees and rounding differ.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, fl_chart, intl, share_plus. Calculations in a pure-Dart service.

## SCREENS

1. Calculator – loan amount, annual interest rate, tenure in months or years, interest method (Reducing Balance or Flat Rate); results for EMI, total interest and total payment; validation.
2. Schedule – month-by-month table of instalment, interest, principal and balance (reducing balance) with totals.
3. Compare Loans – up to three offers side by side, including EMI, total cost and the effective annual rate of a flat-rate offer.
4. Prepayment – effect of a one-time extra payment or higher EMI on tenure and total interest.
5. Saved Loans – saved scenarios with names.
6. Settings – currency, theme, reset.

## NAVIGATION

Bottom tabs Calculator, Compare, Saved, Settings; Schedule and Prepayment from Calculator. Back returns one level.

## UI/UX

Clean financial-tool style, light and dark. Primary navy #1A237E, accent teal #00ACC1, background #F5F6FB. Font Noto Sans (bundled). Big result figures, tabular numbers, text labels on charts. Reusable ResultCard, ScheduleTable, OfferCard. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Reducing balance EMI = P x r x (1 + r)^n / ((1 + r)^n - 1), r = annual rate / 12 / 100; handle zero rate.
- Flat rate: interest = P x rate x years; EMI = (P + interest) / months; effective rate found by numerical solving.
- Prepayment recalculation, amortisation schedule, input limits and validation.

## DATA AND BACKEND

Local storage only; no lender link, account or cloud. State clearly that results are estimates.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for EMI formula with known values, zero-rate case, flat versus effective rate and prepayment effect and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 86. MAINTENANCE MONEY BOX

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 86. MAINTENANCE MONEY BOX

## APPLICATION PURPOSE

Build "Maintenance Money Box", a Flutter app that helps a driver save a portion of earnings toward future repairs. It solves the problem of large repair bills arriving with no money set aside. Target users are auto drivers; main use case: set aside a small amount each day, watch the box grow toward named repair goals and record spending when a repair happens. The box is a record only; no real money is held or moved.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, intl.

## SCREENS

1. Box – current balance, goals with progress bars, and a big Add to Box button; empty state.
2. Add to Box – amount, date and note; quick buttons for the usual daily amount.
3. Set-Aside Rule – choose a fixed daily amount or a percentage of the day's earnings; weekday options.
4. Goals – goals such as tyres, battery or engine service with target amounts and optional dates; allocate money to goals.
5. Spend from Box – record a repair spend against a goal or the general box; balance cannot go below zero.
6. History – deposits and spends with filters; chart of balance over time.
7. Settings – evening reminder, currency, theme, reset.

## NAVIGATION

Bottom tabs Box, Goals, History, Settings. Back returns one level.

## UI/UX

Encouraging savings style, light and dark. Primary green #2E7D32, accent gold #FFC107, background #F4FAF4. Font Noto Sans (bundled). Big balance, progress bars with percentages. Reusable BalanceCard, GoalBar, TransactionRow. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Balance = deposits - spends; goal progress from allocated money.
- Percentage rule applied to an entered day's earnings; suggested amount shown, never added automatically.
- Evening "set aside today" reminder; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank link, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for balance and goal allocation, percentage rule, spend limits and reminder scheduling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 87. BREAKTIME DRIVER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 87. BREAKTIME DRIVER

## APPLICATION PURPOSE

Build "BreakTime Driver", a Flutter app for planning work sessions, meals and rest breaks. It helps drivers avoid skipping meals and rest during long days. Target users are auto drivers; main use case: plan the day's blocks, receive reminders and log breaks actually taken. Suggested interval defaults are editable and are not medical advice.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart.

## SCREENS

1. Day Plan – timeline of work sessions, meals and breaks with the current block highlighted; Start Break and Skip buttons; empty state with a default plan.
2. Edit Plan – add, edit and reorder blocks (type, start time, length); templates such as Morning Shift and Night Shift; validation of overlaps.
3. Break Timer – countdown for a break in progress with a clear End Break button.
4. Reminders – choose which reminders (meal, rest, end of day) and their lead time.
5. History – breaks planned versus taken per day and week; chart.
6. Settings – default block lengths, reminder sounds and vibration, theme.

## NAVIGATION

Bottom tabs Plan, History, Settings; Edit Plan and Break Timer from Plan. Back returns one level.

## UI/UX

Calm practical style, light and dark. Primary blue #0277BD, accent green #43A047, background #F3F8FB. Font Noto Sans (bundled). Large current-block card, icons with text for meal, rest and work. Reusable BlockTile, BreakCountdown, ReminderChip. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Plan generation from a template and editable blocks; overlap detection.
- Timestamp-based break timer that survives backgrounding; reminders rescheduled after edits, boot and restart.
- Log of planned versus taken breaks; weekly summary.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for overlap detection, timer logic, reminder scheduling and the history repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 88. TRAFFIC SIGN TUTOR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 88. TRAFFIC SIGN TUTOR

## APPLICATION PURPOSE

Build "Traffic Sign Tutor", a Flutter app for learning road signs and their meanings. It helps drivers refresh their knowledge and prepare for licence or renewal tests. Target users are auto drivers and learners; main use case: browse signs by group, learn meanings and test with quizzes. Assumption: signs follow the categories used on Indian roads (mandatory, cautionary and informatory); the team draws them in Flutter and checks them against the official standards, and the app tells users the official rules apply.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, optional flutter_tts. Signs drawn with CustomPainter (not copied images).

## SCREENS

1. Home – groups, quiz, progress, bookmarks.
2. Sign Groups – Mandatory (regulatory), Cautionary (warning), Informatory, Road Markings.
3. Sign List – sign pictures with names; search; bookmarks.
4. Sign Detail – large drawn sign, name, meaning, when it applies and a driver tip; Listen button.
5. Quiz – "What does this sign mean?" and "Which sign means...?" with 4 choices; 10 or 20 questions; result with explanations.
6. Progress – signs learned, quiz scores, weak groups.
7. Settings – text size, speech, theme, language labels.

## NAVIGATION

Home > Group > List > Detail; Home > Quiz > Result. Back returns one level.

## UI/UX

Clear road-theme style, light and dark. Primary blue #1565C0, accent yellow #FDD835, with red and green only where the sign requires them, background #F5F8FC. Font Noto Sans (bundled). Large signs with text names, never colour alone. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Sign model drawn in code (shape, colours, symbol, meaning, group).
- Search, bookmarks, learned tracking, weak-group detection.
- Quiz generator without repeats and plausible distractors; scores saved.

## DATA AND BACKEND

Bundled content and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for quiz generation, learned tracking, search and weak-group calculation and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 89. ACCIDENT ACTION GUIDE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 89. ACCIDENT ACTION GUIDE

## APPLICATION PURPOSE

Build "Accident Action Guide", a Flutter app that shows a clear step-by-step checklist for responding to an accident. It helps a driver stay calm and do the important things in order. Target users are auto drivers; main use case: open the guide after an accident and follow it step by step, with one-tap calling. The app is general guidance, not legal or medical advice; the team must have the steps reviewed, and emergency numbers are editable (112 is pre-filled as a default for India, to be verified).

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, url_launcher (open the dialer), share_plus, intl. Fully offline.

## SCREENS

1. Home – a large "I had an accident" button, emergency call buttons, and My Contacts.
2. Step-by-Step Guide – one step per screen with a big Done button and Back: stay calm, move to safety, switch off the engine, check for injuries, call emergency services, do not move seriously injured people, switch on hazard signals, take photos, note details, inform the insurer, keep calm with others.
3. Emergency Numbers – editable numbers (general emergency, ambulance, police) with tap-to-dial that opens the dialer.
4. My Contacts – family, insurer and garage contacts.
5. Incident Notes – date and time, place text, vehicles involved, witness names, damage notes, insurer reported; save and share as text.
6. Settings – text size, theme, reset.

## NAVIGATION

Home > Guide > Incident Notes; Numbers and Contacts from Home. Back returns one level; the guide can be resumed.

## UI/UX

Calm high-visibility style, light and dark. Primary red #C62828 for the emergency button, accent blue #1565C0, background #FFFFFF. Font Noto Sans (bundled). Large type, single-action screens, no clutter. Reusable StepCard, CallButton, NoteForm. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Steps loaded from JSON; progress remembered if the guide is closed.
- Dialer opened with the number pre-filled (the driver presses call); handle missing dialer.
- Incident notes saved and shared as plain text; validation.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud. Do not place real emergency calls during testing.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for step progression and resume, number validation, note text generation and the notes repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 90. PASSENGER LOST & FOUND

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 90. PASSENGER LOST & FOUND

## APPLICATION PURPOSE

Build "Passenger Lost & Found", a Flutter app for recording items found in the vehicle and the steps taken to return them. It helps drivers handle belongings honestly and keep a record. Target users are auto drivers; main use case: log a found item immediately, note every step taken and mark it returned or handed over.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, image_picker (optional photo stored locally), path_provider, flutter_local_notifications + timezone, share_plus, intl.

## SCREENS

1. Items – found items with status chip and age; empty state; Add Item.
2. Add Item – description, date and time found, route or place, optional photo, optional passenger name or phone if known, storage place; validation.
3. Item Detail – timeline of steps taken, status, notes; Add Step and Change Status.
4. Add Step – step type (tried to call, asked nearby stand, informed police station, contact passed on), date and note.
5. Returned / Handed Over – date, person's name, handover note; item moves to Closed.
6. Closed Items – returned items archive.
7. Settings – follow-up reminder days, theme, reset.

## NAVIGATION

Bottom tabs Items, Closed, Settings; floating Add. Back returns one level.

## UI/UX

Honest, simple style, light and dark. Primary teal #00796B, accent amber #FFA000, background #F4F9F8. Font Noto Sans (bundled). Status by icon and text, large buttons. Reusable ItemCard, StepTile, StatusChip. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Status flow: Found, Contact attempted, Returned or Handed to police.
- Follow-up reminders until the item is closed; step history; share item details as text.
- Photos copied into the app folder; validation and persistence.

## DATA AND BACKEND

Local sqflite and app-folder photos; no account or cloud; personal details optional and kept on the device.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for status transitions, follow-up reminder logic, step history and the item repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 91. UPI PAYMENT CHECKER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 91. UPI PAYMENT CHECKER

## APPLICATION PURPOSE

Build "UPI Payment Checker", a Flutter app with a checklist to verify payment status and avoid screenshot scams. It helps a driver confirm money has actually arrived before the passenger leaves. Target users are auto drivers; main use case: run the quick checklist at each UPI payment and read what to do if something looks wrong. The app has no connection to UPI, banks or SMS: it is a checklist and guide only. Helpline numbers are editable; 1930 (India's national cyber crime helpline) is pre-filled and must be verified by the team.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences, url_launcher (dialer), intl. Fully offline.

## SCREENS

1. Quick Check – large checklist for a payment: open the bank or UPI app and see the credit, amount matches the fare, payer details match, do not rely on a screenshot, wait for the sound box or credit message, then tick Received or Not Received.
2. Red Flags – illustrated list of common scams (fake or edited screenshots, "wrong transfer" refund requests, collect requests, fake payment apps) with how to spot each.
3. If Something Goes Wrong – steps: do not refund until the credit is confirmed, note details, tell your bank, report to the cyber crime helpline with tap-to-dial.
4. Payment Log – optional record of each check (time, amount, Received or Not Received, note); totals by day.
5. Settings – helpline numbers, text size, theme, reset log.

## NAVIGATION

Bottom tabs Check, Red Flags, Help, Log, Settings. Back returns one level.

## UI/UX

Clear trustworthy style, light and dark. Primary green #2E7D32 for received and red #C62828 for not received (with icon and text), accent blue #1565C0, background #F6FAF6. Font Noto Sans (bundled). Big tick boxes, one screen per decision, sunlight-readable. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Checklist state per payment; the Received button enables only when the key checks are ticked.
- Log with daily totals of received and not received.
- Scam tips loaded from JSON reviewed by the team; dialer opened with the number pre-filled.

## DATA AND BACKEND

Local sqflite and shared_preferences; no payment, bank or SMS access, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for checklist gating logic, log totals, content parsing and the log repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 92. SHIFT COMPARISON

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 92. SHIFT COMPARISON

## APPLICATION PURPOSE

Build "Shift Comparison", a Flutter app that compares earnings and expenses across work shifts. It helps a driver see which shift (morning, afternoon, night) pays best per hour. Target users are auto drivers; main use case: log each shift's hours, fares, expenses and trips and compare shifts over a period.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl.

## SCREENS

1. Compare – bar charts of net earnings per hour, trips per hour and average net per shift, with the best shift highlighted; period selector (7, 30, 90 days).
2. Log Shift – date, shift (Morning, Afternoon, Evening, Night or custom), hours worked, gross fares, expenses and trip count; validation.
3. Shift History – logged shifts with edit and delete (confirm).
4. Shift Detail – averages and best and worst days for one shift type.
5. Shifts – manage shift names and typical hours.
6. Settings – currency, default period, theme, CSV export.

## NAVIGATION

Bottom tabs Compare, Log, History, Settings. Back returns one level.

## UI/UX

Analytical but simple style, light and dark. Primary indigo #3949AB, accent orange #FB8C00, background #F6F7FB. Font Noto Sans (bundled). Big numbers, colour-coded shifts with text labels. Reusable ShiftBar, StatCard, ShiftRow. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Net = gross - expenses; net per hour = net / hours; trips per hour.
- Aggregation per shift type over the chosen period; best-shift ranking with minimum data warning (fewer than 3 logs).
- CSV export; validation (hours between 0.5 and 24); persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for per-hour calculations, aggregation, ranking with sparse data and the shift repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 93. DAILY CASH RECONCILER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 93. DAILY CASH RECONCILER

## APPLICATION PURPOSE

Build "Daily Cash Reconciler", a Flutter app that compares the cash collected with recorded fares and expenses. It helps a driver confirm the day's cash is correct and spot mistakes. Target users are auto drivers; main use case: enter fares and expenses during the day, count the cash at night and see whether it matches.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, intl, share_plus.

## SCREENS

1. Today – opening cash, cash fares, UPI fares (shown separately and excluded from the cash total), cash expenses and the expected cash; Reconcile button; empty state.
2. Add Fare / Expense – amount, payment mode (cash or UPI), category and note for the fare or expense; validation.
3. Count Cash – a counter for each note and coin (Rs 500, 200, 100, 50, 20, 10 and coins of 10, 5, 2, 1, configurable) with plus and minus buttons and a running total.
4. Result – expected versus counted cash, with Matches, Short or Over and the difference; space to note the reason and save.
5. History – past reconciliations with differences; filters; chart of differences.
6. Settings – denominations, opening-cash carry-forward, business-day start hour, theme.

## NAVIGATION

Bottom tabs Today, Count, History, Settings. Back returns one level; unsaved counts confirm.

## UI/UX

Clear ledger style, light and dark. Primary teal #00796B, accent amber #FFA000, red #D32F2F for shortfalls with text, background #F4F9F8. Font Noto Sans (bundled). Large counters and totals, high contrast. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Expected cash = opening cash + cash fares - cash expenses.
- Difference = counted - expected, with a tolerance setting for small rounding.
- Denomination totals; carry the counted cash forward as tomorrow's opening cash on request.
- Persistence and validation.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank link, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for expected cash calculation, denomination totals, difference and tolerance logic and the reconciliation repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 94. TYRE CARE GUIDE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 94. TYRE CARE GUIDE

## APPLICATION PURPOSE

Build "Tyre Care Guide", a Flutter app that stores tyre pressure specifications and inspection dates and guides routine tyre checks. It helps a driver keep tyres safe and last longer. Target users are auto drivers; main use case: save the recommended pressures from the vehicle manual, record each inspection and get reminders. The app does not provide specifications: the user enters the values from the manual or tyre placard.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, intl.

## SCREENS

1. Tyres – each tyre position (front, rear left, rear right, spare if any) with its recommended pressure, last inspection and status; empty state.
2. Specifications – enter recommended pressures per position and unit (psi, kPa or bar), tyre size and tyre brand; validation.
3. Inspect Tyre – checklist (pressure checked, tread depth, cracks or bulges, nails or cuts, valve cap) with a measured pressure and a note; the result compares to the specification.
4. Inspection History – past inspections per tyre with trend of pressure.
5. Tyre Guide – illustrated how-to cards: how to check pressure, reading tread wear, signs to replace, and tips for care.
6. Replacements – record fitting dates, cost and tyre age (manufacture week and year).
7. Settings – pressure unit, inspection interval days, reminders, theme.

## NAVIGATION

Bottom tabs Tyres, Guide, History, Settings; Inspect from a tyre. Back returns one level.

## UI/UX

Workshop-friendly style, light and dark. Primary charcoal #37474F, accent orange #FF6F00, background #F4F5F6. Font Noto Sans (bundled). Tyre diagram with tappable positions, status by icon and text, large buttons. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Pressure status: low, ok or high compared with the saved specification and a tolerance setting.
- Next inspection date from the interval; reminders rescheduled on edit, completion and restart.
- Tyre age from the manufacture date; replacement history and costs; validation.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud. Guide content reviewed by a mechanic.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for pressure status, next inspection date, tyre age and the inspection repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 95. ENGINE WARNING GUIDE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 95. ENGINE WARNING GUIDE

## APPLICATION PURPOSE

Build "Engine Warning Guide", a Flutter app that explains common dashboard warning symbols and when to seek service. It helps a driver understand a warning light quickly and decide whether to stop. Target users are auto drivers; main use case: find the symbol that is lit and read what it means, how urgent it is and what to do. Assumption: the source description is cut off after "when"; each entry includes when to stop, when to visit a mechanic and when it is only information. The guide is general, not a diagnosis, and the team must have the content reviewed by a mechanic.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences, url_launcher (dialer for saved mechanic contacts), flutter_tts (optional). Symbols drawn with CustomPainter or icons. Fully offline.

## SCREENS

1. Home – search, categories and an urgency filter.
2. Symbol List – symbols by colour group (red, amber, green and blue) with urgency chips; search by name or description.
3. Symbol Detail – large symbol, name, plain-language meaning, urgency (Stop Now, Check Soon, Information), likely causes in simple words, what to do now and when to visit a mechanic; Listen button.
4. Find My Symbol – answer a few questions (colour, shape, flashing or steady) to narrow down the list.
5. My Mechanic – saved contacts with tap-to-dial.
6. Safety Tips – what to do when a warning appears while driving with a passenger.
7. Settings – text size, speech, theme.

## NAVIGATION

Home > List > Detail; Find My Symbol, My Mechanic and Safety Tips from Home. Back returns one level.

## UI/UX

Clear alert-aware style, light and dark. Primary dark blue #1A237E, accent amber #FFA000, red #C62828 for urgent items with text labels, background #F6F7FB. Font Noto Sans (bundled). Large symbols, plain words, urgency by text, icon and colour. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Symbol JSON (name, group, urgency, meaning, causes, actions).
- Search and filter; the guided narrowing by colour, shape and flashing.
- Optional speech; saved contacts; persistence.

## DATA AND BACKEND

Bundled JSON and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for search and filters, guided narrowing, content parsing and contact storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 96. RAINY RIDE CHECKLIST

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 96. RAINY RIDE CHECKLIST

## APPLICATION PURPOSE

Build "Rainy Ride Checklist", a Flutter app with a monsoon driving safety checklist. It helps drivers prepare the vehicle and themselves for heavy rain. Target users are auto drivers; main use case: run the checklist before rainy days and use the on-road tips during the ride. The checklist is general guidance and is reviewed by the team.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite,

flutter_local_notifications + timezone (optional rainy-season reminders).

## SCREENS

1. Home – today's checklist progress, quick tips, Reset for a new day.
2. Before You Go – items such as brakes and brake pedal feel, tyre grip, headlights and indicators, wipers and screen if fitted, side curtains or cover, horn, spare cloth, torch, tools and phone charged; tick each item.
3. On the Road – large tip cards: slow down and keep distance, avoid flooded stretches, use lights, stop safely if visibility is poor.
4. After the Ride – dry the vehicle, check brakes after wading, check electrics and tyres, clean mud.
5. Custom Items – add, edit or hide checklist items.
6. Passenger Comfort – tips for keeping passengers dry and safe.
7. Settings – rainy-season reminder time, text size, theme.

## NAVIGATION

Bottom tabs Before, Road, After, Settings. Back returns to the tab.

## UI/UX

Fresh monsoon style, light and dark. Primary blue #0277BD, accent teal #00ACC1, background #F0F8FC. Font Noto Sans (bundled). Big tick boxes, icons with text, readable on bright and dark days. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Checklist JSON plus user items; tick state saved per day and reset on a new day.
- Progress per section; optional reminders; validation and persistence.

## DATA AND BACKEND

Bundled JSON with local storage; no weather API, account or cloud. State that the app does not forecast weather.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for daily reset, progress calculation, custom item repository and reminder scheduling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 97. DRIVER HEALTH BREAKS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 97. DRIVER HEALTH BREAKS

## APPLICATION PURPOSE

Build "Driver Health Breaks", a Flutter app that offers hydration, posture and rest-break prompts through the day. It helps drivers who sit for long hours look after themselves. Target users are auto drivers; main use case: turn on reminders at the start of a shift and follow the quick tip shown with each prompt. The app gives general wellbeing prompts only, not medical advice, and the tips are reviewed by the team.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite or shared_preferences,

flutter_local_notifications + timezone, fl_chart.

## SCREENS

1. Today – prompts due and done (water, stretch, rest), a simple water count, and a Start Shift or End Shift button; empty state.
2. Reminder Setup – choose reminder types and intervals (for example water every 90 minutes), active hours and quiet hours; validation.
3. Prompt Card – shown from the notification: the prompt, a short illustrated tip and Done and Later buttons.
4. Stretch Tips – illustrated cards for neck, shoulders, back and legs that can be done beside the vehicle; safety note to avoid stretching while driving.
5. Rest Tips – short guidance on taking a break when tired, with a reminder never to drive when drowsy.
6. History – prompts completed per day and week; chart.
7. Settings – sound and vibration, interval defaults, theme, text size.

## NAVIGATION

Bottom tabs Today, Tips, History, Settings; the notification opens the Prompt Card. Back returns one level.

## UI/UX

Friendly wellbeing style, light and dark. Primary teal #00897B, accent blue #29B6F6, background #F3FAF9. Font Noto Sans (bundled). Big Done buttons, drawn illustrations with text. Reusable PromptTile, TipCard, WaterCounter. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Interval scheduling within active hours; reschedule after edits, boot and restart; Android 13+ permission.
- Done and Later actions from the notification; Later re-notifies after a set delay.
- Water count, history aggregation, validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for interval scheduling within active hours, Later delay, history aggregation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 98. LOCAL LANDMARK CARDS

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 98. LOCAL LANDMARK CARDS

## APPLICATION PURPOSE

Build "Local Landmark Cards", a Flutter app for saving frequently requested landmarks and their addresses. It helps a driver remember and quickly confirm destinations with passengers. Target users are auto drivers; main use case: save landmark cards with the name in several languages and the address, then search and show them. Everything is typed by the driver; no map services are required.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, url_launcher (optional geo: link to open the phone's map app), share_plus. Bundle Noto Sans Kannada and Noto Sans Devanagari (OFL).

## SCREENS

1. Landmarks – cards with name, area and category chips; search by name, alias or area; favourites at the top; empty state.
2. Add/Edit Landmark – name, alternate names (such as Kannada or Hindi spelling), area, address text, category (Hospital, Station, Mall, Temple, Market, Office, Other), optional approximate fare note, optional latitude and longitude; validation.
3. Landmark Display – very large text of the name and address to show a passenger; Open in Maps (if coordinates exist); Share as text.
4. Categories and Areas – manage lists.
5. Import / Export – export all cards as a file and import them back (validation of the format).
6. Settings – text size, languages shown, theme.

## NAVIGATION

Landmarks is home with floating Add; Display and Settings from there. Back returns one level.

## UI/UX

Practical card style, light and dark. Primary indigo #3949AB, accent orange #FB8C00, background #F6F7FB. Fonts Noto Sans, Noto Sans Kannada and Noto Sans Devanagari (bundled). Large readable cards, category colours with text. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Landmark CRUD with aliases; fuzzy search across names, aliases and areas.
- Favourites and categories; geo link only when coordinates are present.
- Import and export of landmark data; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no maps SDK, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for alias and fuzzy search, import and export validation and the landmark repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 99. PASSENGER FEEDBACK NOTES

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 99. PASSENGER FEEDBACK NOTES

## APPLICATION PURPOSE

Build "Passenger Feedback Notes", a Flutter app for recording optional private feedback and service improvement notes. It helps a driver learn from comments and improve service. Target users are auto drivers; main use case: jot down feedback after a ride and review common themes. Privacy rule: no passenger names or contact details are collected; entries are private on the device.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl.

## SCREENS

1. Notes – list of feedback notes with rating, tags and date; empty state; Add Note.
2. Add Note – date, feeling or rating (1-5 stars or smiley), tags (Cleanliness, Politeness, Route, Fare, Safety, Waiting, Other), what the passenger said (optional), improvement idea, privacy reminder not to enter personal details; validation.
3. Note Detail – full note; mark the improvement idea as Done; edit and delete with confirm.
4. Improvement Board – improvement ideas as a to-do list with status.
5. Insights – average rating over time, most common tags and positive-versus-negative counts; chart.
6. Settings – tags, theme, reset.

## NAVIGATION

Bottom tabs Notes, Ideas, Insights, Settings; floating Add. Back returns one level.

## UI/UX

Positive simple style, light and dark. Primary orange #EF6C00, accent teal #00897B, background #FFF8F2. Font Noto Sans (bundled). Big rating buttons, tags with icons and text. Reusable NoteCard, TagChip, RatingRow. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Note CRUD, tag filters and search; rating averages by week and month.
- Improvement ideas with status; tag frequency; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no passenger identifiers, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for rating averages, tag frequency, improvement status and the note repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 100. DAILY TRIP COUNTER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 100. DAILY TRIP COUNTER

## APPLICATION PURPOSE

Build "Daily Trip Counter", a Flutter app that counts trips and tracks trip totals without complex dispatch features. It gives drivers a one-tap way to count trips through the day. Target users are auto drivers; main use case: tap the big button after each trip and see the day, week and month totals.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl, HapticFeedback.

## SCREENS

1. Counter – a huge Add Trip button, today's count in very large digits, Undo, and an optional fare field that appears after a tap; empty state at the start of the day.
2. Today's Trips – list of trips with time and optional fare; edit and delete with confirm.
3. History – daily counts for the last 30 days; week and month totals; best day.
4. Stats – bar chart of trips per day and average per working day.
5. Settings – business-day start hour, haptic feedback, optional daily trip goal, theme, CSV export, reset.

## NAVIGATION

Bottom tabs Counter, History, Stats, Settings. Back returns one level; Android back from Counter exits.

## UI/UX

Big-button utility style, light and dark. Primary indigo #3949AB, accent green #43A047, background #F6F7FB. Font Noto Sans (bundled). One-handed layout, digits larger than 96sp, vibration on tap. Reusable BigCountButton, DayBar, StatTile. Built for outdoor use by drivers: high contrast for sunlight, touch targets of 56dp or more, one-handed layout, minimal typing (number pads), works fully offline, and all text kept in ARB files so Kannada and Hindi can be added.

## FUNCTIONALITY

- Each tap logs a trip with a timestamp; Undo removes the last trip; counts by business day.
- Optional fare totals per day; weekly, monthly and average statistics; goal progress.
- CSV export, validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for business-day counting, undo behaviour, weekly and monthly aggregation and the trip repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---
