---
title: Savable Presets
---

Quickly creator or update an animator controller that can save presets in-game.

![](/images/vpm-tools/savable-presets/window.png "Main Window")

## What does it do?

Makes it quick for you to create and update an animator that allows for saving and loading custom presets in-game.

## How to use

### First set-up

When first using the tool you will need to create a new configuration. There are 2 ways to do this:

1. Right-click in a folder `Create/AwA/Savable Preset Configuration`
2. Click the button, this will put it in the `Assets` folder

![](/images/vpm-tools/savable-presets/first-setup.png "First Setup")

### Creating a menu

> [!NOTE]
> For now you will need to create your own menus for this. In the future there may be a way to also auto generate menus for the given presets.

To make it easier there are 3 buttons under each Savable Preset: `Load`, `Reset`, and `Save`. These will copy the parameter to your clipboard for that given Savable Preset.

Below is an example of how to create a menu:

![](/images/vpm-tools/savable-presets/custom-preset-main.png "Main Menu")
![](/images/vpm-tools/savable-presets/custom-preset-toggle.png "Toggle Example")

*The `Reset` button is a submenu with a confirm button inside.*

### Merging the animator

> [!NOTE]
> This will use [VRCFury](https://vrcfury.com/), but [Modular Avatar](https://modular-avatar.nadena.dev/) has a similar tool.

1. Create a new Empty GameObject
2. Make sure it's under your root avatar GameObject
3. Add a `Full Controller` component to that GameObject
4. Add the generated controller, and set the `Type` to `FX`
5. Add all your menus
6. Add the generated Parameters Expressions
7. In `Advanced Options` add a global parameter with the value of `*`
8. *(Optional) Add custom icon overrides for the menus*

![](/images/vpm-tools/savable-presets/full-controller.png "Full Controller Example")