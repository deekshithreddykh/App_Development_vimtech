# Flutter Prompts - Apps for Working Men

One standalone prompt per page. Give each team only its own page.

Each prompt below is in its own box. Use the copy button on the box to copy just that prompt.

126. WORKSPRINT
127. SALARYMAP
128. COMMUTESAVER
129. STREAKBUILDER
130. SKILLUP FIVE
131. OVERTIME CALCULATOR
132. PAYSLIP EXPLAINER
133. BILL DUE RADAR
134. REPAIR COST NOTEBOOK
135. LUNCH BUDGET BUDDY
136. WEEKEND TASK PLANNER
137. MEETING PREP POCKET
138. PROFESSIONAL PHRASEBOOK
139. INTERVIEW ANSWER TRAINER
140. DIGITAL DOCUMENT EXPIRY
141. TOOL INVENTORY MINI
142. SHIFT HANDOVER NOTES
143. WORK BREAK TIMER
144. HOME INVENTORY POCKET
145. SAVINGS MILESTONE TRACKER
146. DEBT REPAYMENT PLANNER
147. MONTHLY SUBSCRIPTION AUDIT
148. PERSONAL ACHIEVEMENT LOG
149. QUICK MEAL SELECTOR
150. LIFE ADMIN DASHBOARD

---

## 126. WORKSPRINT

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 126. WORKSPRINT

## APPLICATION PURPOSE

Build "WorkSprint", a Flutter app that organises the day's tasks by priority, deadline and estimated time, so a working professional can see what to do first and whether the day is realistically full. It solves the problem of long, unordered to-do lists that hide urgent work. Target users are working adults; main use case: add tasks in the morning, get an ordered plan that fits the workday, and tick tasks off.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite (tasks), shared_preferences (settings),

flutter_local_notifications + timezone (deadline reminders), intl. Free and open-source only.

## SCREENS

1. Today – tasks in recommended order with priority chip, deadline and estimate; progress bar of planned vs available hours; tick to complete; overload banner when planned time exceeds the workday; empty state with Add Task prompt.
2. Add/Edit Task – title (required), priority (High/Medium/Low), deadline date-time, estimate in minutes, notes, reminder toggle; validation messages; delete with confirm; unsaved-changes confirm.
3. Plan – tasks packed sequentially into the workday window with start and end times, skipping breaks; tasks that do not fit listed under "Won't fit today"; drag to reorder manually.
4. All Tasks – filter chips (Today, Upcoming, Overdue, Done), search and sort.
5. Summary – tasks completed, estimated time completed, overdue count; weekly bar chart; empty state.
6. Settings – workday start/end, break length, default estimate, reminders on/off, light/dark theme.

## NAVIGATION

Bottom tabs Today, Plan, All, Summary; floating Add button; Settings from the app bar. Android back returns one level; forms confirm before discarding.

## UI/UX

Clean productivity style, light and dark themes. Primary indigo #3F51B5, accent orange #FF7043, background #F6F7FB, surface white. Font Inter (bundled). Priority shown by colour and icon, not colour alone. 8dp grid, 12dp radii, 48dp touch targets. Reusable TaskCard, PriorityChip, TimeBar.

## FUNCTIONALITY

- Urgency score = priority weight + deadline proximity (documented formula); ties favour shorter tasks.
- Scheduler fills the workday window sequentially and reports overflow.
- Overdue detection; completed tasks move to Done and update the Summary.
- Reminders 30 minutes before a deadline, rescheduled on edit, completion and app restart (Android 13+ notification permission).
- Validation of title, estimate (1-720 minutes) and deadline.

## DATA AND BACKEND

Local sqflite database and shared_preferences; no account, cloud, ads or analytics. Reminders are local notifications only.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for urgency scoring, scheduling and overflow, overdue detection and the task repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 127. SALARYMAP

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 127. SALARYMAP

## APPLICATION PURPOSE

Build "SalaryMap", a Flutter app that estimates monthly take-home pay from manually entered gross pay and deductions, then lets the user allocate that money to expenses and savings. It solves the problem of not knowing how much is really available each month. Target users are salaried workers; main use case: enter pay, list deductions, plan a budget and compare with actual spending. Assumption: no tax rules are built in - every deduction is user-entered as a percentage or fixed amount - and the app states that figures are estimates, not tax or financial advice.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart (donut/bar charts), intl. Free and open-source only.

## SCREENS

1. Home – take-home estimate, total allocated, unallocated remainder, donut chart of allocation; empty state prompting pay setup.
2. Pay Setup – gross pay, pay frequency, list of deductions (name, percentage of gross or fixed amount); add, edit, delete; live net-pay preview; validation of non-negative numbers.
3. Allocation Planner – category rows (rent, food, transport, bills, savings, other, custom) with amount or percentage inputs; remaining-to-allocate indicator; over-allocation warning; optional 50/30/20 starter template.
4. Planned vs Actual – enter actual spend per category; bars compare plan with actual; overspend highlighted.
5. History – saved months with take-home, saved amount and savings rate; copy previous month's plan.
6. Settings – currency symbol, rounding, theme, CSV export via share sheet, reset data with confirm.

## NAVIGATION

Bottom tabs Home, Plan, Actual, History; Pay Setup and Settings from Home. Back returns one level; unsaved edits confirm.

## UI/UX

Calm financial style, light and dark. Primary teal #00796B, accent amber #FFB300, background #F4F8F7, surface white. Font Manrope (bundled). Tabular numerals for money, 12dp radii, clear positive/negative colours with icons. Reusable MoneyField, CategoryRow, SummaryCard.

## FUNCTIONALITY

- Net pay = gross - sum of deductions (percentage of gross or fixed).
- Allocation total versus net with remaining and over-allocation states.
- Monthly records saved and compared; savings rate = saved / net.
- Input validation with limits; money stored as integer minor units.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank connection, account, cloud, ads or analytics; manual entry only.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for net-pay calculation, allocation totals, savings rate and the history repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 128. COMMUTESAVER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 128. COMMUTESAVER

## APPLICATION PURPOSE

Build "CommuteSaver", a Flutter app that compares daily and monthly commuting costs for different transport choices (public transport, own vehicle, ride-hailing, walking or cycling). It solves the problem of guessing which commute is cheapest and how much it costs over a month or year. Target users are daily commuters; main use case: enter each option's costs and see which is cheapest, fastest and worth a monthly pass.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl. No maps or live fare APIs: all figures are entered manually.

