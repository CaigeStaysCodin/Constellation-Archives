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
