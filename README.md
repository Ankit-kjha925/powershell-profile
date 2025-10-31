# PowerShell Profile

My custom PowerShell profile with Oh My Posh themes, custom aliases, and productivity enhancements.

## Features

- **Oh My Posh** integration with multiple theme options
- **Custom aliases** for common commands
- **PSReadLine** configuration with predictive IntelliSense
- **Terminal-Icons** for better file visibility
- **Custom functions** for quick navigation

## Prerequisites

Before using this profile, install the following:

1. **Oh My Posh**
   ```powershell
   winget install JanDeDobbeleer.OhMyPosh -s winget
   ```

2. **Terminal-Icons**
   ```powershell
   Install-Module -Name Terminal-Icons -Repository PSGallery
   ```

3. **PSReadLine** (usually pre-installed, but can be updated)
   ```powershell
   Install-Module -Name PSReadLine -AllowPrerelease -Force
   ```

4. **Nerd Font** (recommended for proper icon display)
   - Download from [Nerd Fonts](https://www.nerdfonts.com/)
   - Popular choices: FiraCode Nerd Font, CascadiaCode Nerd Font

## Installation

### Option 1: Clone the Repository

1. Clone this repository:
   ```powershell
   git clone https://github.com/Ankit-kjha925/powershell-profile.git
   ```

2. Copy the profile file to your PowerShell profile location:
   ```powershell
   Copy-Item .\powershell-profile\Microsoft.PowerShell_profile.ps1 $PROFILE -Force
   ```

3. Copy the Oh My Posh theme files:
   ```powershell
   Copy-Item .\powershell-profile\*.omp.json (Split-Path $PROFILE) -Force
   ```

### Option 2: Manual Setup

1. Find your PowerShell profile location:
   ```powershell
   $PROFILE
   ```

2. Download `Microsoft.PowerShell_profile.ps1` from this repository

3. Place it at the profile location (create the directory if it doesn't exist)

4. Download the `.omp.json` theme files and place them in the same directory

## Customization

### Aliases

The profile includes these aliases:
- `tt` → `tree`
- `ll` → `ls`
- `g` → `git`
- `vim` → `nvim`
- `cc` → `clear`
- `dd` → `dir`
- `cdargos` → Navigate to `C:\ARGOS`(ARGOS was the folder which mainly consisted my projects and i needed to access it very frequently. feel free to add your own folder that you need quick access for)

### Themes

The profile uses the `amro` theme by default (line 18). To switch themes:

1. Uncomment your desired theme line in the profile
2. Comment out the current active theme
3. Reload your profile: `. $PROFILE`

Available custom themes:
- `myprofile.omp.json` - Tokyo
- `myprofile2.omp.json` - Tokyo Night Storm
- `myprofile3.omp.json` - Amro (default, fast and efficient)
- `myprofile4.omp.json` - Material

### Functions

- `whereis <command>` - Find the path of a command
- `argos` / `cdargos` - Quick navigation to ARGOS directory

## Reload Profile

After making changes, reload the profile:
```powershell
. $PROFILE
```

## License

Feel free to use and modify as needed!
