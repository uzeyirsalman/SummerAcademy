# Lesson 10: Tech Troubleshooting
## The Diagnostic Loop: How to Fix Anything with Science

*   **Estimated Time**: 60–90 minutes
*   **Ages**: 12 & 15
*   **Key Vocabulary**: Diagnostic Loop, Isolation of Variables, Error Code, IPConfig, Device Manager, Extension Manager.
*   **Prerequisites**: A computer where the parent can safely misconfigure a few basic settings (see Setup guide below).

---

## 1. Parent Prep Guide (3-Minute Refresh)
*   **Troubleshooting is the Scientific Method**: Most people debug by clicking random buttons or panicking. Good troubleshooting means forming a hypothesis, isolating one variable at a time, testing it, and documenting the result.
*   **The Diagnostic Loop**:
    1.  **Define the Symptom**: Exactly what is failing? (e.g., *"Browser says 'DNS_PROBE_FINISHED_NO_INTERNET'"*).
    2.  **Isolate the Scope**: Is it one website, or all websites? One browser, or all browsers? One computer, or every device in the house?
    3.  **Formulate a Hypothesis**: *"If other devices can connect, it’s not the router; it must be this computer's network card or settings."*
    4.  **Test One Change**: Toggle Wi-Fi off and on. Did it fix it? If not, change the DNS. Did that fix it? (Never change three things at once, or you won't know which one worked or if you made it worse).
    5.  **Reflect/Document**: Learn why it broke so you can fix it instantly next time.

---

## 2. Teaching Script & Discussion Flow

### The Light Bulb Analogy
*Explain troubleshooting using a dark room:*

*   **You (the Parent)**: "Imagine you walk into your bedroom, flip the light switch, and nothing happens. The room stays dark. What is the very first thing you do?"
*   **Teens**: "Check if the bulb is burned out, or check if the power is out in the whole house."
*   **You**: "Exactly. If you run to the basement and flip the main fuse box switch without checking if other lights work, is that good troubleshooting?"
*   **Teens**: "No, because if it was just the bulb, you wasted time and turned off power for the whole house."
*   **You**: "Right. You naturally **isolated the variables**. 
    *   If the hallway light is ON, the power to the house is working.
    *   If you put the bedroom bulb into a working desk lamp and it lights up, the bulb is working.
    *   Therefore, the problem must be the bedroom switch or the wiring in the wall."
*   **You**: "Computer systems are exactly the same. When a game won't start or internet drops, we don't throw the computer out the window. We trace the path, test each joint, and isolate the broken piece."

### Socratic Discussion Questions
1.  *“If your internet drops and you call your ISP, and they say: 'Please restart your router,' why is that actually good advice instead of just a lazy answer?”*
    *   **Answer**: Routers are small computers with their own CPU, RAM, and Operating System. Over time, they can run out of memory or experience software crashes (loops) just like your PC. Rebooting clears the RAM and restarts all network services, resolving 90% of temporary routing issues.
2.  *“You get an error code: `0x80070005 - Access Denied` when trying to install a program. How do you use Google or AI to help you solve this?”*
    *   **Answer**: Don't just search: *"my computer won't install stuff."* That is too broad. Search the exact error code: *"0x80070005 Access Denied windows install"* and look for forums (like Reddit or Microsoft Support) where others solved the exact same code. The code is a specific fingerprint.

---

## 3. Hands-On Lab: The "Fix My Computer" Escape Room

*This is the final exam! Before the lesson, the Parent will deliberately "break" 2 or 3 settings on the computer. The kids must work together to diagnose and fix them using only diagnostic tools.*

### Parent Setup Guide (How to "Break" the Computer)
*Choose 2 or 3 of these to set up while the kids are out of the room:*

#### Glitch 1: The Disabled Wi-Fi Adapter (Easy)
*   **How to break it**: On Windows, right-click the Start button, open **Device Manager**, expand **Network adapters**, right-click your Wi-Fi card (e.g., Intel Wi-Fi 6), and select **Disable device**.
*   **The Symptom**: The Wi-Fi icon completely disappears from the taskbar, or says "No network connections available."
*   **How the kids should solve it**: Open Device Manager, locate the adapter showing a down-arrow icon, right-click, and select **Enable device**.

#### Glitch 2: The Broken DNS Server (Medium)
*   **How to break it**: 
    1.  Go to `Settings > Network & internet > Wi-Fi > Hardware properties`.
    2.  Next to "DNS server assignment", click **Edit**. Change it from Automatic (DHCP) to **Manual**.
    3.  Toggle IPv4 ON. Set Preferred DNS to a fake IP: `1.1.1.10` (which does not exist). Click Save.
*   **The Symptom**: The computer says it is connected to Wi-Fi, but opening any website (like `google.com`) returns a DNS error (`DNS_PROBE_FINISHED_NXDOMAIN`).
*   **How the kids should solve it**:
    1.  Open PowerShell and run `ping 8.8.8.8` (Google's public IP). It will succeed! This proves they have internet access, but name resolution is broken.
    2.  Run `nslookup google.com`. It will timeout or error.
    3.  Go into Network settings and change the DNS back to "Automatic" or to a valid public DNS (like `1.1.1.1` or `8.8.8.8`).

#### Glitch 3: The Rogue Chrome Extension (Medium)
*   **How to break it**: Open their web browser. Install a free joke extension from the Web Store (e.g., an extension that turns all webpage fonts into Comic Sans, or flips images upside down). Hide the extension icon from the toolbar.
*   **The Symptom**: Websites load, but they look bizarre or have comic fonts.
*   **How the kids should solve it**: Open the browser menu, go to **Extensions > Manage Extensions**, locate the rogue extension, and turn it off or remove it.

---

### The Kids' Diagnostic Worksheet
*As they work, they must write down their diagnostic steps for each glitch:*

1.  **Glitch 1**:
    *   *Symptom observed*:
    *   *Hypothesis tested*:
    *   *The Fix*:
2.  **Glitch 2**:
    *   *Symptom observed*:
    *   *Hypothesis tested*:
    *   *The Fix*:
3.  **Glitch 3**:
    *   *Symptom observed*:
    *   *Hypothesis tested*:
    *   *The Fix*:

---

## 4. Teens' Reflection & Log
*Have the kids summarize their final exam:*

1.  **Which glitch was the hardest to diagnose? Why?**
2.  **How did you prove that you had an internet connection in Glitch 2 even though you couldn't open `google.com`?**
3.  **What is the danger of changing multiple settings at the same time when trying to fix a problem?**
4.  **Write down your personal "Golden Rule of Troubleshooting" that you will use in the future when a device breaks.**

---

## 5. End-of-Course Wrap-Up! (Review Together)
*Congratulations! You have completed COMP101. Let's do a quick lightning round review of the main lessons:*
*   **Hardware**: CPU is the chef, RAM is the counter, SSD is the pantry.
*   **Files**: Absolute paths start from the drive root; relative paths start from your current folder.
*   **Internet**: Websites are translated by DNS into IP addresses, and data travels as packets.
*   **Work**: Modern collaboration syncing works in the cloud, resolving edit conflicts automatically.
*   **Design**: Slide decks are visual billboards; briefs are detailed documents.
*   **Spreadsheets**: Use cell formulas to automate calculations, and lock reference cells with `$`.
*   **Security**: Long passphrases beat short complex passwords. MFA keeps hackers out.
*   **Mobile**: Apps run in sandbox rooms and need permissions to access your camera/location.
*   **AI**: LLMs are advanced autocomplete engines that predict the next token—verify their facts!
*   **Troubleshooting**: Isolate variables, change one thing at a time, and look up error codes.
