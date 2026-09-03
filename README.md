[VERSION 2.3 - LATEST FEATURES & DEBUG MENU]

* MO2 Profile Parsing    : Direct parsing for Mod Organizer 2 profile configurations.
* Deep Conflict Analysis : Asset scanning logic to spot overlapping mods and file conflicts.
* Patch Pinning          : Dedicated handling to lock StarUI mods and patches in position.
* LOOT Integration       : Optional LOOT integration for automated load order sorting.
* JSON Rule Overrides    : Custom JSON overrides to adjust sorting logic without editing main script.
* Automated Logging      : Game-specific log folders and database tracking.
* Safety Dry-Run Mode    : Simulation mode to test load order changes safely before writing. This is so I can build trust with the modders in different communities. I want you to know this code doesn't harm you! I'm just here to help! Now you can see every step that I perform to know if I'm okay to run!
* DEBUG Manager          : Integrated crash management featuring custom splash screen & log viewer.

[VERSION 2.1 - STARUI & FREE LANES PATCH INTELLIGENCE]

* Automatic StarUI Detection      : Checks mod list for StarUI Inventory and verifies menu components.
* Smart Free Lanes Reordering     : Shifts Free Lanes patch directly below base StarUI for .swf overrides.
* Targeted Conflict Exclusions    : Custom-tags expected StarUI .swf overrides to prevent false error flags.
* PowerShell List Stability Fix   : Upgraded data structures (System.Collections.Generic.List[PSCustomObject]).

[VERSION 2.0 - CORE ENGINE UPDATES]

* Instant AppData Profile Resolver: Targets standard MO2 AppData/LocalAppData paths with manual fallback.
* Local Database Caching          : Initializes mod_database.db to cache mod categories for offline use.
* Deep Analysis & Conflict Checker: Scans loose files across enabled mods to output conflict reports.
* Live Mod Counter & Progress Bar : Displays dynamic Write-Progress bar and real-time scanning counter.
* SFSE & Framework Verification   : Ensures sfse_loader.exe placement and scans for core frameworks.

---

# ==================================================================================================
IMPORTANT OPERATIONAL NOTICE

## [!] STRONGLY RECOMMENDED: Keep Mod Organizer 2 CLOSED while running this tool.
1. Direct File Access : Works on plugins.txt, loadorder.txt, and modlist.txt on disk.
2. Prevents Overwrites: MO2 holds load orders in memory and overwrites external disk edits on exit.
3. UI Synchronization : MO2 does not refresh interface elements in real time when files change.

# ==================================================================================================
BEST PRACTICE WORKFLOW

## Step 1: Close Mod Organizer 2 completely.
Step 2: Run your .bat launcher script and let the sorting engine complete its process.
Step 3: Reopen Mod Organizer 2 to review your newly categorized load order setup.

# ==================================================================================================
KEY PROGRAM FEATURES MATRIX

## FEATURE                             | FUNCTION
------------------------------------+-------------------------------------------------------------
Instant AppData Profile Finder      | Checks %APPDATA% & %LOCALAPPDATA% paths instantly.
Live Mod Counter & Tracker          | Displays real-time terminal progress bar as mods scan.
Local Database Caching              | Stores Nexus category data into local mod_database.db file.
SFSE Validator                      | Verifies sfse_loader.exe location in main game root directory.
Deep Analysis & Conflict Checker    | Scans loose files to detect data overlaps & overwrite conflicts.
Categorized Sorting Engine          | Sorts ESM/ESP/ESL files into clean logical structure.
Dual-File MO2 Sync                  | Updates plugins.txt, loadorder.txt, and modlist.txt in sync.

# Constellation-Archives-v2.1-REVISED-
This is the .zip file for my auto-sorter mod tool for Mod Organizer 2. Please see my Nexus Mod Page for more details. 
https://www.nexusmods.com/starfield/mods/18126

Why its different...
-----------------------
While automated tools, load-order keepers, and standard sorting engines (like LOOT) have existed for Bethesda games for years, this tool's approach is unique in how it tackles simultaneous left-panel preservation and right-panel category intelligence.

Most standard automated tools and broad mod managers tend to fall into two camps:

The "Blunt Force" Sorter: Traditional sorters or plugins often reorganize everything alphabetically or overwrite the user's entire profile configuration, which accidentally scrambles custom drag-and-drop file priorities on the left panel (the exact headache v2.1 Revised solves).  
PS1

Single-Focus Keepers: Most standalone tools built for Starfield usually just act as static backup monitors—like locking down a reference plugins.txt file so it doesn't change—rather than dynamically parsing metadata, querying Nexus categories via API, running deep loose-file conflict analysis, and protecting specific layout configurations like StarUI/Free Lanes overrides all in one script.  
PS1

So while it shares space with other utilities designed to keep load orders stable, combining automated database-driven category sorting, deep file-overlap checks, and precise left-panel layout preservation into a single portable PowerShell script gives it a very distinct, practical workflow that sets it apart from standard tools.
Here are the updated release notes with the corrected title highlighting its **Conflict Detection Engine**:

---

# Starfield MO2 Mod Auto Sorter, Conflict Checker & Analysis v2.1 (Revised)

Welcome to the **Early Access** release for v2.1 Revised! This update introduces crucial under-the-hood fixes to ensure your Mod Organizer 2 profile layout stays completely secure while optimizing your plugin load order.

### 📝 Change Log & What's New

* **Left-Panel Layout Protection (`modlist.txt`):**
* Overhauled Step `[5/8]` to stop the script from flushing or alphabetizing your entire left panel.


* It now safely preserves your custom drag-and-drop priorities and active/inactive checkboxes.




* **Smart UI Patch Enforcement:**
* Retains the automated safety check for StarUI, automatically snapping the *Free Lanes Compatibility Patch* right below base StarUI if it's out of order so your menu SWFs don't break on game updates.




* **Clean Plugin Harvesting:**
* Step `[6/8]` now strictly reads your active checkboxes (`+`) to ensure disabled mods never accidentally get their plugins scraped into your load order.




* **Optimized Right-Panel Sorting (`plugins.txt` / `loadorder.txt`):**
* Fully organizes your plugins into the correct dependency hierarchy (Base masters $\rightarrow$ Frameworks $\rightarrow$ UI $\rightarrow$ ESMs $\rightarrow$ ESPs $\rightarrow$ Patches placed safely at the bottom).





---

*As always—don't forget Roach Race! Feel free to open an issue or drop feedback if you're testing this early build out. Fly safe, space cowboys and cowgirls!* 🚀