## SCREENS

1. Home – saved comparisons (e.g. Home to Office) with the cheapest option highlighted; empty state; Add Comparison.
2. Comparison Setup – name, working days per month, trips per day, add transport options.
3. Option Editor – type-specific fields: public transport (fare per trip or pass price), own vehicle (distance, mileage, fuel price, parking, toll, maintenance per km), ride-hailing (fare per trip), walking/cycling (cost per month); travel time per trip; validation.
4. Compare – table and bar chart of cost per day, month and year plus time per day; badges Cheapest and Fastest.
5. Pass Break-Even – pass price versus pay-per-ride: trips needed per month to break even and the savings at the user's trip count.
6. Settings – currency, distance unit, theme, reset data.

## NAVIGATION

Home > Comparison > Compare/Break-Even; Option Editor from Setup; back returns one level with unsaved-change confirm.

## UI/UX

Practical transit style, light and dark. Primary blue #1565C0, accent green #2E7D32 (savings), bg #F3F6FB. Font Work Sans (bundled). Mode icons plus text labels, 12dp radii. Reusable OptionCard, CostBar, ModeIcon.

## FUNCTIONALITY

- Vehicle cost per trip = distance / mileage x fuel price + tolls + parking + distance x maintenance rate.
- Daily = per-trip x trips per day; monthly = daily x days per month; yearly = monthly x 12.
- Pass break-even and cheapest/fastest ranking; zero-division and empty-field handling.
- Persistence of comparisons and options.

## DATA AND BACKEND

Local sqflite and shared_preferences; no maps, APIs, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for per-trip vehicle cost, day/month/year totals, break-even and ranking and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 129. STREAKBUILDER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 129. STREAKBUILDER

## APPLICATION PURPOSE

Build "StreakBuilder", a Flutter habit tracker for personal habits such as reading, exercise, learning and saving money. It solves the problem of habits fading because progress is invisible. Target users are busy adults; main use case: tick or log habits daily, watch streaks grow and review weekly progress.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, intl.

## SCREENS

1. Today – list of habits due today with one-tap completion; numeric habits (minutes, pages, amount saved) open a quick-entry sheet; streak flame and progress ring; empty state.
2. Add/Edit Habit – name, icon, type (yes/no, count, amount), daily target, schedule days, reminder time, colour; validation.
3. Habit Detail – current streak, best streak, completion rate, calendar heatmap, history list; pause or archive habit.
4. Stats – weekly and monthly completion chart; best habit; total saved for money habits.
5. Settings – week start day, reminder permission status, theme, CSV export, reset with confirm.

## NAVIGATION

Bottom tabs Today, Stats, Habits, Settings; Detail from a habit tap. Back returns one level.

## UI/UX

Motivating clean style, light and dark. Primary orange #F57C00, accent purple #7E57C2, background #FFF8F0. Font Poppins (bundled). Large check circles (56dp), flame and heatmap visuals with text alternatives. Reusable HabitTile, StreakBadge, Heatmap.

## FUNCTIONALITY

- Streak counts consecutive scheduled days completed; non-scheduled and paused days do not break it.
- Count/amount habits complete when the daily target is met; edits recalculate streaks.
- Daily reminders at the chosen time, rescheduled after restart.
- Weekly and monthly statistics; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account, cloud or analytics.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for streak calculation with schedules and pauses, target completion, statistics and the habit repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 130. SKILLUP FIVE

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 130. SKILLUP FIVE

## APPLICATION PURPOSE

Build "SkillUp Five", a Flutter app delivering short five-minute daily lessons in communication, computer skills and workplace productivity. It solves the problem of professionals having no time for long courses. Target users are working adults; main use case: complete one short lesson and quiz each day and keep a learning streak. Assumption: the team writes about 8 original lessons per track (24 total) in a JSON file and has them reviewed for accuracy.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite (progress),

flutter_local_notifications + timezone (daily reminder).

## SCREENS

1. Home – today's lesson card for the chosen track, streak, weekly progress dots; empty/all-done state.
2. Tracks – Communication, Computer Skills, Workplace Productivity with progress bars.
3. Lesson List – lessons of a track with completed ticks and a locked-until-previous option.
4. Lesson Player – 5 swipeable cards (text, example, tip) with a progress bar and an approximate 5-minute indicator; bookmark button.
5. Quiz & Result – 3 questions per lesson; pass at 2/3; explanations; retry.
6. Progress – streak, lessons completed, badges, bookmarks.
7. Settings – daily reminder time, preferred track, text size, theme.

## NAVIGATION

Bottom tabs Home, Tracks, Progress; Settings from Home. Lesson > Quiz > Result > Home. Back confirms mid-lesson.

## UI/UX

Focused learning style, light and dark. Primary blue #1976D2, accent coral #FF7043, background #F5F9FF. Font Nunito Sans (bundled). 18sp lesson text, high contrast, card-swipe animation. Reusable LessonCard, QuizOption, StreakChip.

## FUNCTIONALITY

- Lesson JSON model (track, title, cards, quiz).
- Daily lesson = next uncompleted lesson in the preferred track.
- Quiz scoring, pass/fail, completion saved; streak counts days with a completed lesson.
- Bookmarks, badges and daily reminder.

## DATA AND BACKEND

Bundled JSON content and local storage; no account or cloud. Content is authored offline by the team.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for daily lesson selection, quiz scoring, streak logic and progress storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 131. OVERTIME CALCULATOR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 131. OVERTIME CALCULATOR

## APPLICATION PURPOSE

Build "Overtime Calculator", a Flutter app that estimates additional pay from entered work hours and rates. It solves the problem of not knowing what extra hours are worth before payday. Target users are hourly and salaried workers who work extra hours; main use case: log overtime each day and see the estimated extra pay for the week and month. Assumption: overtime multipliers and daily regular hours are user-entered because rules vary by employer and country; results are estimates to compare against the payslip.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl.

## SCREENS

