# Lesson 2: Files, Folders & The Cloud
## Managing Data Locally and Globally

*   **Estimated Time**: 60–90 minutes
*   **Ages**: 12 & 15
*   **Key Vocabulary**: File Extension, Directory, Absolute vs. Relative Path, Command Line (CLI), Data Center, Virtualization, The Cloud.
*   **Prerequisites**: A computer with Windows PowerShell or Command Prompt.

---

## 1. Parent Prep Guide (3-Minute Refresh)
*   **File Extensions**: The letters after the period (e.g., `.docx`, `.exe`, `.jpg`). They tell the Operating System (OS) what type of data is inside the file and what program should open it. A file extension is just a label; renaming `photo.jpg` to `photo.mp3` does not turn an image into a song.
*   **Paths**: How a computer finds a file.
    *   **Absolute Path**: The full address from the root drive (e.g., `C:\Users\Student\Documents\homework.pdf`).
    *   **Relative Path**: The address relative to where you currently are (e.g., if you are already in `C:\Users\Student\`, the relative path is `Documents\homework.pdf`).
*   **The Cloud**: Simply "someone else's computer" that you access over the internet.
*   **Data Centers & Virtualization**: Data centers are massive warehouses full of physical servers. Instead of assigning one physical computer to one user, software "virtualizes" them, splitting one physical server into dozens of "Virtual Machines" (VMs) that act as independent computers. This saves massive amounts of space and power.

---

## 2. Teaching Script & Discussion Flow

### The Filing Cabinet vs. The Warehouse Analogy
*Explain how files work locally vs. in the cloud:*

*   **You (the Parent)**: "When you store a file on your computer, it’s like putting a sheet of paper inside a folder, inside a drawer, in a metal filing cabinet in your room. You have to walk to the cabinet, open the correct drawer, and find the folder. If you want to describe where it is, you can say: 'Cabinet -> Drawer 2 -> Homework Folder -> Math.docx'. That is a **file path**."
*   **The Parent**: "But what happens if you store it in 'the Cloud' (like iCloud, Google Drive, or OneDrive)? It's like taking your paper, mailing it to a giant, secure warehouse across the country, where a robotic arm puts it in a filing cabinet with millions of other papers. When you click 'Open', the robotic arm scans the page and beams it to your screen over the internet."
*   **You**: "Why do we do this? What are the benefits of the warehouse over your bedroom cabinet?"
    *   **Teens**: "You can access it from any room, or from a phone, or if your house burns down, your papers are safe."
    *   **You**: "Exactly. But what are the downsides?"
    *   **Teens**: "You need internet to get it. And you have to trust the warehouse owners not to look at your papers."

### Socratic Discussion Questions
1.  *“What happens if I change the name of `song.mp3` to `song.docx`? Will MS Word play the music?”*
    *   **Answer**: No. Word will try to read the audio data (binary bits) as text characters. It will open the file and display pages of random symbols, gibberish, and boxes because it doesn't know how to decode audio.
2.  *“If Google Drive holds files for a billion people, do they have a billion separate physical computers running in their data centers?”*
    *   **Answer**: No, they use **Virtualization**. A single giant server computer can act like 100 small virtual computers. This is much cheaper and more efficient.

---

## 3. Hands-On Lab

### Part 1: The CLI Messy Folder Rescue (Local)
Instead of using the mouse, the teens will learn how to navigate and organize a computer using the **Command Line Interface (CLI)**.

#### Step A: Run the Setup Script
To create a simulated messy folder, open **PowerShell** on your computer and paste the following command, then press Enter:
```powershell
powershell -Command "New-Item -ItemType Directory -Force -Path C:\Apps\SummerAcademy\curriculum\comp101\messy_folder | Out-Null; $files = @('homework_math.docx', 'cat_funny.jpg', 'steam_installer.exe', 'budget_2026.xlsx', 'dog_meme.png', 'resume.pdf', 'python_script.py', 'spotify_setup.exe'); foreach ($f in $files) { New-Item -ItemType File -Force -Path C:\Apps\SummerAcademy\curriculum\comp101\messy_folder\$f | Out-Null }; Write-Host 'Setup Complete! folder created at C:\Apps\SummerAcademy\curriculum\comp101\messy_folder' -ForegroundColor Green"
```

#### Step B: The Command Line Mission
Now tell the kids to open a fresh PowerShell window. They must organize the folder `C:\Apps\SummerAcademy\curriculum\comp101\messy_folder` using only the command line.

**Cheat Sheet of commands they will use:**
*   `cd <path>`: Change directory (move to a folder).
*   `ls` or `dir`: List files in the current folder.
*   `mkdir <name>`: Make a new directory.
*   `mv <file> <destination>`: Move a file.

**Their Tasks:**
1.  **Navigate** to the messy folder:
    `cd C:\Apps\SummerAcademy\curriculum\comp101\messy_folder`
2.  **Inspect** the files:
    `ls`
3.  **Create** three new folders: `Documents`, `Images`, and `Installers`:
    `mkdir Documents`, `mkdir Images`, `mkdir Installers`
4.  **Move** the files to their respective folders:
    *   Move `.docx`, `.xlsx`, and `.pdf` to `Documents`:
        `mv homework_math.docx Documents; mv budget_2026.xlsx Documents; mv resume.pdf Documents`
    *   Move `.jpg` and `.png` to `Images`:
        `mv cat_funny.jpg Images; mv dog_meme.png Images`
    *   Move `.exe` installers to `Installers`:
        `mv steam_installer.exe Installers; mv spotify_setup.exe Installers`
    *   (Optionally, move the `.py` script into `Documents` or leave it).
5.  Run `ls` inside the folders to confirm they are clean.

---

### Part 2: Cloud Datacenter Fermi Math (Global)
*Now, let's look at the cloud. A large data center houses about 50,000 servers. Let's do some Fermi estimation together.*

1.  **Assume 1 server uses about 500 Watts of electricity** (running CPU, RAM, and cooling fans).
2.  **Question**: How many Kilowatts (kW) does a 50,000-server data center consume at any given second?
    *   *Calculation*: $50,000 \text{ servers} \times 500 \text{ Watts} = 25,000,000 \text{ Watts} = 25,000 \text{ kW} = 25 \text{ Megawatts (MW)}$.
3.  **Comparison**: If an average family home uses about $1.2 \text{ kW}$ of power, how many homes' worth of electricity does this single data center consume?
    *   *Calculation*: $25,000 \text{ kW} \div 1.2 \text{ kW} \approx 20,833 \text{ homes}$.
    *   *Teaching point*: That's a medium-sized town's worth of power just to keep our cloud photos, emails, and cat videos accessible!

---

## 4. Teens' Reflection & Log
*Have the kids answer these questions in their notebook or text doc:*

1.  **What is the command to make a new directory in PowerShell?**
2.  **If you are in `C:\Apps\SummerAcademy\`, what is the *relative path* to the messy folder?**
3.  **Why do you think data centers require so much cooling (air conditioning)? What happens to electrical energy when a processor does math?**
4.  **How do you think cloud companies make sure your files aren't lost if a data center has a power outage or a fire?**

---

## 5. End-of-Lesson Quiz

1.  **If you rename `report.txt` to `report.exe`, will the computer run it as a program?**
    *   *Answer*: No, it will fail to execute because the internal bytes are text data, not binary computer instructions. The extension is just a label.
2.  **What is the difference between an Absolute Path and a Relative Path?**
    *   *Answer*: An absolute path starts from the very root of the computer (like `C:\`), whereas a relative path starts from where you are currently working.
3.  **What does "Virtualization" mean in cloud computing?**
    *   *Answer*: Running multiple virtual computer systems (virtual machines) on a single physical server hardware, sharing its resources.
4.  **True or False: The Cloud is a magical wireless space in the sky where data floats.**
    *   *Answer*: False. The cloud is just a physical network of giant warehouses (data centers) containing real computers, hard drives, cables, and power plants.
