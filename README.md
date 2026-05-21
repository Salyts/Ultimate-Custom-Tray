# Ultimate Custom Tray 2.0

Adds your own icons to the system tray. Each icon can run an
action on left-click and/or show a context menu on right-click.

---

## Installation

1. Install [Windhawk](https://windhawk.net/).
2. Open **Windhawk** and go to **Explore** → **Search**.
3. Enter **Ultimate Custom Tray** in the search field.
4. In the results, select [Ultimate Custom Tray](https://windhawk.net/mods/ultimate-custom-tray).
5. Click the "Install" button.

---

## Quick start

1. Open Windhawk settings for this mod.
2. Add one or more **Items** to the list.
3. Fill in **Label**, **Icon** and **Action** for each item.
4. Save — the icons appear in the tray immediately.

---

## Action formats

| Prefix | Example | Description |
|--------|---------|-------------|
| `" "` | `"C:\Program Files\Windhawk\windhawk.exe"` | Opens a file or folder by absolute path. |
| `~` | `~Downloads` and `~windhawk.exe` | Opens a folder or file by name. |
| `cmd:` | `cmd:control` | Runs a command through `cmd.exe`. |
| `shell:` | `shell:shutdown /r /f /t 0` | Runs through `powershell.exe`. |
| `press:` | `press:Win+E` or `press:0x5B;0x45` | Keyboard key press using a [Win32 key code](https://learn.microsoft.com/en-us/windows/win32/inputdev/virtual-key-codes). |
| `web:` | `web:https://windhawk.net/` | Opens a URL in the default browser. |
| `ms-settings:` | `ms-settings:bluetooth` | Opens a Windows Settings page. |

### Modifier signs (prepend to any action)

| Sign | Example | Description |
|--------|---------|-------------|
| `-` | `-"C:\Program Files\app.exe"` or `-shell:shutdown /r /f /t 0` | Runs as administrator. |
| `*` | `*cmd:tasklist` or `*shell:Get-Process` | Execution with a terminal window. (only for `cmd:` and `shell:` prefixes). |

Signs can be combined: `-*cmd:control` runs cmd in a visible window as admin.

---

## Icon field

| Type | Example | Description |
|---|---|---|
| **Glyph** | `E774` | Hex code of a [Segoe Fluent Icons](https://learn.microsoft.com/en-us/windows/apps/design/iconography/segoe-ui-symbol-font) glyph. 4-digit hex only, no `\u` prefix. |
| **Image file** | `C:\Icons\name.png` | Full path to an image. Supported: `.png` `.ico` `.jpg` `.bmp`. Recommended: 32x32 px, transparent background. |
| **App path** | `C:\Program Files\Windhawk\windhawk.exe` | Full path to an executable file (`.exe`, `.dll`). The icon will be extracted from the application. |

---

## Style options

### Icon color

- **Auto** - detects the current Windows theme (light/dark) on every click and redraws the tray icon accordingly.
- **White** - always white (for dark taskbar).
- **Black** - always black (for light taskbar).

### Context menu color

- **Auto** - follows the current Windows theme automatically.
- **Light** - light background, dark icons.
- **Dark** - dark background, light icons.

Controls the background and icon color inside the right-click context menu.

---

## Context Menu Settings

### Open menu near tray icon

When enabled, the context menu opens near the tray icon instead of at the cursor position. This allows precise positioning relative to the icon.

### Menu direction

Choose where the menu appears relative to the tray icon:
- **Above icon** - menu opens above the icon
- **Below icon** - menu opens below the icon
- **Left of icon** - menu opens to the left
- **Right of icon** - menu opens to the right

### Menu alignment

Controls how the menu is aligned relative to the icon:
- **Center** - menu is centered on the icon
- **Left** - menu's left edge aligns with the icon
- **Right** - menu's right edge aligns with the icon

### Menu offset

Distance in pixels between the tray icon and the menu (0-200). Default is 10px.

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
