---
title: Presets
# prev: docs/_index
next: docs/avatar-optimization/_index
weight: 2
---

Creating presets for your avatar is really easy, but a bit time-consuming. Using [VRChat's Avatar Parameter Driver](https://creators.vrchat.com/avatars/state-behaviors/#avatar-parameter-driver) you can change parameter's values in an animation state. This method uses 1 layer in your FX controller and no network synced parameters (assuming the things you want to change with the preset are synced).

## Setup
1. To start we have create a new layer in your avatar's FX layer. Name it something useful like `Presets` and make sure the weight is set to 1. (Don't worry about `write defaults`, it doesn't really matter for this.)
![](/images/docs/presets/step1.png)

2. In this layer and add a new empty state `'right click' > Create State > Empty`.
3. After that create a new animation and call it something like `EmptyClip`, that's all, make sure it's completely empty (you may already have this if you're editing an avatar, or have the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) package installed).
4. Now select the empty state you made in step 2, give it a name (for example `Idle`), and set `motion` to the `EmptyClip` you made in step 3 (or the empty clip the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) package provides).

It should look like this when you're done.
![](/images/docs/presets/step2.png)

## Adding a preset
{{< callout type="info" >}}
You can add multiple presets all in the same layer.
{{< /callout >}}

### FX controller
1. Go to your avatar's Expression Parameters, and add a new `bool` parameter, disable both `saved` and `syned`, and set the default value to `false`.
2. In your FX controller add a new `bool` parameter, and give it the same name as the parameter you made in step 1.
3. In the `Presets` layer you made in [Setup](#setup), add a new empty state. Set the motion as `EmptyClip`. And give it a useful name (your parameter name works great for this).
![](/images/docs/presets/step3.png)

4. Create a transition from the state you just made to the `Idle` state, and one from `Idle` to the state you just made. (`'right click on state' > Make Transition > 'click on the other state'`)
5. Click on the transition going from the state you made to `Idle`, add a condition with the parameter you made in step 1 and 2, and set it to `false`. Now do the same going from `Idle` to the state you made, but with `true` instead of `false`.

Here's an example of how the transition going from the state you made to `Idle` should look like:
![](/images/docs/presets/step4.png)

6. Click on the state you made, and add a behaviour of `VRCAvatarParameterDriver`.
7. Click `add`, leave `Type` as `Set`, select the parameter you want to change under `Destination`, and lastly set the `Value`.
8. Repeat step 7 for all the parameters you want to change.
9. As **the last parameter** you change, set it to the parameter you made for the preset, and set the value to `false`. **This is very important**, otherwise you can only change to a preset once and can't use any other presets until you reload.

![](/images/docs/presets/step5.png)

### Menu
1. Create a new expression (I recommend you use a subfolder for all the presets).
2. Set the `Type` to `Button`.
3. Set the parameter to the preset parameter.

![](/images/docs/presets/step6.png)