# Visual Studio Code - A Primer

[Visual Studio Code](http://code.visualstudio.com) is a cross-platform text editor built by Microsoft with features to support code development, including [debugging tools](#debugging), [code completion](#code-completion), and syntax highlighting.

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

**Find and run all commands** will open up the command pallete, allowing you to search through all the commands available in the editor. You can also access the command pallete by pressing <kbd>⌘</kbd>+<kbd>⇧</kbd>+<kbd>P</kbd> on Mac and <kbd>CTRL</kbd>+<kbd>⇧</kbd>+<kbd>P</kbd> on Windows and Linux.

**Interface overview** will display an overlay on top of your editor highlighting the important UI elements of the application.

![Interface Overview][overlay]

Finally, **interactive playground** will launch a short, interactive tutorial which provides a brief overview of the code editing features of Visual Studio Code.

![Interactive Playground][playground]

## Working in Visual Studio Code
This is not a guide on how to use a text editor. That information is beyond the scope of this document; instead, this section will highlight some of the code editing features of Visual Studio Code.

### Code Completion
One of the most important features of any code editor is code completion, a feature which Visual Studio Code provides out-of-the-box for a number of languages, including JavaScript, TypeScript, JSON, HTML, and other web-centric languages and file formats. You can read more about the specifics of the feature (which Microsoft calls IntelliSense) in their [documentation](https://code.visualstudio.com/docs/editor/intellisense).

Visual Studio Code provides the following code completion tools:
- The ability to see variable names, functions, and common code snippets while typing
- The ability to see the usage information of function calls, including the types of paramters accepted by the method
- Other contextual code completion as provided by the language extension

To see some of these tools in action, try out the interactive playground, found on the [Welcome](#welcome) screen.

### Navigation
Visual Studio Code provides a number of tools to move around within a file or project, which are detailed [here](https://code.visualstudio.com/docs/editor/editingevolved). These tools provide ways to jump around or between files based on the context of your code; this includes jumping to definitions of variables, functions, or classes, depending on the support provided by the language extension.

The best way to learn about navigation in Visual Studio Code is to try it! Open up one of your existing projects or start a new one, then reference the documentation when you need to jump between areas in your project. See if Visual Studio Code provides a navigation tool that helps you perform that jump in an easier or quicker manner.

### Syntax and Error Highlighting
Visual Studio Code and its extensions provide comprehensive support for a number of languages, including tools like highlighting to help make source navigation and code writing easier.

The vast majority of programming languages on the market have a syntax highlighting extension for Visual Studio Code. They are the easiest type of language support to write, and, as a consequence, are the most readily available type of language support in the [Marketplace](#extensions).

This syntax highlighting feature will assign different styles and colors depending on the type of token. These colors and styles can be customized by your current theme or in your personal [settings](#settings).

Depending on the language extension you are using, you may be able to see underlines in your project when you have invalid code:

![Error Highlighting][error-underlines]

You can often mouse over these underlines to get information on the speific error in your code, or you can click the panel at the bottom of the screen (the one with a triangle and a circle with an 'x' in it) to see a list of all the errors in your code.

## Debugging
TODO.

## Settings
TODO.

## Extensions
TODO.

<!--- Images go here. --->
[welcome-screen]: img/welcome.png
[new-file]: img/new-file.png
[open-folder]: img/open-folder.png
[language-exts]: img/language-exts.png
[keymap-exts]: img/keymap-exts.png
[color-themes]: img/color-theme.png
[overlay]: img/overlay.png
[playground]: img/playground.png
[error-underlines]: img/error-underlines.png