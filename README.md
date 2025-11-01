# 📘 100 ADB Commands — Categorized & Explained (2025 Edition)

This document lists **100 essential ADB (Android Debug Bridge) commands** categorized by their use case, with a brief description, usage example, and a probability score showing how commonly each is used in 2025.

-

## ⚙️ 1. Core ADB Server & Device Management

| # | Command | Usage / Example |
|-|-|-|-|
| 1 | `adb devices` | Lists connected devices and emulators. | 1.0 |
| 2 | `adb version` | Shows ADB version. | 0.9 |
| 3 | `adb kill-server` | Stops ADB server process. | 0.85 |
| 4 | `adb start-server` | Starts ADB server process. | 0.85 |
| 5 | `adb connect <ip>:5555` | Connects to device over Wi-Fi. | 0.9 |
| 6 | `adb disconnect <ip>:5555` | Disconnects Wi-Fi device. | 0.85 |
| 7 | `adb tcpip 5555` | Enables TCP/IP debugging. | 0.9 |
| 8 | `adb root` | Restarts adbd with root permissions. | 0.5 |
| 9 | `adb remount` | Mounts system partition writable. | 0.5 |
| 10 | `adb reboot` | Reboots device. | 0.9 |
| 11 | `adb reboot recovery` | Reboots to recovery. | 0.6 |
| 12 | `adb reboot bootloader` | Reboots to fastboot mode. | 0.7 |
| 13 | `adb reboot edl` | Reboots to Qualcomm EDL. | 0.4 |

-

## 📦 2. App Installation & Management

| # | Command | Usage / Example |
|-|-|-|-|
| 14 | `adb install app.apk` | Installs APK. | 1.0 |
| 15 | `adb install -r app.apk` | Reinstalls APK, keeping data. | 0.95 |
| 16 | `adb install -d app.apk` | Allows version downgrade. | 0.7 |
| 17 | `adb install -t app.apk` | Installs test APK. | 0.6 |
| 18 | `adb uninstall com.app` | Uninstalls app. | 1.0 |
| 19 | `adb uninstall -k com.app` | Keeps data after uninstall. | 0.7 |
| 20 | `adb shell pm list packages` | Lists installed packages. | 0.95 |
| 21 | `adb shell pm list packages -3` | Lists third-party apps. | 0.9 |
| 22 | `adb shell pm path com.app` | Gets APK path. | 0.8 |
| 23 | `adb shell pm clear com.app` | Clears app data and cache. | 0.95 |
| 24 | `adb shell pm grant com.app android.permission.CAMERA` | Grants permission. | 0.9 |
| 25 | `adb shell pm revoke com.app android.permission.CAMERA` | Revokes permission. | 0.8 |
| 26 | `adb shell pm disable-user com.app` | Disables app. | 0.6 |
| 27 | `adb shell pm enable com.app` | Enables app. | 0.6 |
| 28 | `adb shell cmd package install-existing com.app` | Reinstalls built-in app. | 0.6 |

-

## 🧭 3. App Activity & Intent Control

| # | Command | Usage / Example |
|-|-|-|-|
| 29 | `adb shell am start -n com.app/.MainActivity` | Launches activity. | 0.9 |
| 30 | `adb shell am start -a android.intent.action.VIEW -d https://site.com` | Opens URL/deep link. | 0.85 |
| 31 | `adb shell am force-stop com.app` | Force-stops app. | 0.9 |
| 32 | `adb shell am broadcast -a com.app.CUSTOM_EVENT` | Sends broadcast intent. | 0.8 |
| 33 | `adb shell am instrument -w com.app.test/androidx.test.runner.AndroidJUnitRunner` | Runs instrumentation tests. | 0.7 |

-

## 🧪 4. Debugging & Logs

| # | Command | Usage / Example |
|-|-|-|-|
| 34 | `adb logcat` | Shows logs. | 1.0 |
| 35 | `adb logcat -c` | Clears log buffer. | 0.85 |
| 36 | `adb logcat -d > log.txt` | Dumps logs to file. | 0.9 |
| 37 | `adb logcat *:E` | Filters errors. | 0.9 |
| 38 | `adb bugreport` | Full bug report. | 0.8 |
| 39 | `adb shell dumpsys` | Dumps system info. | 0.9 |
| 40 | `adb shell dumpsys activity` | Activity manager info. | 0.8 |
| 41 | `adb shell dumpsys meminfo com.app` | Memory stats. | 0.85 |
| 42 | `adb shell dumpsys battery` | Battery info. | 0.8 |
| 43 | `adb shell dumpsys window displays` | Display metrics. | 0.8 |
| 44 | `adb shell dumpsys wifi` | Wi-Fi info. | 0.6 |

-

## 💾 5. File System & Data Handling

| # | Command | Usage / Example |
|-|-|-|-|
| 45 | `adb push local.txt /sdcard/` | Push file to device. | 0.9 |
| 46 | `adb pull /sdcard/data.txt ./` | Pull file from device. | 0.9 |
| 47 | `adb shell ls /sdcard/` | List files. | 0.85 |
| 48 | `adb shell cat /sdcard/config.json` | Read file. | 0.8 |
| 49 | `adb shell mkdir /sdcard/testdir` | Create directory. | 0.75 |
| 50 | `adb shell rm /sdcard/test.txt` | Delete file. | 0.75 |

