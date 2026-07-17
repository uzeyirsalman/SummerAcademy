# Lesson 3: How the Internet Actually Works
## Packets, DNS, and the Global Network Pipeline

*   **Estimated Time**: 60–90 minutes
*   **Ages**: 12 & 15
*   **Key Vocabulary**: Packet, IP Address, DNS (Domain Name System), Router, Hop, Latency (Ping), Traceroute, Fiber Optics, Total Internal Reflection, Electromagnetic Waves, Signal Interference.
*   **Prerequisites**: A computer with internet access and Windows PowerShell.

---

## 1. Parent Prep Guide (3-Minute Refresh)
*   **Packets**: The internet doesn't send files in one piece. If you download a photo, it is sliced into thousands of tiny chunks called *packets* (usually around 1,500 bytes each). Each packet is stamped with a source and destination IP, and sent into the network. They might travel different paths and arrive out of order, but your computer reassembles them at the end.
*   **IP Address**: A unique numerical label assigned to each device connected to a computer network (e.g., `142.250.190.46`). It works like a physical mailing address.
*   **DNS (Domain Name System)**: The phonebook of the internet. Humans like names (e.g., `google.com`), but computers only understand numbers (IPs). When you type `google.com`, your computer asks a DNS server: *"What is the IP address for google.com?"* and the DNS server replies: *"It is 142.250.190.46"*.
*   **Routers & Hops**: Routers are the traffic police of the internet. They inspect incoming packets and forward them along the fastest path toward their destination. Each transition from one router to another is called a **hop**.
*   **Ping / Latency**: The time it takes for a packet to go from your computer to a server and back, measured in milliseconds (ms).
*   **Fiber Optics**: Transmitting data as pulses of light through thin strands of glass. Relies on *Total Internal Reflection* to keep light inside the glass core. Immune to electrical noise and can carry terabits of data over thousands of miles.
*   **Wireless Communication**: Transmitting data through the air using electromagnetic radio waves/microwaves (Wi-Fi, 5G, satellite). Highly mobile but susceptible to absorption (walls, rain) and congestion.

---

## 2. Teaching Script & Discussion Flow

### The Postcard Analogy
*Explain how internet routing works by comparing a file to sending a book via postcards:*

*   **You (the Parent)**: "Imagine you want to mail a 100-page notebook to your friend in Tokyo, but the post office has a rule: you can only mail single postcards. What do you do?"
*   **Teens**: "You tear out the 100 pages, put a page number on each, write your friend's address on each page, and drop all 100 postcards in the mailbox."
*   **You**: "Perfect. Do all 100 postcards travel in the exact same mail truck together?"
*   **Teens**: "Not necessarily. Some might go on a plane, some might go on a truck, some might get delayed."
*   **You**: "Exactly. The postcards are **packets**. The mailbox sorting machines are **routers**. The address on the cards is the **IP address**. When they arrive in Tokyo, your friend has to wait for all of them, arrange them by page number, and bind them back into the notebook. If page 45 is lost, what does your friend do?"
*   **Teens**: "They send a postcard back saying: 'Hey, I'm missing page 45, send it again!'"
*   **You**: "That is exactly how the internet works! It's called TCP/IP. It guarantees that if a packet gets lost, it gets resent."

### Socratic Discussion Questions
1.  *“What would happen if the DNS servers worldwide went offline, but the rest of the internet was working perfectly?”*
    *   **Answer**: You wouldn't be able to access websites by typing their names (e.g., `youtube.com` would show an error). However, if you knew YouTube's exact numerical IP address (like `142.250.190.46`), you could type that directly into your browser, and the website would load!
2.  *“When you connect to a website in London from your home, how do the packets cross the Atlantic Ocean? Satellites?”*
    *   **Answer**: Mostly no! Over 95% of international internet traffic travels through massive, fiber-optic **submarine cables** laid on the ocean floor. They are about as thick as a garden hose and carry light pulses across thousands of miles of ocean.
3.  *“During a heavy thunderstorm, your home Wi-Fi signal drops or slows down, but your fiber internet connection is still perfectly stable. Explain this based on the physical properties of how each transmits data.”*
    *   **Answer**: Wi-Fi uses radio waves traveling through the open air, which can be absorbed/scattered by water droplets (humidity/rain) and blocked by physical obstacles like walls. Fiber optic signals travel as light pulses inside physical glass strands buried underground, completely shielded from weather conditions and radio interference.