1. Home – this month's overtime hours and estimated extra pay, last entries, quick Add Hours button; empty state.
2. Rates Setup – pay basis (hourly rate, or monthly salary with working days and hours used to derive an hourly rate), regular daily hours, multipliers for weekday, weekend and holiday overtime, rounding rule; validation.
3. Add/Edit Hours – date, start and end time or total hours, day type, notes; automatic split into regular and overtime hours; delete with confirm.
4. Log – entries by date with filters for month and day type; edit and delete.
5. Monthly Summary – hours and pay by day type, weekly totals, bar chart; month picker.
6. Settings – currency, rounding, theme, CSV export, reset.

## NAVIGATION

Bottom tabs Home, Log, Summary, Settings; Add and Rates from Home. Back confirms unsaved edits.

## UI/UX

Practical payroll-tool style, light and dark. Primary indigo #303F9F, accent amber #FFA000, background #F5F6FA. Font IBM Plex Sans (bundled). Tabular numerals; overtime in amber with icon. Reusable HoursField, SummaryTile, DayTypeChip.

## FUNCTIONALITY

- Hourly rate = monthly salary / (working days x daily hours) when salary basis is used.
- Overtime hours = hours beyond regular hours; pay = overtime hours x hourly rate x multiplier by day type.
- Weekly and monthly totals; overnight shifts that cross midnight handled; validation of time ranges.
- Persistence and CSV export.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud. State clearly that the figures are estimates only.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for hourly-rate derivation, regular/overtime split including overnight shifts, multiplier pay and monthly totals and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 132. PAYSLIP EXPLAINER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 132. PAYSLIP EXPLAINER

## APPLICATION PURPOSE

Build "Payslip Explainer", a Flutter app that explains salary components and deductions in plain language using figures the user types in from their payslip. It solves the problem of payslips being confusing. Target users are employees; main use case: enter earnings and deductions, check that they add up, and read a simple explanation of each line. Assumption: explanations are general and not specific to any country; the app gives no tax or legal advice and does not read or store payslip files.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl. Glossary content bundled as JSON written and reviewed by the team.

## SCREENS

1. Home – saved payslips by month with gross and net; Add Payslip; empty state.
2. Enter Payslip – month, earnings list (basic, allowances, bonus, overtime, other) and deductions list (income tax, social contribution, insurance, loan repayment, other) chosen from presets or custom; entered gross and net fields; validation.
3. Check & Explain – computed gross and net versus entered figures with a mismatch warning; each line card gives a plain-language description, its share of gross, and a "what to ask HR" tip.
4. Breakdown – donut of net versus deductions plus a bar of earnings components.
5. Compare Months – two months side by side with differences highlighted.
6. Glossary – searchable terms (gross, net, CTC, allowance, arrears, etc.).
7. Settings – currency, theme, delete data.

## NAVIGATION

Home > Enter > Check & Explain > Breakdown; Compare and Glossary from Home. Back confirms unsaved edits.

## UI/UX

Clear explanatory style, light and dark. Primary navy #283593, accent teal #00ACC1, background #F6F8FC. Font Source Sans 3 (bundled). Plain wording, tabular numbers, info icons. Reusable LineItemCard, MismatchBanner, GlossaryTile.

## FUNCTIONALITY

- Gross = sum of earnings; net = gross - sum of deductions; mismatch with entered values shown with the difference.
- Percentage of gross per line; month-to-month differences.
- Glossary search; input validation and persistence.

## DATA AND BACKEND

Local sqflite and bundled JSON; no uploads, OCR, account or cloud; manual entry only.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for gross/net computation, mismatch detection, percentage shares and month comparison and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 133. BILL DUE RADAR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 133. BILL DUE RADAR

## APPLICATION PURPOSE

Build "Bill Due Radar", a Flutter app that organises bill amounts and due dates and sends local reminders before they fall due. It solves the problem of missed or late payments. Target users are working adults managing household bills; main use case: add recurring bills once, get reminded, mark them paid and see the month's totals. The app records bills only and never makes payments.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, intl. Reminders must be rescheduled after reboot.

## SCREENS

1. Dashboard – overdue, due this week and upcoming bills; month total, paid and unpaid amounts; empty state.
2. Add/Edit Bill – name, amount, category, due date, recurrence (one-off, weekly, monthly, quarterly, yearly), reminder lead days, notes; validation.
3. Calendar – month view with due-date markers; day tap lists bills.
4. Bill Detail – status, next due date, payment history, Mark Paid, skip, delete with confirm.
5. Reports – monthly totals by category, last 6 months chart.
6. Settings – default reminder lead time and time of day, currency, theme, notification permission status.

## NAVIGATION

Bottom tabs Dashboard, Calendar, Reports, Settings; floating Add button. Back returns one level.

## UI/UX

Dependable utility style, light and dark. Primary teal #00897B, accent red #E53935 for overdue, background #F2F8F7. Font DM Sans (bundled). Status shown by icon and text as well as colour. Reusable BillCard, StatusChip, MonthSummary.

## FUNCTIONALITY

- Mark Paid logs a payment and creates the next occurrence from the recurrence rule (including month-end dates).
- Overdue and due-soon detection; reminders at the chosen lead days; reschedule on edit, paid, boot and restart.
- Category totals; amount and date validation.

## DATA AND BACKEND

Local sqflite and shared_preferences; no payment, bank, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for recurrence next-date rules including month ends, overdue detection, totals and reminder scheduling logic and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 134. REPAIR COST NOTEBOOK

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 134. REPAIR COST NOTEBOOK

## APPLICATION PURPOSE

Build "Repair Cost Notebook", a Flutter app that tracks vehicle, appliance and household repair costs. It solves the problem of forgetting what repairs cost and when they were done, which hurts replace-or-repair decisions. Target users are vehicle and home owners; main use case: register an item, log each repair with costs and see total spend over time.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl, share_plus (CSV export), flutter_local_notifications + timezone (optional service reminders).

## SCREENS

1. Home – total repair spend this year, recent repairs, items needing service; empty state.
2. Items – list of vehicles, appliances and household items with type icon and lifetime cost; Add Item.
3. Item Detail – timeline of repairs, total cost, cost per year, next service date.
4. Add/Edit Repair – item, date, description, parts cost, labour cost, vendor, repair warranty end date, notes, optional next service date and reminder; validation.
5. Reports – spend by item, by category and by month; chart.
6. Settings – currency, categories, theme, CSV export, reset.

