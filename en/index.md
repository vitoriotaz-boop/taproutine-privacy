---
layout: page
title: "TapRoutine Privacy Policy"
lang: en-US
permalink: /en/
description: "Privacy and data-use information for TapRoutine for Android."
eyebrow: "Privacy & data use"
brand_label: "Privacy"
home_label: "TapRoutine privacy policy home"
footer_label: "TapRoutine · Android"
contact_label: "Contact"
---

<p class="last-updated">Last updated: November 12, 2026</p>
<nav class="language-nav" aria-label="Language selection">
<a href="{{ '/' | relative_url }}" lang="pt-BR">Português (Brasil)</a>
<span aria-current="page" lang="en-US">English</span>
<a href="{{ '/es/' | relative_url }}" lang="es-419">Español</a>
<a href="{{ '/fr/' | relative_url }}" lang="fr-FR">Français</a>
<a href="{{ '/de/' | relative_url }}" lang="de-DE">Deutsch</a>
<a href="{{ '/it/' | relative_url }}" lang="it-IT">Italiano</a>
<a href="{{ '/ja/' | relative_url }}" lang="ja-JP">日本語</a>
</nav>

## About this app version

TapRoutine is an Android preview app that lets you configure a routine for a selected app, schedule it on the device, run user-defined steps, and check screen points by color. The inspected APK has package identifier `io.github.vitoriotaz.taproutine`, `minSdk` 24, `targetSdk` 36, and `android:allowBackup=true`. The findings in this notice apply to that preview APK and may not apply to future versions.

## Data the app creates or accesses

- **User routine and settings:** may include the routine name; the selected app’s name and package identifier; times, days, and time zone; steps and gestures (such as taps, swipes, waits, Back, or Home) and their positions; the color, point, and tolerance used for checks; and settings such as check frequency and whether to reopen the target app. Settings may also include Guardian and an alternate screen, with another preconfigured sequence.
- **Apps available to select:** TapRoutine queries Android to display apps that have a launchable activity. You select the target app; its name and package identifier are stored in the local routine.
- **Temporary foreground-window information:** while TapRoutine’s Accessibility Service is active, it receives Android `TYPE_WINDOW_STATE_CHANGED` events and keeps the package name reported by the system in memory. The service does not read the interface tree, text, fields, or other screen content.
- **Local data and logs:** routines and logs may contain times, the target app’s package, step and retry progress and results, technical failure details, and color values, screen points/positions, and screen resolution. `SharedPreferences` also store consent related to the disclosure and the states and times of schedules and Guardian.
- **Temporary capture for a color check:** when checking, the app captures the entire current screen in memory to calculate only the average color of a 3×3-pixel area at the indicated point. Capturing the screen for this color check requires Android 11 or later. Capture may occur during routine checks, alternate-screen detection, and Guardian operation; it is not necessarily limited to the target app or window. The app does not deliberately save the capture to a file. It is transient, and the associated resources are released in the normal flow.

## How the data is used

Data is used on the device to save and load the routine, schedule its execution, perform user-defined steps, compare the color at the configured point, and record results. Depending on the configuration, the detected color may select an already preconfigured alternate sequence or trigger Guardian’s preconfigured action. The app does not invent actions or interpret screen text or content to decide what to do.

## Processing, storage, and transmission

Routines and logs are kept in the app’s private local storage. `SharedPreferences` also hold the data described above, including consent related to the disclosure and schedule and Guardian states and times. The window package observed by the service is held in memory. Screen capture is transient; the app does not deliberately save it to a file and releases associated resources in the normal flow.

The inspected APK’s code does not implement an account, server, synchronization, analytics, ads, payments, or app-originated network calls. This does not mean that no copy can leave the device: Android/Google Auto Backup may copy data as described below. The selected target app may also have its own connections and data practices, which TapRoutine does not control.

If you choose to contact support by email, your message and the address used to send it will be transmitted by your email service so we can receive and reply. This is an external action you initiate, not an app-originated network call by TapRoutine.

## Android/Google Auto Backup

The inspected preview APK sets `android:allowBackup` to `true`. If Android Auto Backup is enabled, Android may copy the app’s private files and `SharedPreferences`—which may include routines, logs, consent, and schedule/Guardian states and times—to the user’s Google account/Drive as part of Android’s service. Behavior depends on backup settings, the Android version, and the device.

This backup is an Android/Google service, not a TapRoutine upload to the developer’s server. The app and developer do not have access to the backup copy. Clearing local app data or uninstalling the app should not be understood as a guarantee that a separate copy maintained by the backup service is removed.

## Retention and your options

The routine and logs remain in the app’s storage until replaced or removed. The prototype’s **Limpar** button (Portuguese for “Clear”) deletes the execution log. If the log grows very large, the prototype may also remove older entries and keep recent ones. Saving a changed configuration replaces the local routine; canceling the schedule stops scheduled execution but does not by itself delete the saved configuration. To remove the app’s local data, use Android’s app-storage controls to clear the app’s data or uninstall it; this does not guarantee removal of a separate backup copy, if one exists. The operating system may use different labels for these controls.

## Android services and permissions

- **Android Accessibility Service:** must be enabled by you in system settings to run configured gestures and perform checks. It receives `TYPE_WINDOW_STATE_CHANGED` events and keeps the package reported by the system in memory; it does not read the interface tree, text, or fields. Transient screen capture is used to calculate the color average described above.

- **`SCHEDULE_EXACT_ALARM`:** associated with scheduling exact alarms. If Android does not allow exact alarms, scheduling may be less precise and may be delayed.
- **`RECEIVE_BOOT_COMPLETED`:** lets the module receive a device-restart event so it can handle rescheduling routines.
- **`WAKE_LOCK`:** allows the device to stay awake during a run that needs to continue in the background.
- **`KILL_BACKGROUND_PROCESSES`:** associated with the preconfigured action of ending the target app’s background process when the routine is set to reopen it.
- **`POST_NOTIFICATIONS`:** associated with displaying local notifications, such as results.

Android controls the availability, grant, and authorization flow for these permissions, which may vary by settings, system version, and device; this notice does not assume that each one produces a particular runtime prompt. Grant only the permissions you consider necessary for the features you want to use.

## Intended age

This TapRoutine beta is intended for adults aged **18 or older**; it is not designed for children or teenagers.

## Future changes

The features and practices described here correspond to the inspected preview APK and may change. If a future version collects, transmits, shares, or retains additional data, or adds services, this policy should be reviewed to describe that version before its distribution. Refer to the policy version accompanying the approved build.

## Contact

Questions or requests about this policy: [vitoriotaz@gmail.com](mailto:vitoriotaz@gmail.com).
