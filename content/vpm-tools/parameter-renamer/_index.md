---
title: Parameter Renamer
---

Quickly rename a parameter everywhere. (menus, parameters, controllers, contacts, etc.)

![](/images/vpm-tools/parameter-renamer/window.png "Main Window")

# What does it do?

This tool aims to rename a given parameter everywhere for a given avatar, this includes:
- All menus
- Parameter Expressions linked to the avatar
- All animators linked to the avatar
    - Parameters
    - All state transitions
    - All [VRC Animator Play Audio](https://creators.vrchat.com/avatars/state-behaviors/#animator-play-audio) components
    - All [VRC Parameter Drivers](https://creators.vrchat.com/avatars/state-behaviors/#avatar-parameter-driver)
    - In all state machines and sub-state machines
- All [Contacts](https://creators.vrchat.com/common-components/contacts) on the avatar GameObject

> [!CAUTION]
> This tool does **not rename physbone parameters**. You will have to do this manually.

> [!NOTE]
> This tool has great integration with [Preset Creator](../preset-creator/) and [VRC SDK+](../vrc-sdkplus/).

# How to use

0. Select an Avatar Descriptor if it didn't select automatically
1. Select the parameter you want to rename
2. Fill in a new name
3. Rename

> [!TIP]
> You can view all menus a parameter occurs in by first selecting the parameter, then clicking `Show menu name(s)`