# Lesson 7: Cybersecurity & Digital Hygiene
## Securing Your Digital Life: Passwords, Phishing, and Privacy

*   **Estimated Time**: 60 minutes
*   **Ages**: 12 & 15
*   **Key Vocabulary**: Entropy, Brute-Force Attack, MFA (Multi-Factor Authentication), Phishing, End-to-End Encryption (E2EE), Social Engineering.
*   **Prerequisites**: Pen and paper (or a blank text document) to conduct the mock audit.

---

## 1. Parent Prep Guide (3-Minute Refresh)
*   **Password Entropy (Strength)**: Entropy is the measure of randomness or unpredictability. Many websites force you to use complex characters (e.g., `P@$$w0rd!`), but these are actually easy for cracking software to guess because humans follow predictable patterns (replacing `a` with `@`, putting `!` at the end). **Length is much more powerful than complexity.** A passphrase of four random words (e.g., `correct-horse-battery-staple`) has massive entropy and takes trillions of years to crack.
*   **MFA (Multi-Factor Authentication)**: Authentication relies on three factors:
    1.  *Something you know* (Password, PIN).
    2.  *Something you have* (Phone, security key).
    3.  *Something you are* (Fingerprint, Face ID).
    MFA requires at least two of these. SMS (text message) codes are okay, but vulnerable to "SIM Swapping" (hackers stealing your phone number). App-based authenticators (like Google Authenticator) are much safer.
*   **Phishing & Social Engineering**: Psychological manipulation. Attackers trick you into giving up secrets by creating artificial urgency (e.g., *"Your account is locked, click here now!"*).
*   **End-to-End Encryption (E2EE)**: Data is encrypted on the sender's device and decrypted only on the recipient's device. No middlemen (not even your internet provider or WhatsApp/Apple) can read the messages because they don't have the keys.

---

## 2. Teaching Script & Discussion Flow

### The Castle Door Analogy
*Explain passwords and MFA using a castle:*

*   **You (the Parent)**: "Imagine you have a castle containing your gold. You put a lock on the front door. The key is a secret word: `Dragon123`. A thief stands outside and starts shouting random words at the door. How long before they guess `Dragon123`?"
*   **Teens**: "Maybe a few minutes, it’s a really common guess."
*   **You**: "What if the secret key is: `purple-skateboard-banana-helicopter`? The thief has to guess four separate random words in the right order. That would take them millions of years."
*   **You**: "But what if the thief tricks you? They dress up as a castle guard, knock on your window, and say: 'King's orders! I need you to whisper the password through the keyhole to verify your identity.' If you give it to them, does the strength of the password matter?"
*   **Teens**: "No, because you just handed it to them. That's **phishing**."
*   **You**: "Exactly. To prevent this, we add a second lock. Even if the thief gets your key, they also need to scan your thumbprint, or turn a physical dial that only you carry in your pocket. That is **MFA**."

### Socratic Discussion Questions
1.  *“If a hacker steals the encrypted database of a website like Spotify, can they immediately read everyone's passwords?”*
    *   **Answer**: No. Good websites do not store passwords as plain text. They run them through a mathematical function called a **hash** (a one-way scramble). When you log in, Spotify hashes your input and checks if it matches the stored scramble. If hackers steal the database, they only get the scrambles (hashes) and must use massive computers to guess passwords to see which ones produce the matching scramble.
2.  *“Why is it dangerous to use the same password for your school account, your email, and your gaming accounts?”*
    *   **Answer**: If a minor gaming website gets hacked (credential leaks), hackers will take your email and that password and try them on Google, Netflix, Discord, and banks. This is called "Credential Stuffing." One weak link breaks your entire security chain.

---

## 3. Hands-On Lab: The "Hack My Account" Audit

Have the teens act as cybersecurity consultants. Below are three mock client profiles. They must review each client, identify the **security vulnerabilities**, explain **how a hacker would exploit them**, and provide a **remediation plan** (how to fix it).

### Client 1: Leo (Age 15 - Gamer)
> "I play a lot of competitive games. To make sure I never forget my password, I use `LeoGamer2011` for Steam, Discord, Epic Games, and my school email. I don't use 2-Factor Authentication because it takes too long to type the codes. Yesterday, I got a Discord DM from a bot saying: 'Congratulations, you won a free game! Click this link steam-gift-cards.com/free and log in to claim it.' I clicked it, but the site just loaded a blank page, so I closed it."

*   **Audit Deliverables**:
    1.  Identify at least 3 security vulnerabilities in Leo's profile.
    2.  What attack did Leo just fall victim to? What should he do immediately?
    3.  How can he make his logins faster without sacrificing security?

---

### Client 2: Sophia (Age 13 - Social Media Creator)
> "I use a password manager to generate random 16-character passwords for TikTok and Instagram, and I have SMS 2-Factor Authentication turned on. I love posting daily life vlogs. When I'm at our local coffee shop or park, I post photos with the location tag so my friends can see where I am. Sometimes I post selfies showing my school uniform or our front door in the background. My accounts are public because I want to get more followers."

*   **Audit Deliverables**:
    1.  Is Sophia's account *security* good?
    2.  What are the major *privacy* and physical safety issues with Sophia's behavior?
    3.  How can she keep sharing content with friends safely?

---

### Client 3: Mr. Davis (Age 45 - Dad's Friend)
> "I got a text message from 'NETFLIX-SUPPORT' saying my billing details were out of date and my subscription would be cancelled in 24 hours. The link was `netflix-billing-update.net`. I clicked it, and it looked exactly like Netflix. I typed in my email, password, and credit card details. After submitting, it redirected me to the real Netflix home page, so I thought everything was fine. But today, I saw a $200 charge on my credit card that I didn't make."

*   **Audit Deliverables**:
    1.  How did the hackers trick Mr. Davis (social engineering tactics)?
    2.  What clues in the text message and URL did Mr. Davis miss?
    3.  What are the 3 immediate steps Mr. Davis must take right now to recover?

---

## 4. Teens' Reflection & Log
*Have the kids write down their audit report:*

1.  **For Client 1 (Leo), what is the danger of reuse of `LeoGamer2011`?**
2.  **For Client 2 (Sophia), how could an online stranger figure out her daily schedule or home address?**
3.  **For Client 3 (Mr. Davis), what was the clue in the URL `netflix-billing-update.net` that proved it was fake?**
4.  **Audit yourself: Do you have any accounts that use the same password? Do you have 2FA enabled on your email? (Make it a goal to set up 2FA on your email today!).**

---

## 5. End-of-Lesson Quiz

1.  **Which password has more entropy (is harder to crack)? `Pa$$w0rd123!` or `apple-window-shoe-yellow`? Why?**
    *   *Answer*: `apple-window-shoe-yellow`. It is much longer (26 characters vs. 12). Cracking software has to guess exponential combinations for length, making long passphrases vastly harder to crack than short, complex ones.
2.  **Name the 3 factors of authentication.**
    *   *Answer*: Something you know (password), something you have (phone/key), and something you are (fingerprint/face).
3.  **Why do phishing emails often say "URGENT" or "Action Required in 24 Hours"?**
    *   *Answer*: To induce panic and fear. When people are in a hurry or afraid, they make quick, emotional decisions and forget to check security indicators (like the URL or sender address).
4.  **What does End-to-End Encryption protect against?**
    *   *Answer*: It prevents anyone intercepting the data in transit (ISPs, hackers on public Wi-Fi, or the messaging service itself) from reading the content, as only the sender and receiver hold the keys to unlock it.
