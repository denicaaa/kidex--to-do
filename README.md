# Kidex

Your first Macedonian task, reminder, and calendar app lives in [kidex/](./kidex/).

**Open your private app:** [Kidex · Мојот ден](https://kidex-plan-denia.spicyreed16384.chatgpt.site)

On Android, open this link in Chrome and use its menu to install the app or add it to your home screen. If asked, sign in with the account that owns the site. Tasks stay on each device for now; the in-app settings explain backups, installation, and reminders.

To try it on this computer, double-click [Start Kidex.cmd](./kidex/Start%20Kidex.cmd), then open **http://localhost:4173** in Chrome. Keep the command window open while you use this local preview. Stop it with Ctrl+C.

Read the [beginner guide](./kidex/README.md) for Android installation, voice input, backups, and the limits of this first version.

The native [Android project](./kidex/android/README.md) packages the screens for offline use, adds Android system speech input and document pickers, and includes a repeatable APK build script. Compiling its first APK requires the Android SDK and acceptance of Google's SDK licence.

Verified: 14 automated logic tests; browser checks for task creation/editing/completion/deletion/undo, reload persistence, calendar dates, Macedonian search, backup validation and export contents, safe rendering of imported text, simulated speech input, missed reminder delivery, and layouts at 360, 390, 768, and 1440 pixels. The speech update detects the known-failing editor preview, provides copyable Chrome instructions, and extracts dates/times from text dictated through the Android keyboard. Browser tests verify both the preview guard and the normal-browser speech review/error flow with a simulated recognizer. Offline reload passed with network requests blocked. This test environment still reported `navigator.onLine` as true under network emulation, so the offline status label was not verified under emulation. Actual Android microphone recognition and installation need testing on your phone. System notification permission and delivery were not tested on a physical device.
