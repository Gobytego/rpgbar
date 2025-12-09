# ⚔️ RPG BAR: Terminal HUD (Health-Up Display)

The **RPG BAR** is a Bash shell script designed to gamify your terminal experience by providing a persistent Heads-Up Display (HUD) that monitors your system resources and tracks personal progress.

Your system's **CPU** and **RAM** usage are translated into your character's Stamina and Health, providing a fun, real-time visual indicator of your machine's performance right above your prompt.

## ✨ Features

* **Real-time Monitoring:** Tracks CPU (Stamina/SP) and RAM (Health/HP) usage.
* **Persistent Save File:** Tracks your Level, XP, and Gold across sessions.
* **XP & Leveling:** Gain XP with every command and Level Up!
* **Gold System:** Receive periodic Gold awards for spending time in the terminal.
* **Customizable Display:** Toggle between Unicode (default) and ASCII borders/emojis.
* **Non-Intrusive:** Uses `PROMPT_COMMAND` and `tput` to draw the bar at the top of the terminal, restoring your cursor position correctly.

---

## 🚀 Quick Setup

### 1. Save the Script

1.  Save the complete script content (File 1 above) to a file named `rpgbar` (or `rpgbar.sh`) in a directory that is included in your system's `$PATH`.
    * **Recommended Location:** `~/.local/bin/rpgbar`

2.  Make the script executable:

    ```bash
    chmod +x ~/.local/bin/rpgbar
    ```

### 2. Enable the HUD (Permanent)

To ensure the **RPG BAR** starts automatically in every session, add the following line to your shell configuration file (`~/.bashrc` or `~/.zshrc`):

```bash
# Add this line to the end of your ~/.bashrc or ~/.zshrc file
source ~/.local/bin/rpgbar
```
---
### For Options run the following like 
```bash
source ~/.local/bin/rpgbar --help
```
* --help	Shows the setup instructions and a list of all available commands.
* --check	Runs a compatibility test for required system utilities (tput, bc, top, etc.) and displays current setting status.
* --settings	Opens an interactive menu to toggle display options (Emojis/Unicode and ASCII Borders).
* --reset	Deletes the save file ($HOME/.rpgbar.save) and resets your Level, XP, Gold, and all display settings to default.
