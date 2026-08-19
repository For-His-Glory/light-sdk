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

<img src="screenshots/home.png" alt="Cozy Sleep Trainer home screen" width="175"

### Active Timer

![Cozy Sleep Trainer active timer](screenshots/active-timer.png)

### Interval Complete

![Cozy Sleep Trainer interval complete](screenshots/interval-complete.png)

### Session Summary

![Cozy Sleep Trainer session summary](screenshots/session-summary.png)

### History

![Cozy Sleep Trainer history](screenshots/history.png)