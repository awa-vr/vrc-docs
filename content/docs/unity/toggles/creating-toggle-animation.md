---
title: Creating Toggle Animation
---

## Setup

To begin it is recommended to have your `FX Animator` in your avatar's `Animator`.

{{% steps %}}

### Open your FX Animator

Click on your avatar, you should see a `VRC Avatar Descriptor` component somewhere in the `Inspector`. Then find your `FX Animator` by searching in `VRC Avatar Descriptor > Playable Layers > FX`. You can double-click to open it, or single-click to highlight it in your `Project` window.
![](/images/docs/unity/general/find-fx-layer.png)

### Set the Animator Controller

By default your avatar should have an `Animator` component, but sometimes the `Controller` is set to another `Animator Controller` than your `FX Animator`.

Set the `Controller` in the `Animator` component on your avatar to the avatar's `FX Animator`.
![](/images/docs/unity/toggles/creating-toggle-animation/step1.png)

{{% /steps %}}

## Open the Animation Window

If you don't see the `Animation` window yet, open it.

In the top bar go to `Window > Animation > Animation` to open a new `Animation` window. (you can also press the shortcut `Ctrl + 6`)
![](/images/docs/unity/toggles/creating-toggle-animation/step2.png)

## Creating a new animation

{{% steps %}}

### Select your avatar

If you did the steps above, you should see the `Animation` window change, and maybe there will be an animation selected by default.
![](/images/docs/unity/toggles/creating-toggle-animation/step3.png "Example of Animation Window")

### Create a new animation

Click on the highlighted drop-down, a new list should pop up with all the animations on your avatar. Then click `Create New Clip...` button on the bottom of the list.

> [!TIP]
> If you don't see the `Create New Clip...` button on the bottom of the list, it's probably because there are too many animations, and you need to scroll down. Fastest way I found to do this is by putting your mouse cursor at the first animation, then pressing `arrow-up` up your keyboard.

![](/images/docs/unity/toggles/creating-toggle-animation/step4.png)

### Saving the animation

Once you press the `Create New Clip...` button a new window will pop up asking where to save it. You can save it anywhere in your project's `Assets` folder, but I suggest using an `Animations` folder inside your `Assets` folder.

> [!CAUTION]
> **Don't** create a new folder inside this window and then save an animation inside it. This will most likely break your entire unity project.

![](/images/docs/unity/toggles/creating-toggle-animation/step5.png)

### Creating keyframes

`Keyframes` are thing that says what an `Animation` does. For example, turning a `GameObject` on and off, changing the Hue Shift of a material, etc. They can be used to animate basically anything on your avatar.

To create a new `keyframe` click on the object you want to toggle, then press the `record` button. This will now automatically create `keyframes` for everything you toggle or change on an avatar, so be careful to not accidentally touch anything you don't want to change.
![](/images/docs/unity/toggles/creating-toggle-animation/step6.png)

Now enable and/or disable your `GameObject` to create a new `keyframe`. You can always change the value of the `keyframe` by clicking the checkbox next to the name. Or remove a `keyframe` by right-clicking on the name, and then `Remove Property`.
![](/images/docs/unity/toggles/creating-toggle-animation/step7.png)

### Create the inverse

Now that you have an `On` or `Off` `Animation`, create an inverse of what you just did. So if you made an `On` animation, now create an `Off` animation, and vise versa.

To do this follow the steps from [Create a new animation](#create-a-new-animation) down.

{{% /steps %}}

## Creating the toggle

To create the toggle, check out the [Toggles](..) page.
