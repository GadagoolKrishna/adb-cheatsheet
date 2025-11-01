# 🧰 Android Debug Bridge (ADB) Commands — 2025 Edition

> A complete, categorized reference of the 100 most useful ADB commands every Android developer should know.  
> Works great for debugging, deployment, automation, and device management.

---

## 📦 Installation & Device Setup

| Command | Description |
|----------|--------------|
| `adb devices` | Lists all connected Android devices and emulators. |
| `adb version` | Displays the ADB version installed. |
| `adb start-server` | Starts the ADB server process. |
| `adb kill-server` | Kills the ADB server process. |
| `adb connect <ip>:5555` | Connects to a device over Wi-Fi. |
| `adb disconnect <ip>:5555` | Disconnects a device connected over Wi-Fi. |
| `adb tcpip 5555` | Enables TCP/IP debugging on port 5555. |
| `adb reboot` | Reboots the device normally. |
| `adb reboot recovery` | Reboots the device into recovery mode. |
| `adb reboot bootloader` | Reboots into the bootloader/fastboot mode. |

---

## 📲 App Installation & Management

| Command | Description |
|----------|--------------|
| `adb install <apk_path>` | Installs an APK on the device. |
| `adb install -r <apk_path>` | Reinstalls an app while keeping data. |
| `adb install -d <apk_path>` | Allows version downgrade. |
| `adb install -t <apk_path>` | Installs test APKs. |
| `adb uninstall <package>` | Uninstalls an app from the device. |
| `adb uninstall -k <package>` | Uninstalls an app but retains data/cache. |
| `adb shell pm list packages` | Lists all installed packages. |
| `adb shell pm list packages -3` | Lists only third-party apps. |
| `adb shell pm path <package>` | Displays APK file path of a package. |
| `adb shell pm clear <package>` | Clears data and cache for an app. |
| `adb shell pm grant <package> <permission>` | Grants a runtime permission. |
| `adb shell pm revoke <package> <permission>` | Revokes a runtime permission. |
| `adb shell pm uninstall <package>` | Uninstalls an app via shell. |
| `adb shell pm disable-user <package>` | Disables a user app. |
| `adb shell pm enable <package>` | Re-enables a disabled app. |

---

## 🧠 Debugging & Development

| Command | Description |
|----------|--------------|
| `adb logcat` | Displays real-time system and app logs. |
| `adb logcat -c` | Clears logcat logs. |
| `adb logcat -d > log.txt` | Saves logs to a text file. |
| `adb logcat *:E` | Shows only error-level logs. |
| `adb shell am start -n <package>/<activity>` | Launches a specific activity. |
| `adb shell am start -a android.intent.action.VIEW -d <url>` | Opens a URL or deep link. |
| `adb shell am force-stop <package>` | Force-stops an app. |
| `adb shell am broadcast -a <intent>` | Sends a broadcast intent. |
| `adb shell am instrument -w <test_package>` | Runs instrumentation tests. |
| `adb shell dumpsys` | Dumps system service information. |
| `adb shell dumpsys activity` | Dumps activity manager state. |
| `adb shell dumpsys meminfo <package>` | Displays memory usage of an app. |
| `adb shell dumpsys battery` | Shows battery info. |
| `adb shell dumpsys wifi` | Displays Wi-Fi info. |
| `adb bugreport` | Generates a complete device bug report. |

---

## 🖥️ File Operations

| Command | Description |
|----------|--------------|
| `adb push <local> <remote>` | Copies files from your computer to the device. |
| `adb pull <remote> <local>` | Copies files from the device to your computer. |
| `adb shell ls` | Lists files in a directory. |
| `adb shell cat <file>` | Displays file content. |
| `adb shell mkdir <dir>` | Creates a new directory. |
| `adb shell rm <file>` | Deletes a file. |

---

## 📸 Screen & Input Control

