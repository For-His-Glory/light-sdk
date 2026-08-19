# Cozy Sleep Trainer

A sleep-training timer built for the Light Phone using the Light SDK and Jetpack Compose.

Cozy Sleep Trainer provides a simple Ferber-style interval timer designed for parents who want a low-distraction way to track sleep-training intervals without relying on a smartphone.

## Why I Built This

I built Cozy Sleep Trainer as my first real application from scratch while learning Kotlin, Android development, and the Light SDK.

The goal was to build and ship a small, useful application for a constrained device rather than focus on building a large or overly complex system.

The project also gave me an opportunity to learn how to work within an existing open-source SDK and integrate my application into its example project structure.

## Features

- Ferber-style sleep-training timer
- Interval progression: 2 → 5 → 10 → 15 → 15 minutes thereafter
- Start and stop controls
- Next interval control
- Vibration trigger when an interval completes
- Session completion summary
- Local session history
- Persistent history using Android DataStore
- Light Phone UI built with the Light SDK and Jetpack Compose
- Unit tests for timer formatting and interval schedule logic

## Screenshots

### Home

<img src="screenshots/home.png" alt="Cozy Sleep Trainer home screen" width="175">

### Active Timer

<img src="screenshots/active-timer.png" alt="Cozy Sleep Trainer active timer" width="175">

### Interval Complete

<img src="screenshots/interval-complete.png" alt="Cozy Sleep Trainer interval complete" width="175">

### Session Summary

<img src="screenshots/session-summary.png" alt="Cozy Sleep Trainer session summary" width="175">

### History

<img src="screenshots/history.png" alt="Cozy Sleep Trainer history" width="175">

## How It Works

Cozy Sleep Trainer uses a simple interval-based timer based on the Ferber sleep-training method.

1. The user starts a sleep-training session.
2. The app begins the current interval countdown.
3. When the interval reaches zero, the app triggers a vibration and pauses for the user to choose the next interval.
4. The user can stop the session or continue to the next interval.
5. Each completed interval contributes to the total session time.
6. When the user stops the session, the app saves the session locally and displays a summary.
7. Saved sessions can be viewed from the History screen.

The interval schedule is:

| Interval | Duration |
|---|---:|
| 1 | 2 minutes |
| 2 | 5 minutes |
| 3 | 10 minutes |
| 4 | 15 minutes |
| 5+ | 15 minutes |