# Evan's Sublime Text 3 Development Stack

## About

This document provides instructions to my fellow MAHI Lab members for duplicating my development stack in Sublime Text 3. I use it extensively for everything from writing Python, LaTeX, Markdown, and HTML, to transferring files over SFTP to our embedded systems.

## Installation

1. Download [Sublime Text 3.0](https://www.sublimetext.com/3) if you don't already have it. It is paid commercial software ($80), but will remain in a full evaluation mode until you finally feel guilty for steeling such an awesome product and decide to purchase a license.
2. Install [Package Control](https://packagecontrol.io/installation), the de facto standard for installing Sublime plugins.
3. Once Package Control is installed, press Ctrl+Shft+P in Sublime to open the Command Palette. Begin typing "install" and select "Package Control: Install Package" when it appears, then type the names of the package you want to install and press Enter when it appears.

## Themes/Appearance

First things first: change themes! My favorites:

- [Material Theme](https://packagecontrol.io/packages/Material%20Theme)
- [Spacegray](https://packagecontrol.io/packages/Theme%20-%20Spacegray)

Also, install [A File Icon](https://packagecontrol.io/packages/A%20File%20Icon) for unique sidebar file icons for literally every file extension known to man.

## Packages Everyone Should Have

These packages add awesome functionality to Sublime:

- [Terminal](https://packagecontrol.io/packages/Terminal)
- [SideBarEnhancements](https://packagecontrol.io/packages/SideBarEnhancements)
- [SyncedSideBar](https://packagecontrol.io/packages/SyncedSideBar)
- [BracketHighlighter](https://packagecontrol.io/packages/BracketHighlighter)

## Packages MAHI Lab Developers Should Have

These packages make development for MAHI Lab hardware (e.g. CompactRIO) easier:

- [SFTP](https://packagecontrol.io/packages/SFTP)
- [Markdown Preview](https://packagecontrol.io/packages/Markdown%20Preview)

## Packages for Git Integration

- [Git](https://packagecontrol.io/packages/Git)
- [GitGutter](https://packagecontrol.io/packages/GitGutter)

## Packages for Python Development

Sublime can be turned into an awesome lightweight Python IDE. First install pyflakes with pip from the command line (assuming you have Python installed):

```
pip install pyflakes
```

Then install these packages:

- [Anaconda](https://packagecontrol.io/packages/Anaconda)
- [SublimeLinter](https://packagecontrol.io/packages/SublimeLinter)
- [SublimeLinter-pyflakes](https://packagecontrol.io/packages/SublimeLinter-pyflakes)

Once Anaconda, SublimeLinter, and SublimeLinter-pyflakes are installed, navigate to **Preferences >> Package Settings >> Anaconda >> Settings - User** and add the following settings:

    ```
    {
      "anaconda_linting": false,
      "swallow_startup_errors": true,
      "hide_snippets_on_completion": true,
      "complete_parameters": true,
      "auto_formatting_timeout": 5
    }
    ```

Open any *.py Python file in Sublime. Navigate to **Preferences >> Settings - Syntax Specific** and add the following into Python.sublime-settings:

    ```
    {
      "auto_indent": true,
      "rulers": [79],
      "smart_indent": true,
      "trim_automatic_white_space": true,
      "use_tab_stops": true,
      "word_wrap": false,
      "wrap_width": 80
    }
    ```

Right-click in the Python file and choose **SublimeLiner >> Toggle Linter...** from the context menu. Make sure **pyflakes** is enabled.

## Packages for LaTeX

Sublime can be used to edit and compile LaTeX documents:

First, make sure you have [MiKTeX](https://miktex.org/) installed. Also, install [Sumatra PDF](https://www.sumatrapdfreader.org/free-pdf-reader.html) and [GhostScript](https://www.ghostscript.com/) for extended capabilities. Then install the following package:

- [LaTeXTools](https://packagecontrol.io/packages/LaTeXTools)
