# Cozy Sleep Trainer

A sleep-training timer built for the Light Phone using the Light SDK and Jetpack Compose.

Cozy Sleep Trainer provides a simple Ferber-style interval timer designed for parents who want a low-distraction way to track sleep-training intervals without relying on a smartphone.

## Project Links

- [Source Code](https://github.com/For-His-Glory/light-sdk/tree/cozy-sleep-trainer/examples/cozy-sleep-trainer)
- [Light Community Discussion](https://github.com/orgs/lightphone/discussions/154)

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

## Screenshots

<table>
  <tr>
    <td align="center">
      <strong>Home</strong><br>
      <img src="screenshots/home.png" alt="Cozy Sleep Trainer home screen" width="175">
    </td>
    <td align="center">
      <strong>Active Timer</strong><br>
      <img src="screenshots/active-timer.png" alt="Cozy Sleep Trainer active timer" width="175">
    </td>
    <td align="center">
      <strong>Interval Complete</strong><br>
      <img src="screenshots/interval-complete.png" alt="Cozy Sleep Trainer interval complete" width="175">
    </td>
  </tr>
<tr>
  <td align="center">
    <strong>Session Summary</strong><br>
    <img src="screenshots/session-summary.png" alt="Cozy Sleep Trainer session summary" width="175">
  </td>
  <td align="center">
    <strong>History</strong><br>
    <img src="screenshots/history.png" alt="Cozy Sleep Trainer history" width="175">
  </td>
</tr>
</table>

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

## Technology

- **Kotlin** — Application logic and Android development
- **Jetpack Compose** — User interface
- **Light SDK** — Light Phone integration and device-specific UI
- **Kotlin Coroutines** — Timer and asynchronous operations
- **Kotlin Serialization** — Session history serialization
- **Android DataStore** — Local session persistence
- **Gradle** — Build and dependency management
- **Git/GitHub** — Source control and project hosting

## Architecture

The application follows a simple flow:

```text
User
  ↓
Light Phone UI
  ↓
Jetpack Compose
  ↓
Sleep Trainer Screen
  ↓
Ferber Schedule + Timer State
  ↓
Session Data
  ↓
Android DataStore
  ↓ 
Session History
```

## Testing

The project includes unit tests for core timer and schedule logic.

Current tests verify:

- Timer formatting for zero seconds, seconds, and minutes
- Ferber interval progression
- The 15-minute interval repeating after the initial schedule

I also tested the application manually using the Android Studio Pixel 9 API 37.1 emulator, including:

- Starting and stopping sessions
- Timer countdown behavior
- Interval progression
- Session completion
- Session summary display
- Local history persistence
- History display after restarting the app

## What I Learned

Building Cozy Sleep Trainer gave me hands-on experience with:

- Learning Kotlin and Jetpack Compose by building a functioning application
- Working with an unfamiliar SDK and existing project structure
- Managing application state for a timer-based user interface
- Persisting application data locally with Android DataStore
- Writing and running basic unit tests
- Debugging UI and application behavior on an Android emulator
- Using Git branches, commits, and GitHub to manage and publish the project
- Iterating on a working MVP instead of over-engineering the application
## Light Community

Cozy Sleep Trainer was built using the Light SDK and shared with the Light Phone community through the community's Tools discussion.

[View the Cozy Sleep Trainer community discussion](https://github.com/orgs/lightphone/discussions/154)

## Future Improvements

Potential future improvements include:

- Testing the application on physical Light Phone hardware
- Adding more sleep-training schedules or customizable intervals
- Improving session history details
- Expanding automated test coverage
- Refining the user interface based on real-world use