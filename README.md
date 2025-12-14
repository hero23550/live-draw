# LiveDraw

A tool that allows you to draw on screen in real-time.

## Why?

When you need to draw or mark something while presenting, you may use some tools like
[Windows Ink Workspace](https://blogs.windows.com/windowsexperience/2016/10/10/windows-10-tip-getting-started-with-the-windows-ink-workspace/),
but all of them are actually **taking a screenshot** and allow you to draw on it.
That's actually annoying when you want to present something dynamic.

However, **LiveDraw is here and built for it!**

## Interface

![Compact mode](screenshots/00.png)

![Actionshot with Blender](screenshots/01.png)

![Actionshot](screenshots/02.png)

## Usage

The shortcuts that can be used:

- [ Z ] Undo, [ Y ]  Redo,
- [ E ] Eraser By Stroke, [ D ]  Eraser By Point,
- [ R ] Release or Recover interface, (This now also toggles the global listenting of your hotkeys. For eg when drawing is toggled to be OFF, other shortcuts except this      are no longer listened, allowing you to use them when not using this program. Toggle drawing to ON to once again enable the listening of other shortcuts!)
- [ + ] Increase size brush, [ - ]  Decrease size brush
- [ B ] Brush mode, [ L ]  Line Mode
- [ C ] Clear

### About this fork

This was forked from [Insire/live-draw](https://github.com/Insire/live-draw) which is also a fork of [antfu/live-draw](https://github.com/antfu/live-draw) . Here is the things i changed:

- Downloadable artifact available in actions category.
- The latest artifact has some QOL fixes to keybind to fix the issues of preventing them from working when the window unfocuses.
  credit to [Sleepylux](https://github.com/Sleepylux) for the [code](https://github.com/antfu/live-draw/issues/52)

### Requirements

- a supported [Windows OS](https://learn.microsoft.com/en-us/windows/release-health/supported-versions-windows-client)
- [.NET 9 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/9.0)

#### Download?

If you want to download an unsigned exe you can do so from the actions category of this repository. 

### Features

- True transparent background (you can draw freely even when you are watching videos).
- Select colors by simply clicks.
- Adjust the size of brush.
- Draw ink with pressure (when using a pen with pen pressure).
- Auto smooth ink.
- Mini mode.
- Unlimited undo/redo.
- Freely drag the palette.
- Save and load ink to file (binary file) with color.
- Temporarily disable draw then you can be able to operate other windows.
- Fully animated.
- Keyboard Shortcuts.

## Publish

### For others to use

(embeds the .NET runtime in the exe file and makes the exe file about 100MB larger, but will basically make it work on any [supported Windows OS](https://learn.microsoft.com/en-us/windows/release-health/supported-versions-windows-client))

- dotnet publish -c Release -r win-x86 --self-contained true -p:PublishSingleFile=true -p:IncludeAllContentForSelfExtract=true
- dotnet publish -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -p:IncludeAllContentForSelfExtract=true

### For yourself

(makes the exe file about 1MB large, but requires the [.NET runtime](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) to be installed)

- dotnet publish -c Release -r win-x68 --self-contained false -p:PublishSingleFile=true
- dotnet publish -c Release -r win-x64 --self-contained false -p:PublishSingleFile=true

## License

MIT
