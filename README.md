# Wi-Fi Toggle for Meta Quest
A simple yet powerful utility for Meta Quest headsets that allows you to toggle your Wi-Fi connection on or off globally using a physical button hotkey, without ever leaving your current VR application.

# Description

Once installed and enabled, it runs silently in the background, listening for a specific hardware button combination. When you press Volume Down followed immediately by Volume Up, the app will instantly turn your Wi-tFi on or off, providing a small confirmation message in your headset.

# Features
Global Hotkey: Toggle your Wi-Fi from anywhere in the Quest OS—whether you're on the home screen or inside any application.

Simple and Lightweight: The app uses a minimal background service that has virtually no impact on performance.

Easy to Use: No complex menus. Just set it up once and use the hotkey whenever you need it.

Confirmation Toasts: Get a quick visual confirmation ("Wi-Fi turned ON" / "Wi-Fi turned OFF") right in your view.

# How It Works
This application leverages Android's Accessibility Service framework. This special type of service is granted permission to listen for hardware key presses, which allows it to detect the Volume Down -> Volume Up hotkey combination globally. When the hotkey is detected, the app uses the Android WifiManager API to programmatically enable or disable the device's Wi-Fi adapter.

# Installation and Setup
To get the app working on your Meta Quest, you will need to build the APK from the source code and "sideload" it onto your device.

Prerequisites

Developer Mode on Quest: You must have a developer account and enable Developer Mode on your Meta Quest.

SideQuest: It is highly recommended to install SideQuest for easy sideloading.

Step 1: Build the APK from Source / or download relese apk | skip to sideloading
Clone the Repository: Download or clone this repository to your local machine.

Open in Android Studio: Open the project folder in Android Studio.

Build the APK: From the top menu bar, navigate to Build > Build Bundle(s) / APK(s) > Build APK(s).

Locate the APK: Once the build is complete, a notification will appear. Click the "locate" link to find the app-debug.apk file in the project's output folder (YourProject/app/build/outputs/apk/debug/).

Step 2: Sideload the Application
Connect Your Quest: Connect your Quest to your computer via a USB-C cable. Put on the headset and accept the "Allow USB debugging" prompt if it appears.

Open SideQuest: Launch SideQuest. A green dot in the top-left corner indicates a successful connection.

Install APK: In SideQuest, click the icon for "Install APK file from folder" (a box with a downward arrow). Navigate to and select the app-debug.apk file you built.

Step 3: Enable the Accessibility Service
This is the most important step. The service will not work until you manually enable it.

Find the App: In your Quest's app library, filter by "Unknown Sources" and launch WifiToggleQuest.

Open Settings: The app will inform you that the service is inactive. Click the "Open Accessibility Settings" button.

Activate the Service: You will be taken to the Quest's system settings. Find and select WifiToggleQuest (it may be under an "Installed apps" or "Downloaded apps" section).

Toggle it ON. You will see a system warning about the permissions you are granting. You must accept this for the hotkey to function.

# Usage
Once the service is active, you're all set!

To toggle your Wi-Fi, simply press the Volume Down button, then immediately press the Volume Up button.

A small confirmation message will appear at the bottom of your view.

The app's main screen will also show you whether the service is currently active or inactive.

# Disclaimer
This application uses an Accessibility Service to function. Android shows a standard warning upon activation because such services have the potential to read screen content and monitor actions. This app, however, is designed only to listen for hardware key events and does not read, store, or transmit any personal information or on-screen content. The source code is available for full transparency.
