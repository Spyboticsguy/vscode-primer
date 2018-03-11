# Visual Studio Code - A Primer

[Visual Studio Code](http://code.visualstudio.com) is a cross-platform text editor built by Microsoft with features to support code development, including [debugging tools](#Debugging), [code completion](#code-completion), and syntax highlighting.

The program is built in Electron, a GitHub framework for developing cross-platform desktop applications in JavaScript. GitHub's code editor, [Atom](http://atom.io), is also written in this framework.

This document will serve as a brief overview of some of the key features Visual Studio Code provides as a code editor, with links to the VS Code [documentation](https://code.visualstudio.com/docs) for more information.

Microsoft provides a comprehensive set of quick-start guides which can be accessed from the official [documentation](https://code.visualstudio.com/docs). This guide is not intended to serve as a replacement for these quick-start resources, but as a companion to highlight some of the key features in more depth.

## The Basics
Visual Studio Code - not to be confused with the Visual Studio IDE - is an open-source text editor written by Microsoft.

When you start up the editor for the first time, you are greeted by the **Welcome** screen:

![Welcome Screen][welcome-screen]

This screen will appear every time you open a new window with the editor as well as every time you close and re-open the application. You can disable this behavior with the checkbox in the lower-left corner of the screen.

This screen contains 5 sections, each of which will be described briefly below:
- [Start](#start)
- [Recent](#recent)
- [Help](#help)
- [Customize](#customize)
- [Learn](#learn)

### Start
This section contains options for starting new projects or opening a new folder.

**New file** will create a new file in the current text editor:

![New File][new-file]

**Open folder...** will open a folder on the disk as the current workspace:

![Open folder...][open-folder]

**Add workspace folder...** is a bit of a strange option, mostly useful for when your project files are split across multiple distant locations on the disk. You can find more information about multi-root workspaces [here](https://code.visualstudio.com/docs/editor/multi-root-workspaces).

### Recent
This section contains links to the workspaces and files you have recently opened. Clicking on one of the entries will open the workspace or file in your current editor.

### Help
This section provides links to common resources used when learning Visual Studio Code. This is an excellent place to look if you want more information on the features of the editor, or if you want to report an issue on GitHub.

This section also includes a link to the keyboard shortcuts PDF, which is an excellent reference for learning the editor's keybinds.

### Customize
This section provides quick access to the most important customization features available in Visual Studio Code.

**Tools and languages** will open up the [**Extensions**](#extensions) panel with a list of popular language extensions:

![Language Extensions][language-exts]

Installing these will add support for various languages, including C/C++, Go, and PHP to Visual Studio Code. These extensions often include custom syntax highlighting, debugging support, and code completion features specific to that language.

**Install keyboard shortcuts** will open up the [**Extensions**](#extensions) panel as well, but with a list of popular keyboard shortcut extensions:

![Keymap Extensions][keymap-exts]

These extensions add keybindings from various other editors into Visual Studio Code, making it easy to transition from another type of editor.

**Color theme** will open up the command pallete with a list of pre-installed themes available to customize the look of your editor:

![Color Themes][color-themes]

You can obtain more themes from the [extension marketplace](#extensions).

### Learn
This section provides a select number of resources used for learning your way around the Visual Studio Code editor.

**Find and run all commands** will open up the command pallete, allowing you to search through all the commands available in the editor. You can also access the command pallete by pressing `cmd+shift+p` on Mac and `ctrl+shift+p` on Windows and Linux.

**Interface overview** will display an overlay on top of your editor highlighting the important UI elements of the application.

![Interface Overview][overlay]

Finally, **interactive playground** will launch a short, interactive tutorial which provides a breif overview of the code editing features of Visual Studio Code.

![Interactive Playground][playground]

<!--- Images go here. --->
[welcome-screen]: img/welcome.png
[new-file]: img/new-file.png
[open-folder]: img/open-folder.png
[language-exts]: img/language-exts.png
[keymap-exts]: img/keymap-exts.png
[color-themes]: img/color-theme.png
[overlay]: img/overlay.png
[playground]: img/playground.png