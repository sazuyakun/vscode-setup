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

## Setup Guidelines

### 1. Clone the repository where you want to store the **custom CSS and JS files**

```bash
git clone https://github.com/sazuyakun/vscode-setup
cd vscode-setup
code .
```

### 2. Get the Absolute Path (Very Important)

Choose one method:
**Option A - VS Code:**

- Right-click in the Explorer sidebar (Any empty space in the file tree)
- Select `Copy Path`

**Option B - Terminal:**

```bash
pwd
```

### 3. Update the `settings.json` file in this directory (around line 24)

```json
"vscode_custom_css.imports": [
    "file:///YOUR/ABSOLUTE/PATH/custom-vscode.css",
    "file:///YOUR/ABSOLUTE/PATH/vscode-script.js"
]
```

### 4. Make sure all the extensions listed above are installed properly and enabled in VS Code.

### 5. Copy the contents of the `settings.json` file in this directory to User `settings.json`

- `cmd+shift+p` on Mac
- Search for `Preferences: Open User Settings (JSON)`
- Replace all the contents of this file.
- Save the file

### 6. `cmd + shift + p` again and select `Enable Custom CSS and JS` (Will ask to reload)

### 7. **Finally:** Copy the contents of the `keybindings.json` file in this directory to User `keybindings.json`

- `cmd+shift+p` on Mac
- Search for `Preferences: Open Keyboard Shortcuts (JSON)`
- Replace all the contents of this file.
- Save the file

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
