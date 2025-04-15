---
title: Direct Blend Tree
---

`Direct Blend Trees` allow for more performant toggles than `Layers` for lots of toggles.

## Setup a new blend tree

{{% steps %}}

### Create a new layer

Open your `FX Animator`, then click the `+` button to create a new layer. Give it a useful name, like `Blendtree`. And lastly make sure the `Weight` is set to 1.

![](/images/docs/unity/toggles/direct-blend-tree/step2.png)

> [!TIP]
> If you don't know where to find your `FX animator`, click on your avatar, you should see a `VRC Avatar Descriptor` component somewhere in the `Inspector`. Then find your `FX Animator` by searching in `VRC Avatar Descriptor > Playable Layers > FX`. You can double-click to open it, or single-click to highlight it in your `Project` window.
> ![](/images/docs/unity/general/find-fx-layer.png)

### Add a blend tree to the new layer

Create a new blend tree by right-clicking an empty area then `Create State > From New Blend Tree`.
![](/images/docs/unity/toggles/direct-blend-tree/step3.png)

### Enabling Write Defaults

> [!CAUTION]
> Without `Write Defaults` the blend tree toggles will **not** work as expected.

Click on the blend tree you just made. In the `Inspector` enable `Write Defaults`.
![](/images/docs/unity/toggles/direct-blend-tree/step4.png)

### Open the blend tree

Open the blend tree by double-clicking on it.

### Change the default blend type

> [!CAUTION]
> Setting the correct `Blend Type` is crucial for `Direct Blend Trees` to work.

Select the blend tree if it isn't selected already. Then change the `Blend Type` from `1D` to `Direct`.
![](/images/docs/unity/toggles/direct-blend-tree/step5.png)

### Add Weight parameter

Create a new parameter by going to the `Parameter` tab in your `FX Animator`, clicking the `+` button and selecting `Float`. Name it `Weight`, and set its value to `1`. You **don't** need to add it to your `VRC Expressions Parameters`.
![](/images/docs/unity/toggles/direct-blend-tree/step6.png)

> [!TIP]
> Move the `Weight` parameter to the top of the parameter list by dragging on the 2 horizontal lines left to the parameter name. This way the `Weight` parameter will be automatically selected, so you don't always need to manually select it while making toggles.

{{% /steps %}}

## Adding a toggle

> [!NOTE]
> This assumes you already have separate On/Off animations. If not check out [Creating Toggle Animation](../creating-toggle-animation).

{{% steps %}}

### Add a new parameter

Add a new float `parameter` to your `FX Animator`, like in [Step 6 - Add Weight parameter](#add-weight-parameter), but give it a useful name like `Toggles/Tail`. Now also add a parameter to your avatar's `VRC Expressions Parameters` with the same name as the `parameter` you made in the `FX Animator`, make it `Saved` and `Synced`, but as the `Type` instead of `float` make it `bool`.

> [!TIP]
> If you don't know where to find your `VRC Expressions Parameters`, click on your avatar, you should see a `VRC Avatar Descriptor` component somewhere in the `Inspector`. Then find your `VRC Expressions Parameters` by searching in `VRC Avatar Descriptor > Expressions > Parameters`. You can double-click to open it, or single-click to highlight it in your `Project` window.
> ![](/images/docs/unity/general/find-vrc-expressions-parameters.png)

> [!TIP]
> Naming your `parameter` with a `/` in it will separate it when trying to search for your `parameter`.
> ![](/images/docs/unity/toggles/direct-blend-tree/step7.png)

> [!NOTE]
> VRChat will automatically convert `bools` to `floats`, this way a single synced toggle will only use 1 synced parameter slots.

### Add a new blend tree

Open the `blend tree` you want your toggle to be in. `Blend trees` can have `blend trees` inside of them, allowing for you to blend between 2 animation.

In your `blend tree`, click on the `+` button then `New Blend Tree`.
![](/images/docs/unity/toggles/direct-blend-tree/step8.png)

Make sure the `Parameter` of this is set to the `Weight` parameter you made in [Step 6 - Add Weight parameter](#add-weight-parameter).
![](/images/docs/unity/toggles/direct-blend-tree/step9.png)

### Creating the toggle logic

Open the `blend tree` you just made, give a useful name like your toggle's name. Set the `Parameter` to your toggle's parameter. And add 2 `Motion Fields`.
![](/images/docs/unity/toggles/direct-blend-tree/step10.png)

Now in these 2 `Motion Fields` add your `Off` and `On` animations.
![](/images/docs/unity/toggles/direct-blend-tree/step11.png)

### Add to menu

Open your `Menu` you want to toggle to be in. Create a new toggle, name it, and set the `Parameter` to your toggle's parameter.
![](/images/docs/unity/toggles/direct-blend-tree/step12.png)

{{% /steps %}}

## Tips

### Disable Physbones

> [!TIP]
> Disable the `GameObjects` Physbones if it has any, like for example Tail, Ears, etc.
> ![](/images/docs/unity/toggles/direct-blend-tree/step13.png)
