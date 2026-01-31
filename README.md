# Ultimate VS Code Dev Environment (VIM-Powered Perfection)

This repo tells you exactly how to make the ultimate VS Code development setup (Opinionated obviously).

## Motivation

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

**Optional** but highly recommended:

- [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)

## Setup Guidelines

1. Clone the repository where you want to store the **custom CSS and JS files**

```bash
git clone https://github.com/sazuyakun/vscode-setup
```

2. Enter directory

```bash
cd vscode-setup
code .
```

3. Update the settings.json file in this directory
   - On **vscode**, right click on any empty space of your directory and click `Copy Path` (eg: Users/...)
   - On **terminal**, enter `pwd` and copy the path printed out

```json
// line 24
"vscode_custom_css.imports": [
    "file:///path/to/custom-vscode.css", // Replace your css file path here
    "file:///path/to/vscode-script.js"   // Replace your js file path here
]
```

4. Make sure all the extensions listed above are installed properly and enabled in VS Code.

5. Copy the contents of the `settings.json` file in this directory to User `settings.json`
   - `cmd+shift+p` on Mac
   - Search for `Preferences: Open User Settings (JSON)`
   - Replace all the contents of this file.
   - Save the file

6. `cmd + shift + p` again and select `Enable Custom CSS and JS` (Will ask to reload)

7. **Finally:** Copy the contents of the `keybindings.json` file in this directory to User `keybindings.json`
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
