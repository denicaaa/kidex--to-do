# Kidex

Your first Macedonian task, reminder, and calendar app lives in [kidex/](./kidex/).

**Open and share the public app:** [Kidex · Мојот ден](https://kidex-plan-denia.deni-acoski.chatgpt.site)

Anyone with this link can open the app without a ChatGPT account. On Android, open it in Chrome and use its menu to install the app or add it to your home screen. Each person's tasks stay on their own device; the in-app settings explain backups, installation, and reminders.

To try it on this computer, double-click [Start Kidex.cmd](./kidex/Start%20Kidex.cmd), then open **http://localhost:4173** in Chrome. Keep the command window open while you use this local preview. Stop it with Ctrl+C.

Read the [beginner guide](./kidex/README.md) for Android installation, voice input, backups, and the limits of this first version.

The native [Android project](./kidex/android/README.md) packages the screens for offline use, adds Android system speech input and document pickers, and includes [a signed release APK builder](./kidex/android/Build%20Release.ps1) for sharing the app with others. Compiling an APK on this computer requires the Android SDK and acceptance of Google's SDK licence. The rebuild was deferred at your request on 20 November 2026. Updated launcher artwork is prepared in source, but no new APK has been produced in this checkout.

Voice entry now stays in listening mode through pauses and phrase endings until you press **Запри** or save/close the form. The 30-second app timeout is removed. All phrases accumulate in a full transcript, and Stop or Save waits for the last recognized words. Long text is retained with a clear task-title length message. Where supported, the screen stays awake while you dictate. Leaving the app or a real speech-service error ends microphone use.

The November update adds an Outlook-style month/week/day calendar, direct month/year selection, and three consistent colour-coded groups: Дома, Работа, and Останато. Change group colours in Settings; colours travel with backups. Your supplied wordmark and app-icon artwork replace the original placeholder branding.

The Chrome-installed version now follows the device's light/dark setting by default, with optional overrides in Settings. Light uses `#ece9e2`; dark uses `#1e1e1e`. Long-press the installed app icon for Calendar, Voice, or New task shortcuts. A real live calendar or combined 2×1 Android launcher widget still needs an Android package; those widgets are not available through Chrome-only installation.

The microphone now has an explicit permission/check action under **Поставки → Микрофон**. Chrome-installed apps use Chrome/site microphone permissions, so a separate Kidex Android permission entry is not required. Permission checks release their capture tracks immediately, including late responses after cancellation. An authorized, visible voice shortcut attempts to listen once; first-use/blocked shortcuts show a start/permission button. A launch URL is consumed to prevent another recording on refresh. Microphone access and the browser's speech-service/language support are diagnosed separately.

Verified: 65 automated tests cover task/backup migration, dates, calendar layouts, colours, notifications, offline-shell assets, shortcuts, theme changes, microphone permission/cancellation, real app voice-entry flows, speech sessions, and the Android adapter. Browser checks cover desktop and phone layouts, exact theme colours, saved overrides, first-use voice consent, month jumping, groups, and colour persistence. Actual phone microphone recognition and OS sound/vibration still need a real-device check. Web notifications require a running browser app; closed-app Web Push needs an additional backend. Native closed-app Android alarms and APK rebuilding remain deferred. Data is local per device.