| Command | Description |
|----------|--------------|
| `adb shell screencap /sdcard/screen.png` | Takes a screenshot. |
| `adb pull /sdcard/screen.png` | Pulls the screenshot to your computer. |
| `adb shell screenrecord /sdcard/demo.mp4` | Records the device screen. |
| `adb shell input tap <x> <y>` | Simulates a screen tap. |
| `adb shell input swipe <x1> <y1> <x2> <y2>` | Simulates a swipe gesture. |
| `adb shell input text "<string>"` | Simulates typing text. |
| `adb shell input keyevent <code>` | Simulates a hardware key event. |
| `adb shell input keyevent 26` | Toggles screen power. |
| `adb shell input keyevent 3` | Presses the Home button. |
| `adb shell input keyevent 4` | Presses the Back button. |

---

## 🌐 Network & Connectivity

| Command | Description |
|----------|--------------|
| `adb shell svc wifi enable` | Enables Wi-Fi. |
| `adb shell svc wifi disable` | Disables Wi-Fi. |
| `adb shell svc data enable` | Enables mobile data. |
| `adb shell svc data disable` | Disables mobile data. |
| `adb shell svc bluetooth enable` | Enables Bluetooth. |
| `adb shell svc bluetooth disable` | Disables Bluetooth. |
| `adb shell cmd connectivity airplane-mode enable` | Enables airplane mode. |
| `adb shell cmd connectivity airplane-mode disable` | Disables airplane mode. |
| `adb forward tcp:<local> tcp:<remote>` | Forwards a TCP port to the device. |
| `adb reverse tcp:<remote> tcp:<local>` | Reverses TCP forwarding. |

---

## ⚙️ System Configuration

| Command | Description |
|----------|--------------|
| `adb shell settings list system` | Lists all system settings. |
| `adb shell settings get system <key>` | Gets a system setting. |
| `adb shell settings put system <key> <value>` | Changes a system setting. |
| `adb shell settings put global stay_on_while_plugged_in 3` | Keeps the screen on while charging. |
| `adb shell getprop` | Lists system properties. |
| `adb shell getprop ro.build.version.release` | Gets Android version. |
| `adb shell getprop ro.product.model` | Gets device model name. |
| `adb shell getprop ro.serialno` | Gets device serial number. |
| `adb shell wm size` | Shows current screen resolution. |
| `adb shell wm density` | Shows current screen density. |
| `adb shell wm size 1080x1920` | Sets custom screen resolution. |
| `adb shell wm density 320` | Sets custom display density. |

---

## 🔋 Battery & Power Management

| Command | Description |
|----------|--------------|
| `adb shell cmd battery unplug` | Simulates device unplugged. |
| `adb shell cmd battery set level <n>` | Sets fake battery level. |
| `adb shell cmd battery reset` | Resets battery simulation. |
| `adb shell svc power stayon true` | Keeps screen awake while charging. |

---

## 🧩 Advanced / Root / DevOps

| Command | Description |
|----------|--------------|
| `adb root` | Restarts adbd with root permissions (if supported). |
| `adb remount` | Remounts system partition as writable. |
| `adb shell su` | Switches to superuser mode (rooted only). |
| `adb shell cmd package install-existing <package>` | Re-enables a system app. |
| `adb shell cmd package list features` | Lists available hardware features. |
| `adb shell cmd package list permissions` | Lists all permissions. |
| `adb shell cmd package resolve-activity <intent>` | Resolves an intent to an activity. |
| `adb shell cmd package dump <package>` | Dumps detailed package info. |
| `adb shell cmd package snapshot` | Takes a snapshot of package state. |
| `adb shell cmd vibrator vibrate 300` | Vibrates the device for 300ms. |
| `adb emu geo fix <long> <lat>` | Sets fake GPS location (emulator only). |
| `adb emu kill` | Shuts down the emulator. |
| `adb shell reboot edl` | Reboots to Qualcomm EDL mode (for flashing). |

---

## 🧾 Credits & Reference

💡 **Created by:** [Krishna Gadagool](https://github.com/krishnagadagool)  
📘 **GitHub Repo:** [ADB Commands Cheatsheet (2025 Edition)](https://github.com/yourusername/adb-cheatsheet)  
🗓️ **Last Updated:** November 2025