-

## 🧠 6. System Properties & Settings

| # | Command | Usage / Example |
|-|-|-|-|
| 53 | `adb shell getprop` | List system properties. | 0.85 |
| 54 | `adb shell getprop ro.build.version.release` | Android version. | 0.9 |
| 55 | `adb shell getprop ro.product.model` | Device model. | 0.9 |
| 56 | `adb shell getprop ro.serialno` | Serial number. | 0.85 |
| 57 | `adb shell settings list system` | List settings. | 0.75 |
| 58 | `adb shell settings get system screen_brightness` | Get setting. | 0.7 |
| 59 | `adb shell settings put system screen_brightness 200` | Set setting. | 0.75 |
| 60 | `adb shell settings put global stay_on_while_plugged_in 3` | Keep screen on. | 0.8 |

-

## 🖥️ 7. Screen, Input & Display Control

| # | Command | Usage / Example |
|-|-|-|-|
| 61 | `adb shell screencap /sdcard/screen.png` | Screenshot. | 0.9 |
| 62 | `adb pull /sdcard/screen.png` | Copy screenshot. | 0.9 |
| 63 | `adb shell screenrecord /sdcard/demo.mp4` | Record screen. | 0.9 |
| 64 | `adb shell input tap 500 800` | Tap screen. | 0.85 |
| 65 | `adb shell input swipe 200 500 200 100` | Swipe gesture. | 0.8 |
| 66 | `adb shell input text "hello"` | Input text. | 0.8 |
| 67 | `adb shell input keyevent 3` | Home button. | 0.85 |
| 68 | `adb shell input keyevent 4` | Back button. | 0.9 |
| 69 | `adb shell wm size` | Display size. | 0.8 |
| 70 | `adb shell wm density` | Display density. | 0.8 |

-

## 🌐 8. Network, Power & Connectivity

| # | Command | Usage / Example |
|-|-|-|-|
| 73 | `adb shell svc wifi enable` | Enable Wi-Fi. | 0.75 |
| 74 | `adb shell svc wifi disable` | Disable Wi-Fi. | 0.75 |
| 75 | `adb shell svc data enable` | Enable data. | 0.7 |
| 76 | `adb shell svc data disable` | Disable data. | 0.7 |
| 77 | `adb shell svc bluetooth enable` | Enable Bluetooth. | 0.7 |
| 78 | `adb shell svc bluetooth disable` | Disable Bluetooth. | 0.7 |
| 79 | `adb shell svc power stayon true` | Keep awake. | 0.8 |
| 80 | `adb shell cmd connectivity airplane-mode enable` | Airplane mode ON. | 0.7 |
| 81 | `adb shell cmd connectivity airplane-mode disable` | Airplane mode OFF. | 0.7 |

-

## 🔋 9. Battery & Power Simulation

| # | Command | Usage / Example |
|-|-|-|-|
| 82 | `adb shell cmd battery unplug` | Simulate unplugged. | 0.75 |
| 83 | `adb shell cmd battery set level 50` | Fake battery level. | 0.7 |
| 84 | `adb shell cmd battery reset` | Reset battery state. | 0.7 |
| 85 | `adb shell cmd battery set status 2` | Charging status. | 0.6 |

-

## 🧩 10. Developer Tools, Automation & Testing

| # | Command | Usage / Example |
|-|-|-|-|
| 86 | `adb shell cmd package list features` | List features. | 0.7 |
| 87 | `adb shell cmd package list permissions` | List permissions. | 0.7 |
| 88 | `adb shell cmd package dump com.app` | Dump package info. | 0.75 |
| 89 | `adb shell cmd package resolve-activity <intent>` | Resolve intent activity. | 0.6 |
| 90 | `adb shell cmd package snapshot` | Snapshot packages. | 0.6 |
| 91 | `adb shell input keyevent 26` | Power key. | 0.8 |
| 92 | `adb shell cmd vibrator vibrate 300` | Vibrate for 300ms. | 0.6 |
| 93 | `adb shell top` | CPU/memory monitor. | 0.85 |
| 94 | `adb shell ps` | Process list. | 0.8 |
| 95 | `adb forward tcp:8080 tcp:8080` | Port forward. | 0.75 |
| 96 | `adb reverse tcp:8080 tcp:8080` | Reverse port forward. | 0.75 |

-

## 🧭 11. Emulator & Location Control

| # | Command | Usage / Example |
|-|-|-|-|
| 97 | `adb emu geo fix 77.5946 12.9716` | Set fake GPS. | 0.75 |
| 98 | `adb emu geo nmea <nmea-string>` | Send NMEA data. | 0.5 |
| 99 | `adb emu avd name` | Emulator AVD name. | 0.6 |
| 100 | `adb emu kill` | Shut down emulator. | 0.7 |

-

## 📊 Probability Meaning

| Range | Meaning | Example |
|-|-|-|
| 0.9–1.0 | Everyday essential commands | `adb devices`, `adb install`, `adb logcat` |
| 0.7–0.8 | Regular dev/test utilities | `adb shell screencap`, `adb shell dumpsys` |
| 0.5–0.6 | Advanced / rooted / niche use | `adb root`, `adb remount` |

-

**Author:** *Mobile Architect & Tech Blogger (2025)*  
**License:** MIT  
**GitHub Repo:** [YourRepoName](#)

