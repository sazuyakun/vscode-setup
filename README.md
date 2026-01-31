# Ultimate VS Code Dev Environment (VIM-Powered Perfection)

This repo tells you exactly how to make the ultimate VS Code development setup (Opinionated obviously).

## Why this Setup?

I have been a dedicated user of Neovim for the past couple of months. From learning all the VIM motions and bindings to setting up Neovim using Lua, I realized I was getting too deep into the rabbit hole. (I also got myself a split keyboard!) This has definitely helped me become a more "efficient" developer. But I always missed the `plug-and-play` features that VS Code provided out of the box. So yeah, this is me migrating my fast dev neovim experience to VS Code. This is definitely an experimental setup right now but will also (hopefully) improve over time.

## Before you proceed

I highly recommend you to get comfortable with VIM motions and keybindings before adopting this setup.

## Extensions to install

> **NOTE:** Apart from Copilot, these extensions are needed for the specific settings to work. The custom VIM bindings take a lot of inspiration from [JOSEAN MARTINEZ](https://www.youtube.com/@joseanmartinez). You can always customise and add more according to your preferences

- [Catppuccin Theme](https://marketplace.visualstudio.com/items?itemName=Catppuccin.catppuccin-vsc)
- [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)
- [Custom UI Style](https://marketplace.visualstudio.com/items?itemName=subframe7536.custom-ui-style)
- [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Vim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)

### **Optional** but highly recommended:

- [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)

---

## Setup Guidelines

### 1: Clone the Repository

Open your terminal and run:

```bash
git clone https://github.com/sazuyakun/vscode-setup
cd vscode-setup
code .
```

### 2: Get Your Absolute Path

> ⚠️ **Critical Step:** You'll need the absolute path to your cloned repository.

Choose **one** of these methods:

#### Option A: Using VS Code

- Open the Explorer sidebar
- Right-click on any empty space in the file tree
- Select **Copy Path**

#### Option B: Using Terminal

```bash
pwd
```

### 3: Update Configuration Path

- Open `settings.json` in your cloned repository
- Navigate to **line 24** (approximately)
- Replace the placeholder paths with your absolute path:

```json
"vscode_custom_css.imports": [
    "file:///YOUR/ABSOLUTE/PATH/custom-vscode.css",
    "file:///YOUR/ABSOLUTE/PATH/vscode-script.js"
]
```

### 4: Install Required Extensions

Ensure all extensions listed in the repository are **installed** and **enabled**

### 5: Apply User Settings

- Open the Command Palette:
  - **macOS:** `Cmd+Shift+P`
  - **Windows/Linux:** `Ctrl+Shift+P`
- Search for: `Preferences: Open User Settings (JSON)`
- **Replace all contents** with the contents from your repository's `settings.json`
- **Save the file** (`Cmd+S` / `Ctrl+S`)

### 6: Enable Custom CSS and JS

- Open the Command Palette again (`Cmd+Shift+P` / `Ctrl+Shift+P`)
- Search for and select: `Enable Custom CSS and JS`
- VS Code will prompt you to reload — click **Reload**

> 💡 You may see a warning about VS Code being corrupted. This is normal and expected when using custom CSS/JS.

### 7: Apply Keyboard Shortcuts

- Open the Command Palette:
  - **macOS:** `Cmd+Shift+P`
  - **Windows/Linux:** `Ctrl+Shift+P`
- Search for: `Preferences: Open Keyboard Shortcuts (JSON)`
- **Replace all contents** with the contents from your repository's `keybindings.json`
- **Save the file** (`Cmd+S` / `Ctrl+S`)

---

## ✨ You're All Set!

Make changes and customise it further from here for your liking

### Note:

All the additional changes in the settings that you make / are made while downloading other extensions will get appended to this section in `settings.json`:

```json
  // Additional
  "window.newWindowProfile": "Default",
  ...
```

## Troubleshooting

If custom CSS/JS doesn't load:

1. Verify the file paths are absolute (start with `file:///`)
2. Check that paths use forward slashes `/` (even on Windows)
3. Ensure no typos in the file paths
4. Try running `Reload Custom CSS and JS` command

---

**Feedback & Contributions:** Issues and pull requests are welcome!
