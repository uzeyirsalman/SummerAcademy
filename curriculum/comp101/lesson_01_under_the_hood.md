# Lesson 1: Under the Hood
## Hardware vs. Software: How Computers Actually Think

*   **Estimated Time**: 60–90 minutes
*   **Ages**: 12 & 15 (Adaptable for both)
*   **Key Vocabulary**: CPU, RAM, SSD/HDD, Motherboard, GPU, Operating System.
*   **Prerequisites**: A computer/tablet with internet access to open [PCPartPicker](https://pcpartpicker.com/).

---

## 1. Parent Prep Guide (3-Minute Refresh)
Before you start, here is a quick summary of what we are teaching so you can speak with confidence:
*   **CPU (Central Processing Unit)**: The "brain" of the computer. It executes instructions (arithmetic, logic). Speed is measured in Gigahertz (GHz)—billions of cycles per second. Cores allow it to do multiple tasks at once.
*   **RAM (Random Access Memory)**: Fast, temporary workspace. When you open a program, it's loaded from storage into RAM so the CPU can access it instantly. RAM is *volatile* (wiped when the power turns off).
*   **Storage (SSD/HDD)**: Long-term memory. Where your files, games, and OS live. SSDs (Solid State Drives) use flash memory and are much faster than old HDDs (Hard Disk Drives) which use spinning physical platters. Storage is *non-volatile* (retains data when powered off).
*   **Motherboard**: The main circuit board that connects all components and allows them to talk to each other.
*   **GPU (Graphics Processing Unit)**: A specialized processor designed to handle images, videos, and 3D graphics (essential for gaming, video editing, and AI workloads).

---

## 2. Teaching Script & Discussion Flow

### The Kitchen Analogy
*Start the lesson by asking the kids to imagine they are running a busy restaurant kitchen. Use this story to explain how a computer runs:*

*   **You (the Parent)**: "Imagine you want to bake a cake. You need a chef, a kitchen counter, a pantry, and a floor to walk on. Let’s map these to computer parts."
*   **The Chef = The CPU**: "The chef does all the chopping, mixing, and cooking. A fast chef (high GHz) cooks quickly. A chef with 8 arms (8 cores) can chop carrots, boil pasta, and whip cream all at the same time."
*   **The Kitchen Counter = RAM**: "When the chef is making a salad, they put the tomatoes, lettuce, and bowl on the counter. Why? Because it's right in front of them and fast to grab. But what happens if the counter is tiny? The chef has to keep running to the pantry to grab one ingredient at a time, slowing everything down. What happens at the end of the night when the kitchen closes? The counter is wiped completely clean. That's RAM."
*   **The Pantry = Storage (SSD/HDD)**: "This is where you store 50 bags of flour, canned goods, and cookbooks. It's huge, and the food stays there even when the kitchen is closed overnight. But it takes time to walk to the pantry, open the door, and carry things to the counter. An old HDD is like a messy pantry at the end of a long hallway. An SSD is like a modern cabinet right next to the counter."
*   **The Motherboard = The Kitchen Floor & Wiring**: "It's what connects the pantry to the counter and lets the chef walk between them. It routes power and data."
*   **The GPU = The Assistant Pastry Chef**: "Making intricate frosting designs on a cake takes a lot of time. If the head chef does it, other meals stop. So, they hire a specialized pastry chef who only does visual designs. That's the GPU."

### Socratic Discussion Questions
Ask your teens these questions to get them thinking:
1.  *“If we have a super-fast Chef (CPU) but a tiny kitchen counter (RAM), what will happen when we try to cook three complex meals (games/apps) at once?”*
    *   **Answer**: The chef will run out of space and have to constantly swap ingredients back and forth to the pantry (Storage), making the kitchen run very slowly. This is called "swapping" or bottlenecking.
2.  *“Why doesn't a computer just use RAM for everything and get rid of SSDs?”*
    *   **Answer**: RAM is expensive, much smaller in capacity, and most importantly, it loses all its data when the power is turned off. If we didn't have storage, our files and games would disappear every time we shut down.

---

## 3. Hands-On Lab: The $1,000 Virtual PC Build

### The Mission
The kids are running a custom PC building shop. They have received a request from three different clients, but they only have a budget of **$1,000 USD** for the parts (excluding monitor, keyboard, mouse).

Have them pick **one** client below and work together (or split up and compete!) to spec out a compatible PC on [PCPartPicker](https://pcpartpicker.com/).

#### Client Profiles (Choose One):
*   **Client A (The Gamer - Ethan, 16)**: "I want to play modern 3D games at high frame rates. I don't care about video editing, I just want smooth gameplay."
    *   *Teaching Tip*: They should spend a major portion of their budget (30-40%) on the **GPU**, and get a decent mid-range CPU and 16GB of RAM.
*   **Client B (The YouTuber/Content Creator - Maya, 18)**: "I edit 4K videos, do 3D modeling, and stream. I need to render videos fast and hold lots of raw video footage."
    *   *Teaching Tip*: They need to prioritize a strong **multi-core CPU**, more **RAM** (32GB is ideal), and a large, fast **SSD** (2TB+). They can compromise on a mid-range GPU.
*   **Client C (The Coding & School Student - Sarah, 14)**: "I write code, run virtual machines, and do homework. I want the computer to boot instantly, open 50 browser tabs without lagging, and be super quiet."
    *   *Teaching Tip*: They don't need a dedicated GPU (integrated graphics on the CPU is fine!). They should spend money on a high-end **CPU**, **32GB of RAM**, a premium **SSD**, and a very quiet CPU cooler and case.

### Rules of the Build:
1.  Must not exceed **$1,000**.
2.  Must include: CPU, Motherboard, RAM, Storage (SSD), Case, Power Supply (PSU), and GPU (if needed).
3.  PCPartPicker must show **"Compatibility: No issues or incompatibilities found"** in green at the top.

---

## 4. Teens' Reflection & Log
*Have the kids write down their build details and answer these questions:*

1.  **Which Client did you choose, and what was your final build cost?**
2.  **Which single component was the most expensive in your build, and why did you prioritize it for this client?**
3.  **How much RAM and storage did you choose, and what were the speeds/types?**
4.  **What was the most challenging part of matching components (e.g., matching the motherboard socket to the CPU, or finding a big enough power supply)?**

---

## 5. End-of-Lesson Quiz (Review Together)

1.  **If your computer starts running very slowly when you open a 20th tab in Chrome, which component is likely full?**
    *   *Answer*: RAM (the kitchen counter has run out of space).
2.  **What is the main physical difference between an HDD and an SSD?**
    *   *Answer*: An HDD has spinning magnetic disks and a moving read/write arm; an SSD has no moving parts and uses microchips (flash memory) to read and write data.
3.  **Why do motherboards have specific "sockets"?**
    *   *Answer*: Motherboards are built for specific CPU brands (Intel vs. AMD) and generations. A CPU physical socket must match the motherboard layout to connect the pins correctly.
4.  **What does "volatile" mean in reference to computer memory?**
    *   *Answer*: It means the memory requires electrical power to maintain its data. When power is lost, the data is erased (like RAM).
