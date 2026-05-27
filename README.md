# 💎 sqAFK — Dynamic Vanilla AFK Zone Engine

An advanced, ultra-lightweight, and lag-free **AFK Zone** reward engine meticulously designed for **1.21.x** Minecraft servers. Engineered with a strict zero-dependency matrix, it delivers a high-fidelity visual experience optimized for clean performance.

---

## 🎯 What is sqAFK? (Project Objective)
Deploying heavy region management systems or external addon-reliant tools often introduces massive ticking overhead and instability to Minecraft servers. 

**sqAFK** completely bypasses this limitation. Utilizing **100% Pure Vanilla Skript**, it handles proximity boundary math and distinct vertical plane checking natively. It allows network owners to deploy fully customizable reward regions that automatically adjust their bounding box sizes in real-time, providing a clean plugin environment with an elegant visual progression bar.

---

## ✨ Premium Features Overview

*   **⚡ Zero-Addon Dependency:** Runs flawlessly out of the box with zero external addon requirements (No SkQuery, Skellett, or TuSKe needed).
*   **📊 Premium Visual Progression:** Employs an ultra-fast 1-second refresh cycle rendering dynamic real-time progress percentages (`0%` to `100%`) directly inside the player's Action Bar.
*   **📐 Seamless Dynamic Scaling:** Boundary metrics are linked instantly to the configuration matrix. Modifying the radius or height updates the 3D boundary grid on-the-fly without needing to break or re-register coordinates.
*   **🛡️ Fail-Safe Safeguards:** Functions like a full-scale premium plugin. It blocks multi-zone overlaps, intercepts missing database pointers, and prints native troubleshooting feedback during administrative execution.
*   **🎒 Multi-Tier Reward Infrastructure:** Supports autonomous economy delivery (merges smoothly into Vault/EssentialsX) or maps up to 10 independent custom console commands with dynamic string placeholder replacement.
*   **🚨 Leaving Zone Alert:** Triggers an immediate, responsive red-colored notification overlay to users the exact split-second they step out of the designated AFK bounds.

---

## 🕹️ Command Reference & Interface


| Command | Permission | Description |
| :--- | :--- | :--- |
| `/sqafk set` | `sqafk.admin` | Instantiates the absolute 3D center-point of the AFK Zone at your exact feet coordinates. |
| `/sqafk remove` | `sqafk.admin` | Safely purges and wipes the designated AFK zone data from the internal script database. |
| `/sqafk reload` | `sqafk.admin` | Executes a clean, hard compilation reload of the internal script files. |

---

## 🛠️ Step-by-Step Administrative Tutorial

### 1️⃣ Initial System Deployment
* Make sure you have the base **Skript** plugin installed on your 1.21.x server.
* Download the `sqafk.sk` script file from this repository.
* Place the file into your server directory path: `/plugins/Skript/scripts/`.

### 2️⃣ Setting Up the Reward Bounding Box
* Walk into your server's spawn or AFK arena and stand on the precise block you wish to make the **center core**.
* Run the command `/sqafk set`. The system will automatically fetch your coordinate variables and build the 3D zone structure around you.

### 3️⃣ Editing Parameters & Updating Shapes
* Open up the script file using any text editor and scroll to the `options:` header.
* Adjust `AFK-Time` (in seconds), `Zone-Radius` (horizontal stretch), or `Zone-Height` (vertical blocks check).
* Adjust `Money-Reward` (or set it to `-1` to turn it off completely).
* Populate the `Cmd-1` to `Cmd-10` slots with your custom crate keys, items, or broadcast commands (Set any slot to `"none"` to leave it inactive). Use `<player>` as your placeholder text.
* Save the file and run `/sqafk reload` inside the game. The parameters change instantly without breaking the existing area setup!

---

## 📋 Technical Configurations Layout

```skript
options:
    Prefix: &8[&bsqAFK&8] &r
    Permission: sqafk.admin
    Permission-Message: &cYou do not have permission to use this command.
    
    AFK-Time: 10          # The time loop cycle tracker
    Zone-Radius: 4        # Dynamic horizontal radius extension
    Zone-Height: 5        # Dynamic vertical block checking ceiling
    
    Money-Reward: 50      # Set to -1 to entirely disable economy routines
    
    Cmd-1: "give <player> diamond 1"
    Cmd-2: "xp add <player> 10 levels"
    Cmd-3: "none"
    # [... Up to Cmd-10 slots available]
```

---

## 🤝 Project Outreach & Links
*   **Discord Support Guild:** [Join our Official Discord Server](https://discord.gg/28pTmAYCwH)

### 📂 Check Out My Other Projects:
If you like this lightweight engine, check out my full standalone King of the Hill system here:  
👉 **[SQKoth — King of the Hill System]([https://github.com](https://github.com/amajd3078/SQKoth---King-of-the-hill)**