## NAVIGATION

Bottom tabs Home, Items, Reports, Settings; floating Add Repair. Back returns one level.

## UI/UX

Workshop notebook style, light and dark. Primary slate #455A64, accent orange #FF6F00, background #F5F6F7. Font Work Sans (bundled). Item-type icons, 12dp radii, large cost numbers. Reusable RepairTile, ItemCard, CostChip.

## FUNCTIONALITY

- Total cost = parts + labour; totals per item, year and category.
- Search and filters by item, vendor and date range.
- Optional service reminder scheduling; CSV export of the repair log.
- Validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for cost totals, report aggregation, filters and the repair repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 135. LUNCH BUDGET BUDDY

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 135. LUNCH BUDGET BUDDY

## APPLICATION PURPOSE

Build "Lunch Budget Buddy", a Flutter app that plans meals and compares expected food spending against a budget. It solves the problem of everyday lunches and snacks quietly exceeding the food budget. Target users are working adults; main use case: set a weekly food budget, plan each day's meals with expected costs, then record actual costs.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl.

## SCREENS

1. Home – budget gauge (planned, spent, remaining), today's meals, per-day allowance left; empty state.
2. Budget Setup – weekly or monthly budget, working days, warning thresholds (default 80% and 100%).
3. Meal Planner – weekly grid by day and meal slot (breakfast, lunch, dinner, snack); add meal with name, expected cost and type (home, office canteen, takeaway).
4. Meal Library – saved meals with typical cost; quick-add to plan; add, edit, delete.
5. Log Actual – record actual cost against a planned meal or as an extra spend.
6. Summary – planned versus actual by day and meal type; chart; over-budget days highlighted.
7. Settings – currency, theme, reset.

## NAVIGATION

Bottom tabs Home, Plan, Log, Summary; Budget Setup and Settings from Home. Back confirms unsaved edits.

## UI/UX

Friendly food-budget style, light and dark. Primary green #43A047, accent orange #FB8C00, background #F6FBF4. Font Nunito (bundled). Gauge with text values, meal-type icons. Reusable BudgetGauge, MealTile, DayColumn.

## FUNCTIONALITY

- Planned total, actual total, remaining and daily allowance = remaining / days left.
- Warning banners at thresholds; copy last week's plan.
- Library reuse; validation of costs and budget; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for budget totals and daily allowance, threshold warnings, plan copying and meal repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 136. WEEKEND TASK PLANNER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 136. WEEKEND TASK PLANNER

## APPLICATION PURPOSE

Build "Weekend Task Planner", a Flutter app that organises errands, shopping, family activities and rest time across Saturday and Sunday. It solves the problem of weekends disappearing without rest or important errands. Target users are working adults; main use case: block out the weekend, keep a shopping list and make sure rest time is protected. Assumption: weekend days default to Saturday and Sunday and are configurable.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, intl.

## SCREENS

1. Weekend View – day tabs with a timeline of time-blocked items by category colour; unscheduled items list; empty state.
2. Add/Edit Item – title, category (errand, shopping, family, rest), day, start time, duration, location note, reminder; validation and overlap warning.
3. Shopping List – items with quantity and check-off; clear completed; share list as text.
4. Balance – donut of hours by category; warning if rest time is below the chosen minimum.
5. Templates – save and reuse a weekend routine.
6. Settings – weekend days, minimum rest hours, default reminder, theme.

## NAVIGATION

Bottom tabs Weekend, Shopping, Balance, Settings; Add button on Weekend. Back confirms unsaved edits.

## UI/UX

Relaxed lifestyle style, light and dark. Primary teal #26A69A, accent coral #FF7043, background #F3FAF9. Font Nunito Sans (bundled). Category colours with icons, rounded blocks. Reusable TimeBlock, CategoryChip, ShoppingRow.

## FUNCTIONALITY

- Overlap detection for time blocks; unfinished items can roll over to next weekend.
- Hours-per-category calculation and rest-time warning.
- Reminders before items; template save and load; list sharing.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for overlap detection, balance calculation, rollover and template storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 137. MEETING PREP POCKET

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 137. MEETING PREP POCKET

## APPLICATION PURPOSE

Build "Meeting Prep Pocket", a Flutter app for preparing agendas, questions and checklists for meetings and capturing outcomes afterwards. It solves the problem of walking into meetings unprepared and losing action items. Target users are working professionals; main use case: create a meeting from a template, prepare, then record decisions and actions.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, share_plus, intl.

## SCREENS

1. Home – upcoming and recent meetings, open action-item count; empty state.
2. New/Edit Meeting – title, date and time, length, attendees (names), template choice; validation.
3. Meeting Detail – tabs Agenda (items with time allocations), Questions, Checklist, Notes & Decisions; edit inline.
4. Templates – 1:1, project update, client call, interview and custom, each with preset agenda and checklist.
5. Action Items – all actions across meetings with owner, due date and status filters.
6. Settings – reminder lead time, default meeting length, theme.

## NAVIGATION

Bottom tabs Home, Actions, Templates, Settings; floating New Meeting. Back confirms unsaved edits.

## UI/UX

Professional organised style, light and dark. Primary blue #1E88E5, accent amber #FFB300, background #F5F8FC. Font Inter (bundled). Tab layout, check-off animations, 48dp targets. Reusable AgendaRow, ChecklistTile, ActionCard.

## FUNCTIONALITY

- Agenda time total versus meeting length with an overrun warning.
- Create from template; carry unfinished actions forward.
- Export a plain-text meeting summary via the share sheet.
- Reminder before the meeting; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no calendar sync, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for agenda time totals, template creation, action filters and summary text generation and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 138. PROFESSIONAL PHRASEBOOK

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 138. PROFESSIONAL PHRASEBOOK

## APPLICATION PURPOSE

Build "Professional Phrasebook", a Flutter app for practising polite workplace English and common professional phrases. It solves the problem of non-native and early-career speakers lacking the right words for emails, meetings and calls. Target users are working adults learning professional English; main use case: browse phrases by situation, hear them, then practise with short quizzes. Assumption: the team writes about 120 phrases in JSON and has them reviewed by a fluent English speaker.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite, flutter_tts (pronunciation).

## SCREENS

