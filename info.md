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
Visual Studio Code includes a built-in debugging tool that works with Node.js out of the box. This means that you can debug applications which run in node, including TypeScript and JavaScript applications, without having to set up any additional extensions.

To open the debugging panel, click the icon of a bug in the activity bar:

![Debugging Panel][debugging]

This panel will display a list of variables in the current scope (**Variables**), a list of expressions whose value will be calculated by the debugger (**Watch**), the current call stack of the program (**Call Stack**), and a list of breakpoints in your debugging environment (**Breakpoints**).

### Setup
Before you begin debugging, you should make sure you have an [extension](#extensions) installed for your language that includes debugging support. As an example, Microsoft publishes a [C/C++ extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) which includes support for popular debuggers such as gdb and lldb.

In order to debug your program, Visual Studio Code will need a configuration file detailing how to launch your program, the debugger to use, as well as other details about your debugging toolchain. In most cases, Visual Studio Code can generate this file for you.

To let Visual Studio Code generate its launch configuration, open the debugging panel and then click on the gear (it should have a small orange light on it):

![Tasks File][launch-setup]

This will try and generate a `launch.json` file in your project workspace with a default configuration that works with your toolkit.

For Go projects, the default file looks like this:

![Go launch.json][go-tasks]

You can further configure your launch task by adding configuration variables or changing those provided. As the default file mentions, you can use IntelliSense to find out about the different configuration values and what their functions are. You can also see descriptions of each configuration value by mousing over their entries in the configuration file.

One of the most important configuration values is the `"args"` entry. This configuration value is an array of command-line arguments you want to be passed to your program when this launch configuration is used.

For example, to debug `tar -x -z -f file.tgz`, you would set your `"args"` value to this:

```json
{
    ...
    "args": ["-x", "-z", "-f", "file.tgz"],
    ...
}
```

You can find more information on how to edit your launch configurations [here](https://code.visualstudio.com/docs/editor/debugging).

### Adding Breakpoints
In order to debug your program, you will likely want to add breakpoints at specific functions or lines in your code.

Visual Studio Code supports adding both conditional and unconditional breakpoints.

#### Unconditional Breakpoints
The easiest breakpoints to add are unconditional. To add unconditional breakpoints, you can do one of two things:
- Add the breakpoint at a specific line in code
- Add the breakpoint by specifying a function name

To add the breakpoint at a certain line of code, open the file you would like to add a breakpoint in, then click to the left of the line number:

![Adding an inline breakpoint][add-breakpoint]

To add the breakpoint at a specific function call, click the plus button in the debug panel next to **Breakpoints**, then enter in the name of the function:

![Adding a function breakpoint][function-breakpoint]

#### Conditional Breakpoints
This is a more advanced topic beyond the scope of this guide. You can find more information on how to add them [here](https://code.visualstudio.com/docs/editor/debugging#_advanced-breakpoint-topics).

### Running the Debugger
Once you've set up your [breakpoints](#breakpoints) and your [launch configuration](#setup), you can run the debugger by clicking the green arrow at the top of the debug panel.

This will run the program until it hits a breakpoint:

![Debugging Environment][debug-screen]

This screen provides options for stepping over, into, or out of routines, an option to restart, resume, or stop the execution of the program, as well as information on the context of the breakpoint on the right-hand side of the screen.

On the right-hand side of the screen, in the debugging panel, you can see a list of variables currently visible to the program, any **Watch** expressions you have created, and an overview of the call stack of the program.

The screen also includes a debugging console. The usage of this console is specific to your debugging environment, but you can learn more about it [here](https://code.visualstudio.com/docs/editor/debugging#_debug-console-repl).

### Other Debugging Topics
This serves as a very brief overview of the different tools Visual Studio Code offers for debugging. The official documentation offers information on advanced variable inspection, global launch configurations, and more. You can view the official debugging documentation [here](https://code.visualstudio.com/docs/editor/debugging).

## Settings
Visual Studio Code has a comprehensive set of settings for its editor, each of which can be configured on a global level or for a specific project. Additonally, all extension settings are stored in the same file, allowing for their settings to be configured per-workspace as well.

To open up your user settings, open the command pallete and type in "User Settings," then hit enter. When you type in the command pallete, Visual Studio Code will display the keyboard shortcut for opening settings on your platform.

Once you open user settings, you will be greeted by the following screen:

![User Settings][settings-screen]

The left portion of the screen is a list of settings, their default values, and descriptions of what the setting controls.

The right portion of the screen contains all of your personal settings as a JSON object. The user settings file supports IntelliSense, so you can hover over settings to see suggested and allowed values.

In addition, Visual Studio Code will underline a setting if you have given it an invalid value.

By clicking the pencil to the left of a setting, you can copy the setting to the right portion of the screen. From there, you can manually change the setting to your desired value.

The right portion of the screen also allows you to click a small pencil icon to the left of the setting's line to see a list of accpeted values for the setting and easily switch between them.

You may view the Visual Studio Code documentation on settings [here](https://code.visualstudio.com/docs/getstarted/settings).

### Language-specific Settings
In the above screen, you may have seen sections which looked like this:

```json
    "[javascript]": {
        "editor.tabSize": 2
    },
```

By placing settings inside of these entries, you can change settings only for a specific language. You can read more about this feature [here](https://code.visualstudio.com/docs/getstarted/settings#_language-specific-editor-settings).

### Workspace Settings
Workspace configuration files are identical in format to the user settings file, but are saved in your project root at `.vscode/settings.json`. You can access this file from the command pallete by searching for "Workspace Settings."

Settings placed in this file will only apply to your current project.

## Extensions
Visual Studio Code provides support for custom extensions that add new features to the editor. Recommending specific extensions is beyond the scope of this document, but this guide will explain the basics of installing and removing extensions.

To open the extensions panel, press <kbd>⌘</kbd>+<kbd>⇧</kbd>+<kbd>X</kbd> on Mac and <kbd>CTRL</kbd>+<kbd>⇧</kbd>+<kbd>X</kbd> on Windows and Linux:

![Extensions Panel][extensions-panel]

This will display a list of your installed extensions as well as a list of extensions recommended by Microsoft.

You can use the search bar at the top of the panel to look for new extensions in the marketplace.

To view a full-length description of an extension, simply click on the icon in the extension panel.

![Extension Description][extensions-description]

### Installing Extensions
Once you have found an extension, you may install it by pressing the "Install" button from the extension panel or the extension's description page.

This will automatically download and install the extension to your editor. Once it is installed, a small "Reload" button will replace the "Install" button. Clicking this button will reload the editor, enabling the extension immediately. If you do not press this button, the extension will not be enabled until the next time you restart the editor.

### Uninstalling Extensions
To remove an extension, type `@installed` into the search bar, followed (optionally) by the name of the extension you would like to remove.

![Installed Extensions][extensions-uninstall]

From here, you will see a list of your installed extensions. Clicking the gear for an extension then selecting the "Uninstall" option will remove the extension from your editor. You will need to reload your editor to fully uninstall the extension.

### Other Extension Topics
Visual Studio Code provides comprehensive documentation on how to manage extensions and information on how to write your own.

If you would like to learn more about extensions, visit [this](https://code.visualstudio.com/docs/editor/extension-gallery) part of the documentation.

To learn more about writing your own, visit [this](https://code.visualstudio.com/docs/extensions/overview) part of the documentation.

## Read More
The Visual Studio Code documentation is excellent and covers nearly all the uses of the editor. I would highly encourage reading through it to learn more about the editor.

Intrested in learning about a specific feature? I would look at its [version control](https://code.visualstudio.com/docs/editor/versioncontrol) or [integrated terminal](https://code.visualstudio.com/docs/editor/integrated-terminal) support.

## Copyright

This document and all images are copyright 2018 Tristen Allen.
This document and all images are licensed under the [Creative Commons Attribution License, 4.0](LICENSE).

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
[debugging]: img/debugging.png
[launch-setup]: img/launch-setup.png
[go-tasks]: img/go-tasks.png
[add-breakpoint]: img/add-breakpoint.png
[function-breakpoint]: img/function-breakpoint.png
[debug-screen]: img/debug-screen.png
[settings-screen]: img/settings.png
[extensions-panel]: img/extensions.png
[extensions-description]: img/exts-descript.png
[extensions-uninstall]: img/exts-uninstall.png
