# KaliArch

## Index
* [About](#-about)
* [How it works](#how-it-works)
* [Usage Modes](#usage-modes)
* [Recommendations](#recommendations)
* [Future Features](#future-features)
* [References](#references)

---

## 💡 About
> This simple script allows you to automatically install utilities through a *.txt* list, automatically apply customizable themes, dynamically add wallpapers according to the user's preferences, and automatically restore the original settings if the user wishes.

---

## How it works
- The script must be run within the repository directory.
- Allows you to install packages listed in a `.txt` file through the specified package manager.
- You can remove all packages and files installed by the script at any time. - The user can apply **Kali-like** themes, for example, which can be customized.
- It is also possible to configure a **dynamic wallpaper**, which changes automatically according to the configured time and the chosen mode.
- Before any modification, configuration files or directories are **backed up** with the `.old` extension to ensure security.

⚠️ **Important:**
- It is always recommended to run only as a normal user; the script itself will ask for the *sudo* password if necessary.
- After applying the theme, it is recommended to review and, if necessary, customize the added configuration files.
- `.old` files allow you to restore the original configuration at any time.

---

## Usage Instructions

```bash
# Install packages listed in a file
python3 KaliArch.py install-utilities utilities.txt

# Uninstall packages listed in a file
python3 KaliArch.py uninstall-utilities utilities.txt

# Apply the Kali-like theme
python3 KaliArch.py install-kalitheme

# Apply the Kali-like theme with dynamic wallpaper
python3 KaliArch.py dynamic-background 5 randomize ~ kalitheme

# You can also use the default order instead of random
python3 KaliArch.py dynamic-background 5 ordered ~ kalitheme

# Remove the Kali-like theme and restore backups
python3 KaliArch.py uninstall-kalitheme
```
---

## Recommendations
- Run in virtual machines during or after installation.
- Customize the *packages.json* of *themes* or the script if necessary, but be careful to follow the script and packages.json standards.
- Customize `~/.config/i3/config` to your preferences after applying the theme.
- Configure the terminal color, theme, or transparency, if necessary.
- Adjust the **Kitty** fonts if necessary.
- Set **Zsh** as the default shell.

---

## References
- [Kitty Themes](https://github.com/dexpota/kitty-themes)