1. Home – phrase of the day, scenarios, practice, favourites; progress.
2. Scenarios – Greetings, Emails, Meetings, Phone Calls, Requests, Polite Disagreement, Apologies, Giving Feedback, Small Talk.
3. Phrase List – phrases with formal and casual versions; search; favourite toggle.
4. Phrase Detail – phrase, meaning, example sentence, when to use it and when to avoid it; Listen button; Mark Learned.
5. Practice – quizzes: choose the most polite phrase, fill the blank, match situation to phrase; 10 questions; results.
6. Favourites & Progress – saved phrases, learned count per scenario, streak.
7. Settings – speech speed, text size, daily reminder, theme.

## NAVIGATION

Bottom tabs Home, Scenarios, Practice, Progress; Detail from lists. Back returns one level.

## UI/UX

Professional but friendly style, light and dark. Primary blue #3949AB, accent orange #FF7043, background #F5F6FD. Font Source Sans 3 (bundled). Large text, tone labels (formal, neutral, casual) with icons. Reusable PhraseCard, ToneChip, QuizOption.

## FUNCTIONALITY

- Phrase JSON model (scenario, text, tone, meaning, example, when/when-not).
- Search and scenario filtering; speech with failure handling.
- Quiz generator with plausible distractors; learned tracking and streak; favourites.

## DATA AND BACKEND

Bundled JSON and local storage; no account or cloud. Needs an English TTS voice on the device (document it).

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for search and filtering, quiz generation, progress tracking and favourites storage and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 139. INTERVIEW ANSWER TRAINER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 139. INTERVIEW ANSWER TRAINER

## APPLICATION PURPOSE

Build "Interview Answer Trainer", a Flutter app for practising interview questions and saving personal answers. It solves the problem of struggling to recall good examples under pressure. Target users are job seekers and professionals; main use case: write answers using a simple structure, practise with a timer and rate each attempt. Assumption: practice is self-assessed; the app does not score answers with AI. About 60 bundled questions are written and reviewed by the team.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, share_plus, intl.

## SCREENS

1. Home – practice streak, questions answered, quick Start Practice; empty state.
2. Question Bank – categories (Common, Behavioural, Situational, Strengths and Weaknesses, Salary and HR), search, favourites, add custom question.
3. Answer Editor – question, answer fields following Situation, Task, Action, Result or free text, notes, confidence rating; autosave draft; validation.
4. Practice Session – random or category questions, optional 2-minute timer, reveal saved answer, self-rating after each; 5-question mock mode.
5. Session Summary – questions covered, average self-rating, weakest questions to revisit.
6. My Answers – saved answers list with search; share one answer as text.
7. Settings – timer length, theme, reminders, reset.

## NAVIGATION

Bottom tabs Home, Bank, Practice, My Answers; Settings from Home. Practice back confirms exit.

## UI/UX

Calm confident style, light and dark. Primary indigo #3F51B5, accent green #26A69A, background #F6F7FC. Font Inter (bundled). Large readable question text, timer ring with text. Reusable QuestionCard, AnswerField, RatingRow.

## FUNCTIONALITY

- Question and answer models; custom questions; favourites.
- Practice selection weights low-rated and unanswered questions higher.
- Timer using elapsed time; session statistics; share text.
- Validation and persistence.

## DATA AND BACKEND

Local sqflite, bundled JSON; no account, cloud or AI service. Answers stay on the device.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for question selection weighting, session statistics, answer storage and search and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 140. DIGITAL DOCUMENT EXPIRY

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 140. DIGITAL DOCUMENT EXPIRY

## APPLICATION PURPOSE

Build "Digital Document Expiry", a Flutter app that tracks expiry dates for driving licences, insurance, vehicle papers and other documents, and reminds the user before they lapse. It solves the problem of missed renewals and the fines or lapses that follow. Target users are working adults; main use case: add each document's expiry date once and get reminders. Privacy rule: the app stores only a label, type, expiry date and notes - no document numbers, scans or identity data - and warns the user not to enter them.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, intl. Reminders must be rescheduled after reboot.

## SCREENS

1. Dashboard – counts for Expired, Due within 30 days, Due within 90 days and Valid; most urgent documents; empty state.
2. Add/Edit Document – type (driving licence, insurance, vehicle registration, passport, warranty, other), label, expiry date, renewal notes, reminder offsets (90, 30, 7 days or custom); validation and privacy warning.
3. Document List – sorted by expiry with status chips; filter and search.
4. Document Detail – days remaining, renewal checklist the user writes, Mark Renewed (enter new expiry), delete with confirm.
5. Calendar – expiry dates by month.
6. Settings – default reminder offsets, reminder time, notification permission status, theme.

## NAVIGATION

Bottom tabs Dashboard, Documents, Calendar, Settings; floating Add. Back returns one level.

## UI/UX

Trustworthy utility style, light and dark. Primary blue #1565C0, accent red #D32F2F for expired and amber #FFA000 for soon, background #F3F6FB. Font DM Sans (bundled). Status by icon, text and colour. Reusable DocCard, StatusChip, CountTile.

## FUNCTIONALITY

- Status from days remaining (expired, <= 30, <= 90, valid).
- Multiple reminders per document; reschedule on edit, renewal, boot and restart.
- Renewal updates the expiry and keeps a short history.
- Date validation; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no scans, numbers, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for status calculation, reminder date generation, renewal flow and repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 141. TOOL INVENTORY MINI

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 141. TOOL INVENTORY MINI

## APPLICATION PURPOSE

Build "Tool Inventory Mini", a Flutter app that keeps a simple list of work tools with quantities and condition. It solves the problem of lost, duplicated or broken tools and not knowing what needs replacing. Target users are tradespeople, technicians and hobbyists; main use case: record tools, adjust quantities and flag tools needing repair or restocking.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, share_plus (CSV export), intl.

## SCREENS

1. Inventory – searchable list with category, quantity and condition chip; filters by category, condition and location; empty state.
2. Add/Edit Tool – name, category, quantity, condition (New, Good, Fair, Needs Repair, Lost), location (toolbox, van, shed...), purchase date, low-stock threshold, notes; validation.
3. Tool Detail – quantity +/- buttons with history, condition changes, lend-out record (borrower, date, returned); delete with confirm.
4. Needs Attention – tools needing repair, below threshold, lent out or lost.
5. Summary – totals by category and condition; chart.
6. Settings – manage categories and locations, theme, CSV export, reset.