---

## 3. Hands-On Lab: Tracing the Packet Journey

Let’s use real network tools in PowerShell to map a packet's journey across the world.

### Step 1: Lookup the IP Address (DNS)
1.  Open **PowerShell**.
2.  Run the `nslookup` command to ask your DNS server for the IP address of Google Japan:
    ```powershell
    nslookup google.co.jp
    ```
3.  Write down the IP address returned under "Addresses" (e.g., `142.250.190.35`).

### Step 2: Measure the Speed (Ping)
1.  Let's test the response speed (latency) to Google Japan. Run:
    ```powershell
    ping google.co.jp
    ```
2.  Look at the `time=` value in milliseconds (ms).
    *   *Discussion*: How fast did it take to go to Japan and back? (Usually around 100–200ms). Remember, light in fiber cables takes about 60–70ms just to travel to Japan and back in a straight line!

### Step 3: Map the Hops (Traceroute)
Now, let's trace every single router (hop) your packet passes through. We will trace a path to the University of Tokyo (`www.u-tokyo.ac.jp`).
1.  In PowerShell, run:
    ```powershell
    tracert www.u-tokyo.ac.jp
    ```
    *(Note: This might take 1–2 minutes to complete. It will list up to 30 rows.)*
2.  Each row is a router.
    *   **Hops 1-3**: Usually your home router (e.g., `192.168.1.1`) and your local ISP (Internet Service Provider).
    *   **Middle Hops**: Regional routing hubs. Look at the names of the servers in the text! Often, they have airport codes in their names (e.g., `LHR` for London Heathrow, `JFK` for New York, `NRT` for Tokyo Narita) or ISP names like Telia, Level3, or NTT.
    *   **Final Hops**: The destination network in Tokyo.

### Step 4: Geolocation Lookup
1.  Pick one of the public IP addresses from the middle of your `tracert` output (avoid IPs starting with `10.`, `192.168.`, or `172.16.`, as these are private home/ISP network IPs).
2.  Open a web browser and go to [ipinfo.io](https://ipinfo.io/).
3.  Type the IP address into the search bar.
4.  Where is this router physically located? (It’s amazing to see your packet jumping from your city to New York, then over the ocean, and finally to Tokyo).

---

## 4. Teens' Reflection & Log
*Have the kids record their network findings:*

1.  **What was the IP address of `google.co.jp`?**
2.  **What was your average ping (latency) to `google.co.jp` in milliseconds? How many times could a packet make that trip in a single second?**
3.  **How many "hops" (routers) did it take for your packet to reach the University of Tokyo (`www.u-tokyo.ac.jp`)?**
4.  **Look at your `tracert` list. Did any of the hop names give away their location (e.g., containing letters like `ny`, `lon`, `tok`, or ISP names)? Write down 2-3 interesting hop names.**

---

## 5. End-of-Lesson Quiz

1.  **Why does the internet break large files into packets instead of sending them as one big file?**
    *   *Answer*: If one big file fails at 99%, you have to resend the whole thing. Packets allow multiple devices to share the same cables at the same time, and if one packet is lost, only that tiny piece needs to be resent.
2.  **What system translates `wikipedia.org` to an IP address like `208.80.154.224`?**
    *   *Answer*: The Domain Name System (DNS).
3.  **If your ping to a gaming server is 250ms, is that better or worse than 20ms? Why?**
    *   *Answer*: Worse. Higher ping means higher latency (delay), meaning it takes a quarter of a second for your actions to reach the server. Lower ping (20ms) is much faster and smoother.
4.  **What is a "hop" in computer networking?**
    *   *Answer*: The movement of a data packet from one router or network device to the next along its path.
5.  **Why is a wired fiber optic connection less prone to interference than a wireless 5G/cellular connection?**
    *   *Answer*: Fiber optic cables keep light signals sealed inside physical glass strands, completely shielded from electromagnetic noise and physical blockers. Wireless signals must travel through open space, where they are easily blocked by walls, weather (like rain fade), and other competing radio signals.
