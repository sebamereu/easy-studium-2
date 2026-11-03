# easy study

Android study-planning app: daily calendar, exam tracking (with CFU and
stats), and in-app chat between users, backed by Firebase.

## Features

- **Daily calendar** — view/edit events for the day (`DailyCalendarFragment`,
  `CalendarAdapter`)
- **Exam tracker** — add exams with CFU, see stats on completed/remaining
  exams (`ExamFragment`, `ExamStatFragment`, chart via AnyChart)
- **Chat** — realtime messaging between users (`ChatActivity`,
  `MessageAdapter`) over Firebase Realtime Database
- **Auth** — login/signup via Firebase Authentication
- **Daily reminder** — a foreground service + `AlarmManager` fires a
  notification every day at a fixed time to prompt the user to open the app

## Stack

- Java (+ a bit of Kotlin), Android (compileSdk 32, minSdk 26)
- Firebase: Authentication, Realtime Database
- AndroidX Navigation, ViewBinding, AnyChart for exam stats

## Build

```bash
./gradlew assembleDebug
```

Requires your own `google-services.json` from a Firebase project (not
committed) placed in `app/`.

## Status / possible next steps

- Migrate screens incrementally to Kotlin
- Add instrumented/unit tests (currently only the default JUnit/Espresso
  scaffolding is present)
- Move the hardcoded reminder time (08:30) to a user-configurable setting