## NAVIGATION

Bottom tabs Inventory, Attention, Summary, Settings; floating Add. Back returns one level.

## UI/UX

Rugged workshop style, light and dark. Primary charcoal #37474F, accent safety orange #FF6F00, background #F4F5F6. Font Roboto Condensed headings and Roboto body (bundled). Large quantity steppers, high contrast, condition icons. Reusable ToolTile, ConditionChip, QtyStepper.

## FUNCTIONALITY

- Quantity never below zero; low-stock flag when quantity <= threshold.
- Lend and return tracking; condition history.
- Search, filters, category totals, CSV export.
- Validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for quantity rules, low-stock detection, lend/return logic, filters and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 142. SHIFT HANDOVER NOTES

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 142. SHIFT HANDOVER NOTES

## APPLICATION PURPOSE

Build "Shift Handover Notes", a Flutter app for recording tasks completed, pending work and handover instructions at the end of a shift. It solves the problem of information being lost between shifts. Target users are shift workers and supervisors; main use case: write a structured handover in a few minutes and share it with the next person as text.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, share_plus, intl.

## SCREENS

1. Home – latest handovers, open pending-item count, New Handover; empty state.
2. New/Edit Handover – date, shift name, optional author name, sections: Completed tasks, Pending tasks (priority, note), Instructions, Issues and safety notes; template picker; autosave draft; validation.
3. Handover Detail – read-only formatted view; Share as text; duplicate as new.
4. Pending Board – all unresolved pending items carried over from earlier handovers with Resolve action and age.
5. History – searchable list filtered by date and shift.
6. Settings – shift names, checklist templates, theme.

## NAVIGATION

Bottom tabs Home, Pending, History, Settings; New Handover floating. Back confirms unsaved draft.

## UI/UX

Clear operational style, light and dark. Primary blue #0277BD, accent amber #FFB300, background #F3F7FA. Font Inter (bundled). High contrast, large touch targets for gloved or hurried use, priority icons. Reusable SectionCard, PendingTile, ShiftChip.

## FUNCTIONALITY

- Pending items persist and carry over until resolved.
- Create from the previous handover or a template.
- Export formatted plain text via the share sheet.
- Search, filters, validation, persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account, server or cloud sync. Mention that sharing happens through the user's chosen app.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for carry-over logic, text export formatting, filters and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 143. WORK BREAK TIMER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 143. WORK BREAK TIMER

## APPLICATION PURPOSE

Build "Work Break Timer", a Flutter app that schedules focus sessions and regular breaks. It solves the problem of working for hours without breaks, or losing focus. Target users are desk workers and students; main use case: start a focus session, take the scheduled break and review focus time.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone (alerts when a session ends), wakelock_plus (optional

keep-awake), fl_chart, vibration or HapticFeedback.

## SCREENS

1. Timer – large ring countdown, session label, Start/Pause/Skip/Reset, current phase (focus, short break, long break) and cycle count.
2. Presets – 25/5, 50/10, custom focus, short and long break lengths and sessions before a long break.
3. Stats – focus minutes per day and week, sessions completed, daily goal progress; chart.
4. History – list of sessions with label, duration and time.
5. Settings – auto-start next phase, sound and vibration, keep screen on, daily goal, notification permission, theme.

## NAVIGATION

Bottom tabs Timer, Stats, History, Settings. Back from the timer does not stop it; Reset asks to confirm.

## UI/UX

Focused minimal style, light and dark. Primary red-orange #E64A19 for focus, accent green #43A047 for breaks, background #FFF8F5. Font Poppins (bundled). Big numerals, smooth ring animation, text labels for phases. Reusable TimerRing, PhaseChip, StatCard.

## FUNCTIONALITY

- Timer uses end-timestamp logic so it stays accurate when the app is backgrounded or the screen is locked.
- A scheduled notification fires when the phase ends; phase auto-advance; long break after N focus sessions.
- Session logging, daily goal and statistics.
- Settings persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for phase sequencing, remaining-time calculation from timestamps, statistics and the session repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 144. HOME INVENTORY POCKET

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 144. HOME INVENTORY POCKET

## APPLICATION PURPOSE

Build "Home Inventory Pocket", a Flutter app that records household items, warranties and purchase dates. It solves the problem of not knowing what is owned, what it cost or whether a warranty is still valid when something breaks. Target users are home owners and renters; main use case: add items by room, track warranty expiry and find items quickly.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, share_plus (CSV export), intl.

## SCREENS

1. Home – item count, total recorded value, warranties expiring soon; empty state.
2. Items – list grouped by room with search and filters; Add Item.
3. Add/Edit Item – name, room, category, quantity, purchase date, price, store, warranty end date, serial note (optional text), notes; validation.
4. Item Detail – warranty status and days left, purchase details; edit; delete with confirm.
5. Warranties – items sorted by warranty expiry with Expired, Soon and Valid sections.
6. Rooms & Categories – add, rename, delete.
7. Settings – currency, warranty reminder lead time, CSV export, theme, reset.

## NAVIGATION

Bottom tabs Home, Items, Warranties, Settings; floating Add. Back returns one level.

## UI/UX

Tidy household style, light and dark. Primary brown-teal #00695C, accent amber #FFA000, background #F4F8F7. Font Nunito Sans (bundled). Room icons, warranty status by icon and text. Reusable ItemTile, WarrantyChip, RoomHeader.

## FUNCTIONALITY

- Warranty status from days left; total value = sum of price x quantity.
- Search by name, room, category; filters.
- Reminders before warranty end; reschedule on edit and restart.
- CSV export; validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no receipts uploaded, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for warranty status, value totals, search and filters, reminder scheduling and repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 145. SAVINGS MILESTONE TRACKER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 145. SAVINGS MILESTONE TRACKER

## APPLICATION PURPOSE

Build "Savings Milestone Tracker", a Flutter app that tracks savings targets with progress indicators and milestones. It solves the problem of savings goals feeling endless and unmeasured. Target users are working adults; main use case: create goals, log deposits manually and watch progress toward milestones. Assumption: all amounts are entered manually; there is no bank connection.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl, confetti (milestone celebration, optional).

