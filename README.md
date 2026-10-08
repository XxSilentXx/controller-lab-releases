# Controller Lab (beta)

A Windows app for Fortnite players on PlayStation and Xbox controllers. It measures your controller (polling rate, stick deadzone, stick health, connection) and turns the numbers into Fortnite settings. It also has stick curves, one turbo button, and a guided USB polling overclock.

This is a test build. Thanks for trying it.

**[Download the latest version](https://github.com/XxSilentXx/controller-lab-releases/releases/latest)**: get `ControllerLab.exe` from the Assets list.

## Install

1. Download `ControllerLab.exe` and double-click it.
2. Windows shows **"Windows protected your PC"** because the beta isn't code-signed yet. Click **More info**, then **Run anyway**.
3. It installs itself to your user folder and adds **Controller Lab** to the Start menu. No admin rights or extra downloads are needed for measuring.

You need Windows 10 or 11 (64-bit). Windows 11 already has everything else the app needs.

## Curves and turbo need two free drivers

Measuring and Fortnite tuning work without them. Curves and turbo need both of these; install them, then restart your PC:

- [ViGEmBus](https://github.com/nefarius/ViGEmBus/releases/latest): the virtual controller games see.
- [HidHide](https://github.com/nefarius/HidHide/releases/latest): hides your real controller so the game doesn't see two.

Controller Lab manages HidHide on its own. You don't need to change anything in HidHide's window.

## What to try

1. **Home:** move both sticks and watch the trails. The rate should read about 250 Hz on PlayStation controllers over USB.
2. **Checkup:** run it with the controller put down during the "hands off" parts. You get a recommended Fortnite deadzone.
3. **Fortnite tuning:** answer the questions and copy the settings card.
4. **Curves** (needs the drivers):
   - Pick a preset, then press **Go on air before starting Fortnite**.
   - **Xbox controllers:** unplug and replug the controller once when the app asks.
   - In Fortnite, set your deadzones to 0 and the look curve to Linear, so you only feel the curve from the app.
5. **Turbo** (needs the drivers): pick a button, set the rate, go on air.
6. **Doctor → Polling overclock** (optional, PlayStation over USB): follow the three steps. In the author's setup, switch the top-left list from **Mice** to **All** before picking your controller.

Supported: DualShock 4, DualSense, DualSense Edge, the Sony wireless adapter, and Xbox controllers. Curves and turbo work with one Xbox controller connected at a time.

## Report a problem

In the app, open **Doctor** and press **Copy diagnostics**. Then paste the result into your message, with a sentence on what you did and what went wrong. The report covers versions, controllers, drivers and the app's log; your Windows user name is left out.

The app tells you in its side rail when a newer build is out.

## Uninstall

1. Turn off curves and turbo, then right-click the tray icon and choose **Quit Controller Lab**. If you turned on "Start with Windows", untick it first.
2. Delete `%LOCALAPPDATA%\Programs\ControllerLab` (the app) and `%LOCALAPPDATA%\ControllerLab` (settings and logs).
3. Delete the Start menu shortcut under `%APPDATA%\Microsoft\Windows\Start Menu\Programs`.

Your HidHide settings are put back whenever curves or turbo turn off, including after a crash or a power cut.

## Be aware

- Epic doesn't support any third-party input software, and turbo in Fortnite is widely reported as bannable. Using curves or turbo online is your call.
- Measuring never changes your controller or game settings. Curves and turbo change what games receive only while they're on air, and the app always shows when they are.

Controller Lab is an independent product and is not endorsed by or affiliated with Epic Games, Inc.
