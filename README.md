Install Oh my Posh!

```
1. install terminal and powershell from MS store

2. shell: winget install JanDeDobbeleer.OhMyPosh -s winget

3. Reopen shell

4. run: New-Item -Path $PROFILE -Type File -Force

5. run: notepad $PROFILE. Then paste: "oh-my-posh init pwsh | Invoke-Expression". Save and reopen shell.

6. Install a nerd font for icons to work. https://www.nerdfonts.com/font-downloads

7. Go to shell settings or press "Ctrl + ," then open Json file.

8. Write on defaults property. More info: https://learn.microsoft.com/en-us/windows/terminal/customize-settings/color-schemes.
  {
    "font": {
      "face": "DroidSansMono NF",
      "size": 11
    },
    "opacity": 40,
    "colorScheme": "One Half Dark",
    "useAcrylic": true
  }

9. (Optional) change oh my posh theme. https://ohmyposh.dev/docs/themes. Run shell: Get-PoshThemes

10. (Optional) Open the $PROFILE file: notepad $PROFILE. Then replace the content with: oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\catppuccin.omp.json" | Invoke-Expression. you can select the theme you want just replace catppuccin for other name and save it or use theme.json, restart.

11. Open shell settings or press "Ctrl + ," then on Startup replace default shell with PowerShell and save.

```

Install icons for folders on PowerShell.

```
1. We will use this repo https://github.com/devblackops/Terminal-Icons. Run: Install-Module -Name Terminal-Icons -Repository PSGallery and press Y.

2. Open $PROFILE settings. notepad $PROFILE and paste at the end: Import-Module -Name Terminal-Icons and save.

3. Run: ls. and see the icons!

```

Use terminal on vscode

```
1. Open settings.json in vscode

2. add or replace this lines:
  "terminal.integrated.defaultProfile.windows": "PowerShell",
  "terminal.integrated.fontFamily": "DroidSansMono NF",
  "terminal.integrated.fontSize": 14

3. Restart vscode

```
