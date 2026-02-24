# App Review Notes — HeartOxy

---

## Overview

HeartOxy is a heart rate zone training app for Apple Watch. Users start a workout session, select a target heart rate zone, and receive real-time intensity feedback as their heart rate moves between zones (Recovery, Low, Target, High, Peak). A post-workout summary with zone distribution is shown after each session. All data is stored locally on-device and in Apple HealthKit.

**No login or account is required to test the app.**

---

## Hardware Required

- Apple Watch Series 4 or later (paired with iPhone) — physical Apple Watch required to demonstrate core functionality
- iPhone for companion app (settings, live chart, workout history)

---

## HealthKit Usage Justification

| Permission | Type | Reason |
|-----------|------|--------|
| Heart Rate | Read + Write | Core feature — reads live HR during workout, writes HR samples via workout builder |
| Blood Oxygen (SpO₂) | Read + Write | Displayed alongside HR during workout sessions |
| Workouts | Read + Write | Creates, manages and saves HKWorkoutSession; workouts saved to Apple Health and visible in Fitness app |
| Sleep Analysis | Read | Detects sleep state during background monitoring sessions |

HeartOxy uses `HKWorkoutSession` with `.preparationAndRecovery` activity type for continuous heart rate sensor access. `HKWorkoutBuilder.finishWorkout()` is called on every session end, saving the workout to Apple Health.

---

## How to Test

### Initial Setup (iPhone)

1. Launch HeartOxy on iPhone
2. Complete the onboarding (8 screens, tap Next/Done)
3. Grant HealthKit permissions when prompted (Read and Write access)
4. Go to **Settings → Workout Settings**, enter an age (e.g. 35) and select a target HR zone (e.g. Fat Burn)

### Starting a Workout (Apple Watch)

1. Open HeartOxy on Apple Watch
2. Home screen shows live HR readings with a "Start Workout" label
3. Slide the **Slide to Start** button to begin
4. Zone bar appears showing current HR zone (e.g. "HR is in Fat Burning Zone")
5. As HR changes, zone bar updates with colour-coded feedback
6. Intensity feedback notifications appear when HR crosses intensity thresholds

### Stopping & Reviewing (Apple Watch + iPhone)

1. Slide **Slide to Stop** on Apple Watch to end the workout
2. Post-workout summary shows Duration, Avg/Max/Min HR, and Zone Distribution
3. On iPhone, open **History** tab to view the Live Workout chart
4. Workout is saved to Apple Health and visible in the Fitness app

### Settings & Customisation (iPhone)

1. Go to **Settings → Workout Settings** to adjust intensity threshold sliders
2. Go to **Settings → Workout Settings → Advanced** to toggle which intensity levels trigger feedback
3. The **Feedbacks** tab shows a full history of intensity alerts

---

## Additional Notes

- HeartOxy is a fitness guidance tool only — not a medical device. A Fitness & Wellness Disclaimer is shown on first launch: https://github.com/dareindie/HeartOxy/blob/main/Fitness_Wellness_Disclaimer.md
- All health data remains on-device — no external servers used
- No internet connection required to function
- Privacy Policy: https://github.com/dareindie/HeartOxy/blob/main/PRIVACY_POLICY.md
- Marketing URL: https://github.com/dareindie/HeartOxy/blob/main/README.md

---

*HeartOxy — Heart Rate Zone Training for Apple Watch*
*Prepared for Apple App Store Review — February 2026*
