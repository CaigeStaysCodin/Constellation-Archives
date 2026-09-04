Soooooo...how about that other Description huh? (It was pretty bad...here's the new one that isn't rushed as much lol.)

# Constellation Archives

**Constellation Archives** is an advanced, automated load order sorter and conflict analysis engine built specifically for Starfield users on Windows. Instead of forcing a generic, crowd-sourced "master list" onto your game, this tool uses a private local database alongside live Nexus API queries to build a unique load order tailored directly to your installed mods.

---

## 🔑 Key Features & How It Works

* **Private Local Database Logging:** Stores a local database file (`mod_database.db`) on your machine to log performance and sorting outcomes for your specific mod setup. It learns over time as you add or remove mods—no tracking, no data collection, and no public master list uploads.
* **Smart Starfield Recognition:** Integrates deeply with Starfield asset, script, and plugin behavior. It queries Nexus Mods via APIs using unique package numbers to accurately identify your specific mods.
* **Safe MO2 Integration:** Directly updates MO2's configuration text files to organize your right-panel load order without modifying, moving, or risking damage to the physical mod files on your drive.
* **Optional LOOT Hooking:** While this isn't a LOOT clone, the script allows you to optionally hook LOOT directly into its core framework if you already have it installed.
* **Tailored Setup:** Avoids "one-size-fits-all" templates by creating an auto-sorted load order specifically tuned to your exact mix of installed mods.

---

## ⚡ What Makes It Different?

Unlike static backup monitors or traditional "blunt force" sorters that often overwrite your profile configuration and scramble custom drag-and-drop file priorities on the left panel, this tool balances right-panel category intelligence with left-panel layout preservation.

> **The Advantage:** By combining category-based auto-sorting, deep loose-file conflict checks, and layout protection into a single portable PowerShell script, it delivers a clean, practical workflow designed from the ground up for Starfield modders.

---

## 📋 Change Log

### 🚀 v2.3 — Latest Features & Debug Menu

* **MO2 Profile Parsing:** Direct parsing for Mod Organizer 2 profile configurations.
* **Deep Conflict Analysis:** Asset scanning logic to spot overlapping mods and loose-file conflicts.
* **Patch Pinning:** Dedicated handling to lock StarUI mods and patches in position.
* **LOOT Integration:** Optional LOOT integration for automated load order sorting.
* **JSON Rule Overrides:** Custom JSON overrides to adjust sorting logic without editing the main script.
* **Automated Logging:** Game-specific log folders and local database tracking.
* **Safety Dry-Run Mode:** Simulation mode to safely test and preview load order changes step-by-step before applying edits to your MO2 profile.
* **DEBUG Manager:** Integrated crash management featuring a custom splash screen and log viewer.

### ⚙️ v2.1 — StarUI & Free Lanes Patch Intelligence

* **Automatic StarUI Detection:** Scans your mod list for StarUI Inventory and verifies menu components.
* **Smart Free Lanes Reordering:** Automatically shifts the Free Lanes patch directly below base StarUI for `.swf` overrides.
* **Targeted Conflict Exclusions:** Tags expected StarUI `.swf` overrides to eliminate false-positive error flags.
* **PowerShell List Stability Fix:** Upgraded data structures using `System.Collections.Generic.List[PSCustomObject]`.

### 🛠️ v2.0 — Core Engine Updates

* **Instant AppData Profile Resolver:** Targets standard MO2 AppData/LocalAppData paths with manual fallback.
* **Local Database Caching:** Initializes `mod_database.db` to cache mod categories locally for offline use.
* **Deep Analysis & Conflict Checker:** Scans loose files across enabled mods to output detailed conflict reports.
* **Live Mod Counter & Progress Bar:** Displays a dynamic `Write-Progress` bar and real-time scanning counter.
* **SFSE & Framework Verification:** Verifies `sfse_loader.exe` placement and scans for core framework requirements.

---

## 💻 System Requirements & Compatibility

* **OS:** Windows only (native PowerShell script). *Linux / Steam Deck setups are currently unsupported.*
* **Mod Manager:** Requires **Mod Organizer 2 (MO2)**.

---

## 🔮 Roadmap (Upcoming v2.4 Release)

* [ ] Code stabilization & performance optimizations w/ bug fixes (report bugs via the issue tracker!)
* [ ] Out-of-game cheat menu with auto-injection
* [ ] Expanded DEBUG suite & error diagnostic tools

---

## ⚠️ Important Operational Notice

> [!CAUTION]
> **STRONGLY RECOMMENDED: Keep Mod Organizer 2 CLOSED while running this tool.**
> 1. **Direct File Access:** Operates directly on `plugins.txt`, `loadorder.txt`, and `modlist.txt` on disk.
> 2. **Prevents Overwrites:** MO2 holds load orders in memory and will overwrite external disk edits on exit.
> 3. **UI Synchronization:** MO2 does not refresh interface elements in real time when files change externally.
> 
> 

### Practice Workflow

1. **Close Mod Organizer 2** completely.
2. **Run your `.bat` launcher script** and let the sorting engine complete its process.
3. **Reopen Mod Organizer 2** to review your newly categorized load order setup.
