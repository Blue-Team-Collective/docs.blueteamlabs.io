# Scripts and Automation
While this guide focuses on building from scratch to help build some of the more foundational knowledge that engineers and architects need, I do provide some scripts and resources for automating the provisioning of this lab where possible.

## Scripts Github
You can find all scripts on the Blue Team Collective Github organization page.

!!! tip "Bookmark This!"
    [Github - Blue Team Collective](https://github.com/Blue-Team-Collective/)

## Working with the Repo
While it is possible to download an archive or directly access the files via HTTPS, this is not recommended. Instead, you should use Git in your lab to get familiar with version control systems. This is a fundamental skill in my opinion as an engineer in the future where idempotent and automated configuration take precendence. 

### Install Git
For all systems, the below instructions require a terminal with administrative privilege on the system.

#### Linux
Use the following commands to install git on Linux based systems.
=== "dpkg Based (Debian/Ubuntu)"
    ```sh
    sudo apt-get install git
    ```

=== "pacman Based (Arch, Manjaro)"
    ```sh
    sudo pacman -Sy git
    ```
=== "yum Based (Fedora, RHEL, Rocky)"
    ```sh
    sudo yum install git
    ```

#### Mac OS
For Mac OS, the easiest way to install and maintain the updates of the software is using homebrew  [^1] [^2]
```sh
# Fist, install HomeBrew (see https://brew.sh/):
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Second, install git
brew install git
```

#### Windows
For Windows, use PowerShell to install WinGet[^3] and install the git client for Windows[^4]
```powershell
# Install WinGet
# This is direct from Microsoft documentation, for updates check https://learn.microsoft.com/en-us/windows/package-manager/winget/#install-winget
$progressPreference = 'silentlyContinue'
Write-Information "Downloading WinGet and its dependencies..."
Invoke-WebRequest -Uri https://aka.ms/getwinget -OutFile Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle
Invoke-WebRequest -Uri https://aka.ms/Microsoft.VCLibs.x64.14.00.Desktop.appx -OutFile Microsoft.VCLibs.x64.14.00.Desktop.appx
Invoke-WebRequest -Uri https://github.com/microsoft/microsoft-ui-xaml/releases/download/v2.7.3/Microsoft.UI.Xaml.2.7.x64.appx -OutFile Microsoft.UI.Xaml.2.7.x64.appx
Add-AppxPackage Microsoft.VCLibs.x64.14.00.Desktop.appx
Add-AppxPackage Microsoft.UI.Xaml.2.7.x64.appx
Add-AppxPackage Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle
Add-AppXPackage -Path .\Microsoft.DesktopAppInstaller_8wekyb3d8bbwe.msixbundle


# Install Git
winget install --id Git.Git -e --source winget

```

### Clone the Repo
```sh
git clone https://github.com/blue-Team-Collective/build-scripts
```

### Pull the Latest Changes from the Repository 
```sh
cd build-scripts
git pull
```

### Discard Changes and Reset to Current HEAD
This resets the content to the current head and discards all changes [^5]
```sh
cd build-scripts
git reset --hard
```

[^1]: See https://git-scm.com/download/mac | Installing Git on MacOS using the recommendations on Git's homepage requires homebrew or Mac Ports.
[^2]: See https://brew.sh/ | Homebrew provides a oneliner to easily install Brew via command line on MacOS systems.
[^3]: See https://learn.microsoft.com/en-us/windows/package-manager/winget/ for information about the winget application.
[^4]: See https://git-scm.com/download/win for information about installing the Git client on Windows.
[^5]: See https://git-scm.com/docs/git-reset for information about the Git reset command