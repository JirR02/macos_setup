# My MacOS Setup

This guide will guide you through the steps of setting up a macbook for students with development as a side hustle. This setup is heavily focused on taking Notes with LaTeX. Of course other options are available. As I am quite new to development by contributing to public repositoires the development side is not quite efficient yet but will be updated regulary.

![MacBook Development](https://images.unsplash.com/photo-1555066931-4365d14bab8c?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MXwxMTc3M3wwfDF8c2VhcmNofDE2fHxjb2RlfGVufDB8fHw&ixlib=rb-1.2.1&q=80&w=2000)

---

## Table of Contents
1. [System Preferences](#system-preferences)
2. [Terminal](#terminal)
3. [Apps](#apps)

---

## System Preferences

How you set up the general appearance of the mac is individual. If you want to have the same setup do the following:

### Dock

1. Put the Dock to the left of the screen
2. Autohide the dock
3. Add spacers to the dock
4. Remove the "Recently opened section"

To add spacers to the dock run the following command:

    $ defaults write com.apple.dock persistent-apps-array-add '{"tile-type"="spacer-tile";}'; killall Dock
This command can be run multiple times to add multiple spacers.
 
### Menu Bar

1. Autohide the Menu Bar

The Apps wich appear in the Menu Bar as Icons are mentioned in [Apps](#apps)

## Terminal

The terminal of choice depends on the preference. I use the Terminal App which already is installed on MacOS but there are many more. (iTerm, Kitty, Terminator, ...) You are welcome to install your prefered terminal. The setup should work with all terminals.

### Oh My Zsh

![Oh My Zsh](https://camo.githubusercontent.com/4db3e4069e59f51d03dd3e7fa5e89ab8fb95c9f4acda36cd5bfdf58d95269d92/68747470733a2f2f6f686d797a73682e73332e616d617a6f6e6177732e636f6d2f6f6d7a2d616e73692d6769746875622e706e67)

Oh My Zsh is an open source, community-driven framework for managing your zsh configuration. ([OhMyZsh](https://ohmyz.sh/))

To install Oh My Zsh run the following command in your Terminal

    $ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

After that open up the `.zshrc` file with any text editor app (TextEdit is installed by default on MacOS) find `plugins=()` and edit it as follows

```zsh
plugins=(git zsh-syntax-highlighting zsh-autosuggestions sudo copypath copyfile copybuffer web-search)
```
Restart the terminal by quitting it or by running the command `zsh`. If an error occours run the following commands

    $ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    $ git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

This should resolve the error.

### HomeBrew

![HomeBrew](https://brew.sh/assets/img/homebrew.svg)

The Missing Package Manager for macOS (or Linux)

HomeBrew eases the install process of an App or Script by downloading it over the terminal and eliminates the "Copy to Applications Folder".

To install HomeBrew run the following command

    $ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Now that the Terminal is Setup we can install the apps

## Apps

To install my apps you have to use the following commands

    $ wget https://gitlab.com/JirR02/macos_homebrew_packages/-/raw/main/Brewfile
    $ brew bundle

This will also install the App which appear in the Menubar.

The following apps will be installed:

For Code and Design:

- Visual Studio Code
- Blender
- FreeCAD
- Cura Ultimaker
- Neovim
- VNC Viewer

For Work:

- Adobe Acrobat Reader
- Zathura
- Microsoft Office
- Nextcloud
- Teams
- OBS
  
For Terminal:

- vifm
- Python 3.10
- thefuck
- zip
- unzip 
- git

## LaTex and Visual Studio Code Setup

My LaTex setup consists of the Visual Studio Code editor with the Zathura PDF Viewer on the side. The Zathura PDF Viewer always shows the state of the pdf after compiling. In order to keep up with the teacher I tried to make the note taking process with LaTex as efficient as possible.

