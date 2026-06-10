# Lesson 8: Mobile & Platforms
## Under the Screen: Permissions, Privacy, and App Ecosystems

*   **Estimated Time**: 60 minutes
*   **Ages**: 12 & 15
*   **Key Vocabulary**: Native App, Web App, Sandbox, API (Application Programming Interface), Advertising ID (IDFA), Background App Refresh.
*   **Prerequisites**: The kids' own smartphones (iOS or Android).

---

## 1. Parent Prep Guide (3-Minute Refresh)
*   **Native Apps vs. Web Apps**:
    *   **Native Apps**: Built specifically for a phone's OS (Swift for iOS, Kotlin for Android). They are downloaded from app stores, run directly on the hardware, and have deep access to system features (camera, contacts, Bluetooth, background services).
    *   **Web Apps**: Run inside a browser sandbox (like Safari or Chrome). They don't require downloading and have much tighter security restrictions. They can't access hardware features easily unless you explicitly grant them permission in the browser.
*   **App Permissions**: To protect users, mobile OS designs run apps in a **sandbox** (an isolated environment). An app cannot access your photos or location unless it asks the OS, which then asks you.
*   **The Business of Tracking**: Many free apps make money by collecting your data. They use your **Advertising ID** (a unique code on your phone) to track your behavior across different apps, building a profile of your age, interests, and location to sell targeted ads.
*   **iOS vs. Android Security Philosophy**: iOS is a "walled garden" (stricter control, Apple approves every app and blocks sideloading by default). Android is open-source (more customization, allows alternative app stores, but higher risk if users download apps from untrusted sites).

---

## 2. Teaching Script & Discussion Flow

### The Hotel Guest Analogy
*Explain app permissions using a hotel:*

*   **You (the Parent)**: "Imagine your phone is a highly secure hotel. You are the owner. An app is a guest checking in. In the old days of computers, when you installed an app, it got a master key card to every room in the hotel. It could go into your bedroom (photos), read your diary (contacts), and look out your window (location)."
*   **You**: "Today, mobile phones use a **sandbox**. When an app checks in, the hotel doesn't give it any key card. The app is locked in its own room. If the app wants to take a photo, it has to call the front desk (the Operating System) and say: 'Can I have temporary access to the camera room?' The OS then calls you in your room and asks: 'Do you want to let this guest use the camera?'"
*   **You**: "What happens if a simple calculator app checks in and asks to use the microphone and your location? What should you do?"
    *   **Teens**: "Say no! A calculator doesn't need to hear you or know where you are to do math."
    *   **You**: "Exactly. If you say no, the OS blocks the request, but the calculator still works. Today we are going to audit our own phones and see what room keys our apps have."

### Socratic Discussion Questions
1.  *“If an app is free, and it doesn't show any ads, how does the company pay its employees and servers?”*
    *   **Answer**: *"If you aren't paying for the product, you are the product."* They are likely collecting your data (location history, app usage, search queries) and selling it to data brokers, or using it to train AI models, or planning to add paid features later.
2.  *“Why does Instagram want to track your location even when you aren't posting a photo?”*
    *   **Answer**: To serve highly targeted ads. If they see you walk into a Nike store, they can instantly show you a discount code for sneakers on your feed.

---

## 3. Hands-On Lab: The Smartphone Privacy Audit

Have the kids get their phones. They will act as security auditors and inspect their own devices. Follow the steps for iOS or Android.

### Step 1: The Location Audit
Find out which apps are watching where you go.
*   **iOS**: Go to `Settings > Privacy & Security > Location Services`.
*   **Android**: Go to `Settings > Location > App Permissions`.
*   **Task**: 
    1.  List any apps that have **"Always Allow"** location access. Ask: *Does this app really need to know where I am when it is closed?* (Change to "While Using" or "Never").
    2.  Find an app that doesn't need location at all (e.g., a music player, game, or shopping app) and turn it off.
    3.  Check if **"Precise Location"** is enabled. (For weather apps, general city location is fine; precise location within 10 feet is only needed for maps/Uber).

---

### Step 2: The Camera & Microphone Audit
*   **iOS**: Go to `Settings > Privacy & Security > Camera` (and `Microphone`).
*   **Android**: Go to `Settings > Privacy > Permission Manager > Camera` (and `Microphone`).
*   **Task**:
    1.  Inspect the list of apps that have access to your camera and microphone.
    2.  Are there any apps you haven't used in months that still have access? Turn them off.

---

### Step 3: Stop Cross-App Tracking
Turn off the tracking ID that lets apps spy on your activity in other apps.
*   **iOS**: Go to `Settings > Privacy & Security > Tracking`. Toggle off **"Allow Apps to Request to Track"**.
*   **Android**: Go to `Settings > Privacy > Ads`. Tap **"Delete Advertising ID"** or **"Reset Advertising ID"**.

---

### Step 4: Background Refresh Clean-Up
Many apps run in the background, wasting battery and sending telemetry data to their servers.
*   **iOS**: Go to `Settings > General > Background App Refresh`.
*   **Android**: Go to `Settings > Apps > [Select App] > Mobile Data > Allow background data usage` (or battery background settings).
*   **Task**: Turn off background refresh for apps that don't need to update instantly (e.g., Spotify, games, retail apps). Leave it on only for messaging apps (WhatsApp, Discord) where you need instant notifications.

---

## 4. Teens' Reflection & Log
*Have the kids record their audit results:*

1.  **How many apps had "Always Allow" access to your location? What did you change them to?**
2.  **Did you find any app with camera or microphone permissions that surprised you? Which one?**
3.  **How many apps did you disable "Background App Refresh" for? How do you think this will affect your phone's battery life?**
4.  **Based on the iOS vs. Android comparison, which operating system do you prefer and why?**

---

## 5. End-of-Lesson Quiz

1.  **What is the difference between a Native App and a Web App?**
    *   *Answer*: A native app is built specifically for the phone's OS, downloaded from an app store, and runs directly on the device with deep hardware access. A web app runs inside the web browser's sandbox with limited system access.
2.  **What does a mobile OS "sandbox" do?**
    *   *Answer*: It isolates apps from each other and from the core operating system, preventing them from accessing your private files, camera, or sensors without your explicit permission.
3.  **What is an Advertising ID (like Apple's IDFA)?**
    *   *Answer*: A unique, resettable identifier assigned to a mobile device that allows ad networks to track user activity across different apps to build a profile for targeted advertising.
4.  **Why is SMS MFA less secure than using an Authenticator app?**
    *   *Answer*: SMS messages are unencrypted and can be intercepted. More importantly, hackers can perform a "SIM swap" attack, tricking the phone carrier into routing your phone number to their own SIM card to steal your codes.
