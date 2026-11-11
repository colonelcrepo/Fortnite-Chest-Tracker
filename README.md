# Fortnite-Chest-Tracker
A simple Fortnite chest tracker that keeps track of how many chests you open, your total chests across matches, and your average per match. Also tracks rare chests, sprite chests, and loot cannons. Uses Fortnite replay files to log your stats automatically, with experimental real-time tracking as well.

# Fortnite Chest Tracker

A simple, open-source Fortnite application that tracks how many chests you open, your average per match, and your overall statistics.

I made this because I wanted a way to keep track of how many chests I was opening while grinding for rare items, and couldn't really find anything that did exactly what I wanted.

## Features

- **Total Chests Opened** — Keeps track of how many chests you've opened across all your matches.
- **Average Chests Per Match** — Calculates your average based on your recorded matches.
- **Chest Categories** — Tracks normal chests, rare chests, sprite chests, and loot cannons separately.
- **Automatic Replay Tracking** — Analyzes Fortnite replays to update your stats after each match.
- **Experimental Live Tracking** — Attempts to count chests in real time using on-screen notifications.
- **Match Statistics** — Keeps your recorded stats organized and prevents duplicate match imports.

## Installation

1. Head over to the [Releases](../../releases) page.
2. Download the latest Windows ZIP.
3. Extract the ZIP file wherever you'd like.
4. Run `FortniteChestTracker.exe`.
5. Make sure **Record Replays** is enabled in your Fortnite settings.

No need to install any development tools or compile anything yourself.

## How It Works

The tracker uses Fortnite's built-in replay system to detect when you've opened chests.

Once a match ends, Fortnite saves its replay data. The application reads this data, identifies chest interactions, and attempts to determine which chests you personally opened rather than your teammates.

It then categorizes the chests and adds them to your overall statistics.

**Your confirmed stats update after matches, not during gameplay.** This is because the application needs Fortnite to finish saving the replay before it can analyze it.

### Experimental Live Tracking

There's also an optional feature that attempts to track chests while you're playing.

To enable it:

1. Open the application's **Tracking** menu.
2. Enable **Experimental Screen Detection**.
3. Select the monitor you're playing on.
4. Make sure your Fortnite chest notifications are visible and set to English.

This feature reads notifications on your screen to estimate how many chests you've opened.

It's still experimental and may miss or incorrectly count some chests. Live cannon detection isn't supported yet. Once the replay is analyzed, its confirmed counts replace the live estimates.

## Troubleshooting

**Chests aren't being counted?**

Make sure replays are enabled in Fortnite. Remember that regular tracking only updates after a match has finished and the replay is saved.

**Live tracking isn't working?**

Double-check that screen detection is enabled and the correct monitor is selected. This feature is still being worked on and isn't completely reliable.

**Some chests are missing or incorrectly categorized?**

Fortnite updates can change how containers are recorded. If you notice any issues, feel free to report them on the [Issues](../../issues) page.

## Building From Source

The project is completely open source. If you'd rather compile it yourself, clone the repository and build the desktop project using the required .NET SDK or the included build scripts.

The repository also includes a GitHub Actions workflow for automated builds.

The project is licensed under **GPL-3.0-or-later**. See the LICENSE file for more information.

## Support the Project ☕

This is a free, open-source project that I plan on continuing to improve.

If you find it useful and want to support development, you can leave a donation through Ko-fi. It's completely optional but appreciated!

**[Support me on Ko-fi](https://ko-fi.com/colonelc)**

## Disclaimer

This is an unofficial Fortnite application and isn't affiliated with or endorsed by Epic Games.

The tracker doesn't modify Fortnite or read its running process memory. However, compatibility with Fortnite updates and anti-cheat policies isn't guaranteed.
