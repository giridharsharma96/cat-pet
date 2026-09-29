# Cat Pet

A tiny native macOS desktop companion that lives above your windows, follows your pointer, reacts to what you are doing, and takes the occasional nap.

> **Apple Silicon only** · Requires macOS 12 Monterey or later

## Preview

<p align="center">
  <img width="192" height="208" alt="Cat Pet desktop companion" src="https://github.com/user-attachments/assets/7f29e1ed-c275-4c4f-9b62-933faa60788c" />
</p>

## Download

Download the latest ready-to-run ZIP from the [Releases page](https://github.com/giridharsharma96/cat-pet/releases/latest).

1. Download `Cat-Pet-1.2.0-macOS-arm64.zip`.
2. Unzip it and move **Cat Pet.app** to your **Applications** folder.
3. Double-click **Cat Pet.app** once. Because this release is ad-hoc signed and not notarized, macOS may block the first launch.
4. If it is blocked, open **Apple menu → System Settings → Privacy & Security**.
5. Scroll down to the **Security** section, find the message about **Cat Pet**, and click **Open Anyway**. This option is normally available for about one hour after the blocked launch attempt.
6. Enter your Mac login password or use Touch ID if prompted. When the warning appears again, click **Open**.
7. Cat Pet is now saved as an exception. Future launches work by double-clicking the app normally. Use the paw menu or right-click the cat to access its controls.

See [Apple's official instructions for opening an app from an unidentified developer](https://support.apple.com/102445).

> **Security notice:** Only choose **Open Anyway** if you downloaded Cat Pet from this repository and trust the file. The current release is not Developer ID signed or notarized, so Apple has not checked it for known malware. Do not disable Gatekeeper globally.

## Features

- Transparent, always-on-top 192×208 desktop companion
- Drag the cat around your screen with left- and right-facing walk animations
- Eight-direction pointer-facing poses
- Idle, walking, grooming, and sleeping animations
- App-aware reactions and 80 randomized messages without immediate repeats
- Automatic ten-second naps after five minutes of inactivity
- Optional browser-site reactions for Safari, Chrome, Brave, and Chrome for Testing
- Menu-bar and right-click controls
- No third-party runtime or network connection required

## Menu-bar controls

Click the **paw icon** in the macOS menu bar to open Cat Pet's controls. You can also right-click the cat for quick access. A checkmark next to a setting means that feature is enabled.

<p align="center">
  <img width="272" height="336" alt="Cat Pet menu-bar controls" src="https://github.com/user-attachments/assets/a3e22028-4b79-4319-972d-32197b064b4c" />
</p>

You can drag the cat anywhere on the screen. Dragging plays the appropriate left- or right-facing walk animation; releasing it returns the cat to idle.

### One-time actions

- **Idle (Default)** — Stops the current temporary action and returns the cat to its normal idle state.
- **Walk Left Once** — Plays one left-facing walking cycle in place, then returns to idle.
- **Walk Right Once** — Plays one right-facing walking cycle in place, then returns to idle.
- **Sleep Briefly** — Puts the cat into its sleeping pose for about three seconds, then returns to idle.
- **Groom Once** — Plays one grooming animation, then returns to idle.

### Settings and status

- **Face Pointer** — While idle, the cat looks toward the pointer using eight directional poses. The cat stays in place.
- **App Reactions** — Shows local speech bubbles when the foreground app changes.
- **Browser Site Detection** — Enables optional reactions based on the active website. It is disabled by default, checks the active tab about every five seconds, and requires macOS Automation permission for each supported browser. Cat Pet uses the hostname only for a temporary local reaction; it does not save or transmit browsing data. Supported browsers are Safari, Chrome, Brave, and Chrome for Testing.
- **Idle Chatter** — Shows an occasional message after five minutes without activity, then at random intervals of roughly five to ten minutes. Activity resets the timer.
- **Browser Detection Status…** — Opens a local status window listing registered browsers and whether Cat Pet can detect sites in each one, including permission or support information.
- **Quit Cat Pet** — Closes both the desktop pet and its menu-bar app completely.

## Privacy

Cat Pet runs locally and contains no telemetry. It does not log, save, or transmit URLs, browsing history, app activity, keystrokes, or pointer activity.

Optional Browser Site Detection reads the active tab only to extract its hostname for a local reaction. It requires macOS Automation permission for each supported browser and can be turned off at any time. Idle behaviour uses only the system's aggregate inactivity duration.

## Compatibility

| Requirement | Supported |
| --- | --- |
| macOS | 12 Monterey or later |
| Apple Silicon | Yes (arm64) |
| Intel Mac | Not supported by the current download |
| Internet connection | Not required |

## Current release

**Cat Pet 1.2.0 (build 3)**

SHA-256 for `Cat-Pet-1.2.0-macOS-arm64.zip`:

```text
f2df58a717784bf0342d5aa7f59a3d9dfb405975853d34022af2c3f1f6c5e435
```

Automated logic and resource tests, property-list validation, strict code-signature verification, and ZIP integrity checks passed. Live browser-permission flows and end-to-end UI behaviour have not yet been manually verified.
