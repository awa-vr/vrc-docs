---
title: Presets
# prev: docs/_index
weight: 2
---

Creating presets for your avatar is really easy, but a bit time-consuming. Using [VRChat's Avatar Parameter Driver](https://creators.vrchat.com/avatars/state-behaviors/#avatar-parameter-driver) you can change parameter's values in an animation state. This method uses 1 layer in your FX controller and no network synced parameters (assuming the things you want to change with the preset are synced).

## Setup

{{% steps %}}

### Adding a presets layer

To start we have create a new layer in your avatar's FX layer. Name it something useful like `Presets` and make sure the weight is set to 1. (Don't worry about `write defaults`, it doesn't really matter for this.)
![](/images/docs/presets/step1.png)

### Create an empty state

In this layer and add a new empty state `'right click' > Create State > Empty`.

### Add an empty clip to the animation state

After that create a new animation and call it something like `EmptyClip`, that's all, make sure it's completely empty (you may already have this if you're editing an avatar, or have the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) package installed).

### Name the empty animation state

Now select the empty state you made in [step 2](#create-an-empty-state), give it a name (for example `Idle`), and set `motion` to the `EmptyClip` you made in [step 3](#add-an-empty-clip-to-the-animation-state) (or the empty clip the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) package provides).

It should look like this when you're done.
![](/images/docs/presets/step2.png)

{{% /steps %}}

## Adding a preset

> [!NOTE]
> You can add multiple presets all in the same layer.

## FX controller

{{% steps %}}

### Create parameter

Go to your avatar's Expression Parameters, and add a new `bool` parameter, disable both `saved` and `syned`, and set the default value to `false`.
Next in your FX controller add a new `bool` parameter, and give it the same name as the parameter you made before.

### Create a new animation state

In the `Presets` layer you made in [Setup](#setup), add a new empty state. Set the motion as `EmptyClip`. And give it a useful name (your parameter name works great for this).
![](/images/docs/presets/step3.png)

### Create transitions

Create a transition from the state you just made to the `Idle` state, and one from `Idle` to the state you just made. (`'right click on state' > Make Transition > 'click on the other state'`).

Next click on the transition going from the state you made to `Idle`, add a condition with the parameter you made in [Create parameter](#create-parameter), and set it to `false`. Now do the same going from `Idle` to the state you made, but with `true` instead of `false`.

Here's an example of how the transition going from the state you made to `Idle` should look like:
![](/images/docs/presets/step4.png)

### Add VRC Parameter Driver

Click on the state you made, and add a behaviour of `VRCAvatarParameterDriver`.
Next click `add`, leave `Type` as `Set`, select the parameter you want to change under `Destination`, and lastly set the `Value`.

### Add all the parameters you want to change

Repeat [Add VRC Parameter Driver](#add-vrc-parameter-driver) for all the parameters you want to change.

### Finish the preset

As **the last parameter** you change, set it to the parameter you made for the preset, and set the value to `false`. **This is very important**, otherwise you can only change to a preset once and can't use any other presets until you reload your avatar, or change worlds.

![](/images/docs/presets/step5.png)

{{% /steps %}}

## Menu

{{% steps %}}

### Create a toggle
Create a new expression (I recommend you use a subfolder for all the presets). Next set the `Type` to `Button`. Finally, set the parameter to the preset's parameter.

![](/images/docs/presets/step6.png)

{{% /steps %}}