## SCREENS

1. Goals – goal cards with progress ring, saved/target and next milestone; empty state; Add Goal.
2. Add/Edit Goal – name, icon, target amount, optional target date, starting amount, custom milestones; validation.
3. Goal Detail – progress ring, milestone list (25/50/75/100% plus custom) with reached marks, deposit and withdrawal history, projected completion date, line chart.
4. Add Deposit – amount, date, note, deposit or withdrawal.
5. Completed Goals – finished goals with completion date.
6. Settings – currency, celebrations on/off, theme, reset.

## NAVIGATION

Goals > Detail > Add Deposit; Completed from Goals; Settings from the app bar. Back returns one level.

## UI/UX

Encouraging finance style, light and dark. Primary green #2E7D32, accent gold #FFC107, background #F4FAF4. Font Manrope (bundled). Large progress rings with text percentages, gentle celebration animation. Reusable GoalCard, MilestoneRow, ProgressRing.

## FUNCTIONALITY

- Progress = saved / target; milestones reached automatically.
- Projection = remaining / average monthly contribution (needs at least two months of data, otherwise hidden).
- Target date check: required monthly saving to hit the date.
- Withdrawals allowed without going below zero; validation; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank link, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for progress and milestones, projection and required monthly saving, deposit/withdrawal rules and repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 146. DEBT REPAYMENT PLANNER

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 146. DEBT REPAYMENT PLANNER

## APPLICATION PURPOSE

Build "Debt Repayment Planner", a Flutter app that compares repayment schedules using manually entered loan figures. It solves the problem of not knowing how long debts will last or how much interest extra payments save. Target users are working adults with loans or card balances; main use case: enter debts, try extra payments and strategies, and compare payoff time and total interest. Assumption: the app uses simple monthly compounding (balance x annual rate / 12) and states that real lender terms may differ; it gives no financial advice.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences, fl_chart, intl. Calculations in a pure-Dart service for testing.

## SCREENS

1. Debts – list with balance, rate and minimum payment; totals; empty state; Add Debt.
2. Add/Edit Debt – name, current balance, annual interest rate percent, minimum monthly payment; validation (balance > 0, rate 0-100, minimum > 0).
3. Plan Setup – extra monthly payment amount and strategy: Minimum only, Avalanche (highest rate first), Snowball (smallest balance first).
4. Comparison – cards for each strategy showing months to debt-free, total interest and interest saved versus minimum-only; balance-over-time line chart.
5. Schedule – month-by-month table (payment, interest, principal, balance) for the chosen strategy with per-debt view.
6. Settings – currency, theme, reset.

## NAVIGATION

Debts > Plan Setup > Comparison > Schedule. Bottom tabs Debts, Plan, Compare; Settings from the app bar. Back returns one level.

## UI/UX

Serious but clear finance style, light and dark. Primary navy #1A237E, accent teal #00ACC1, red #D32F2F for warnings, background #F5F6FB. Font IBM Plex Sans (bundled). Tabular numbers, charts with text labels. Reusable DebtCard, StrategyCard, ScheduleTable.

## FUNCTIONALITY

- Monthly simulation: add interest, apply minimums, apply extra payment per strategy, roll freed payments to the next target debt.
- Detect payment below interest (never pays off) and show a clear warning; cap simulation at 600 months.
- Totals and interest saved; schedule generation; persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no lender connections, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for single-debt payoff math, avalanche and snowball ordering, payment-below-interest detection and the iteration cap and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 147. MONTHLY SUBSCRIPTION AUDIT

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 147. MONTHLY SUBSCRIPTION AUDIT

## APPLICATION PURPOSE

Build "Monthly Subscription Audit", a Flutter app that lists recurring payments and helps identify services to reconsider. It solves the problem of forgotten subscriptions quietly draining money. Target users are working adults; main use case: record subscriptions, rate how much each is used and review which to keep or cancel. The app only records and reminds; it never cancels anything.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart, intl.

## SCREENS

1. Overview – monthly total, yearly total, donut by category, upcoming renewals; empty state.
2. Subscriptions – list with cost, cycle, next renewal and decision chip; search and filters.
3. Add/Edit Subscription – name, cost, billing cycle (weekly, monthly, quarterly, yearly), next renewal date, category, usage rating 1-5, decision (Keep, Review, Cancel), notes, reminder; validation.
4. Audit Mode – step through each subscription as a card showing cost per use rating; buttons Keep, Review, Cancel.
5. Savings – potential monthly and yearly savings from items marked Cancel; ranked list of high-cost low-usage subscriptions.
6. Settings – currency, renewal reminder lead days, theme, reset.

## NAVIGATION

Bottom tabs Overview, List, Audit, Savings; Settings from the app bar. Back returns one level.

## UI/UX

Clean money-hygiene style, light and dark. Primary purple #6A1B9A, accent green #2E7D32 (savings), background #FAF6FC. Font DM Sans (bundled). Decision chips with icon and text. Reusable SubCard, DecisionChip,

SavingsBanner.

## FUNCTIONALITY

- Normalise costs to monthly and yearly (weekly x 52/12, quarterly / 3, yearly / 12).
- Reconsider ranking = high cost with low usage rating.
- Next-renewal roll-forward after the date passes; reminders before renewal.
- Validation and persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no bank or email scanning, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for cost normalisation, ranking, renewal roll-forward, savings totals and repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 148. PERSONAL ACHIEVEMENT LOG

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 148. PERSONAL ACHIEVEMENT LOG

## APPLICATION PURPOSE

Build "Personal Achievement Log", a Flutter app for recording completed tasks, milestones and accomplishments. It solves the problem of forgetting wins when preparing for appraisals, interviews or CV updates. Target users are working adults; main use case: log achievements as they happen and generate a summary for any period.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone (weekly nudge), share_plus, fl_chart, intl.

## SCREENS

1. Timeline – achievements newest first grouped by month with category chips; search; empty state; Add button.
2. Add/Edit Achievement – title, date, category (Work, Learning, Fitness, Personal, Financial, Other), description, measurable result or impact, tags, significance 1-3 stars; validation.
3. Achievement Detail – full entry; edit and delete with confirm.
4. Insights – counts by category and month, months logged in a row, top tags; chart.
5. Review Report – choose a date range and categories; formatted summary shown and shared as plain text.
6. Settings – categories, weekly reminder day and time, theme, reset.

