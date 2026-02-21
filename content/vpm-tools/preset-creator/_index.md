---
title: Preset Creator
---

Quickly create, edit or remove presets for an avatar.

![](/images/vpm-tools/preset-creator/window.png "Main Window")

## How to use

### First time set-up

When first using the tool on an avatar you will be asked to run the first set-up.

This will create a new layer called `AwA - Presets - DO NOT TOUCH`. **Do not delete, or change the name** of this layer, this will break the tool.

### Creating a new preset

1. Click on the `New` button
2. Fill in a fitting name, you can change this later if you have [Parameter Renamer](../parameter-renamer/) installed
3. *(Optional) You can enable or disable **Write Defaults**. This doesn't affect the presets, but will shut up vrcfury and the VRC SDK for having mixed Write Defaults*
4. Add the new preset

> [!IMPORTANT]
> You will need to manually create a menu and assign a toggle to this. For more info see [Adding to a menu](#adding-to-a-menu)

### Updating a preset

1. Select the preset you want to update
2. Set the values you want for that preset
    - `Change`: Will say if that preset should change that parameter to the specified value, if off the preset will leave that parameter alone
    - `Value`: The value the parameter should change to when using the preset
3. When you're done click `Update`

### Deleting a preset

1. Select the preset you want to delete
2. Click the `Delete` button

> [!WARNING]
> This will not touch the menus of the avatar, you will have to delete the presets manually in the menus.

### Rename a preset

> [!IMPORTANT]
> This requires [Parameter Renamer](../parameter-renamer/) to be installed.

1. Select the preset you want to rename
2. Give it a new name

## Adding to a menu

1. Select or create a new menu
2. Create a new Toggle
3. Assign the Parameter to the chosen parameter *(All presets are in this format `Presets/<preset name>`)*

![](/images/vpm-tools/preset-creator/toggle.png "Example Toggle")