## NAVIGATION

Bottom tabs Timeline, Insights, Report, Settings; floating Add. Back returns one level.

## UI/UX

Warm proud-but-minimal style, light and dark. Primary amber-brown #F57F17, accent indigo #3F51B5, background #FFFBF2. Font Poppins (bundled). Star ratings with text alternative, soft card shadows. Reusable AchievementCard, CategoryChip, StarRow.

## FUNCTIONALITY

- Entry CRUD, tag and category search.
- Aggregations by month and category; consecutive-months-logged counter.
- Report generator groups entries by category with dates and results in clean text.
- Weekly reminder, validation, persistence.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account or cloud; entries stay on the device.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for aggregation, months-in-a-row logic, report text generation and the repository and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 149. QUICK MEAL SELECTOR

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 149. QUICK MEAL SELECTOR

## APPLICATION PURPOSE

Build "Quick Meal Selector", a Flutter app that suggests meal ideas from the ingredients the user has and the time available to cook. It solves the problem of staring into the fridge deciding what to make. Target users are busy working adults; main use case: enter ingredients and a time limit, then pick from ranked recipe suggestions. Assumption: the team writes about 60 simple recipes (ingredients, time, steps, vegetarian flag) in JSON and tests them for sensible quantities.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, shared_preferences or sqflite (pantry, favourites), intl.

## SCREENS

1. Home – ingredient entry with chips and autocomplete, time filter (10, 20, 30, 45+ minutes), Find Meals button; empty state.
2. Suggestions – ranked recipe cards with match percentage, time, missing ingredients; sort and filter.
3. Recipe Detail – ingredients (have/missing marked), steps, servings scaler, Favourite, Add Missing to Shopping List.
4. Pantry – saved staples that are always counted as available.
5. Shopping List – missing items with check-off.
6. Favourites – saved recipes.
7. Settings – vegetarian-only filter, excluded ingredients, units, theme.

## NAVIGATION

Bottom tabs Home, Pantry, Favourites, Shopping; Settings from the app bar. Suggestions > Detail > back keeps the ingredient state.

## UI/UX

Fresh kitchen style, light and dark. Primary orange #EF6C00, accent green #7CB342, background #FFF9F2. Font Nunito (bundled). Large recipe cards, have/missing marks with icon and text. Reusable RecipeCard, IngredientChip, MatchBadge.

## FUNCTIONALITY

- Ingredient normalisation (lowercase, trim, simple plural and synonym map).
- Match score = matched required ingredients / total required, pantry staples counted; recipes within the time limit ranked by score then speed.
- Excluded-ingredient and vegetarian filters; servings scaling; missing-items shopping list.
- Persistence of pantry, favourites and list.

## DATA AND BACKEND

Bundled JSON and local storage; no recipe APIs, account or cloud.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for ingredient normalisation, match scoring and ranking, filters and servings scaling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---

## 150. LIFE ADMIN DASHBOARD

```text
# FLUTTER APPLICATION DEVELOPMENT PROMPT — 150. LIFE ADMIN DASHBOARD

## APPLICATION PURPOSE

Build "Life Admin Dashboard", a Flutter app that brings tasks, bills, appointments, goals and document reminders into one compact dashboard. It solves the problem of everyday obligations scattered across notes, messages and memory. Target users are working adults; main use case: see everything due today and this week in one place and add items in seconds. Assumption: this app is self-contained; each of the five item types is a lightweight module sharing one data model rather than a copy of the full dedicated apps.

## TECHNOLOGY

Flutter, Dart, Android. Packages: provider, sqflite, shared_preferences,

flutter_local_notifications + timezone, fl_chart (goal progress), intl, table_calendar.

## SCREENS

1. Dashboard – cards for Today, This Week, Overdue, Bills Due (with total), Appointments, Goals progress and Documents Expiring; empty state with quick-add buttons.
2. Calendar – month view with type-coloured markers; day list.
3. Add Item – chooser for Task, Bill, Appointment, Goal or Document, then a form with only the fields that type needs (title, date/time, amount, recurrence, progress target, reminder, notes); validation.
4. Items – tabs per type with search, status filters and swipe to complete or delete.
5. Item Detail – edit, complete or mark paid, history of completions, delete with confirm.
6. Settings – default reminder times, notification permission status, theme, reset.

## NAVIGATION

Bottom tabs Dashboard, Calendar, Items, Settings; centre Add button. Back returns one level.

## UI/UX

Compact organised style, light and dark. Primary blue #3F51B5, accent teal #00BFA5, background #F5F7FB. Font Inter (bundled). Type icons and text labels, compact cards, 8dp grid. Reusable DashboardCard, ItemTile, TypeChip.

## FUNCTIONALITY

- Single LifeItem model (type, title, due date-time, amount, recurrence, progress, status, reminder offset, notes).
- Unified timeline sorted by due date; overdue detection; recurrence next-date rules.
- Goal progress updates; document expiry status; bill totals due this week.
- Reminders per item rescheduled on edit, completion, boot and restart.

## DATA AND BACKEND

Local sqflite and shared_preferences; no account, cloud, calendar or bank integrations.

## DEVELOPMENT, TESTING AND DELIVERABLES

Development: complete Flutter/Dart project (null safety) with organised folders (models, screens, widgets, services, repositories, utils), reusable widgets, helpful comments, and handling for invalid input and exceptions. Implement every screen, route and feature above. Build the real working app, not a visual prototype or static mock; add no unrelated features; do not claim an integration works if it is only simulated. If too large for one response, work in phases, keep working code intact and continue until all essential functionality is done. Testing: run flutter pub get, flutter analyze (fix errors, address warnings) and flutter test. Write tests for unified sorting and overdue logic, recurrence rules, dashboard aggregation and reminder scheduling and main flows; verify navigation, validation, persistence and core features; run on an Android emulator or device if available and check for crashes, overflow and broken controls. Report actual results and clearly state anything that could not be verified. Deliverables: complete project, clear folder structure, all source files; working screens, navigation and core features; setup and run instructions; tests with real results; release APK steps (flutter build apk --release); limitations and any configuration still required. Finish with a summary of what was implemented, tested and what remains.
```

---
