---
title: UV Tile Discard
---

UV Tile Discard allows for part of a mesh to be _hidden_, allowing for example the use of multiple toggles on a single mesh.
![](/images/docs/avatar-optimization/uv-tile-discard/preview.gif "Preview of UV Tile Discard")

## Introduction

The most popular shaders used in VRChat support UV Tile Discard. Such as: [Poiyomi](https://www.poiyomi.com/special-fx/uv-tile-discard), [lilToon](https://lilxyzw.github.io/lilToon/), and [orels](https://shaders.orels.sh/docs/toon/uv-discard). It's a fast and optimized way to _hide_ part of a mesh. This way you can have multiple toggles without increasing draw call and material slot counts (if the mesh uses one material). However, UV Tile Discard can be quite confusing to set up at first.

## Setup Blender

{{% steps %}}

### Setup the `UV Editing` tab

Go to the `UV Editng` tab, then click the arrow next to the 2 circle looking thing. (It's on left window, on the top right-ish, if you have the default layout)

Then change the `Tiles` `X` and `Y` to 4. This will help to show what column and row vertices are in.
![](/images/docs/avatar-optimization/uv-tile-discard/step1.png)

### Creating a new UV Map

To avoid any rendering issues we'll be making a new `UV Map`. With an object selected, go to the `Data Properties` tab, and create a new `UV Map`. Be sure to give it a useful name, like `UV Tile Discard` or `UV1`.

> [!IMPORTANT]
> Take note of the order of the `UV Maps`, the shader in Unity won't have a friendly name like in blender. But instead it will have `UV0`, `UV1`, `UV2`, and `UV3`, in that order.

{{% details title="Example of ordering" closed="true" %}}

In the image below there are 3 UV Maps: `UVMap`, `UV Tile Discard`, and `Metal`. These would map like this:

| Name in blender   | Name in Unity |
| ----------------- | ------------- |
| `UVMap`           | `UV0`         |
| `UV Tile Discard` | `UV1`         |
| `Metal`           | `UV2`         |
|                   | `UV3`         |

{{% /details %}}

![](/images/docs/avatar-optimization/uv-tile-discard/step2.png)

### Moving part of mesh to a different tile

Select part of the mesh you want to make a different toggle. Then on the left window press `G`, then `X`, then `1` to move the selected mesh over by 1 tile. The same can be done in the `Y` axis and with multiple tile steps at once, just change `X` to `Y` and `1` to a number between `-3` and `3`.
![](/images/docs/avatar-optimization/uv-tile-discard/step3.png)

{{% /steps %}}

## Setup Unity

> [!NOTE]
> For this part of the guide we'll be using [Poiyomi](https://www.poiyomi.com/) shaders, but other shaders (should) work in a similar way.

{{% steps %}}

### Enable UV Tile Discard in your shader

Most shaders require you to enable `UV Tile Discard`. In `Poiyomi` this is under `Special FX`, then you should see a matrix like this.
![](/images/docs/avatar-optimization/uv-tile-discard/step4.png)

### Set the correct UV Map

By default this is set to `UV1` which should be fine. But you may need to change the `Discard UV` to the correct `UV Map`, check back on [Creating a new UV Map](#creating-a-new-uv-map) if you aren't sure what `UV Map` to choose.

### Creating toggles

You can animate each of these tiles alone like you would with any other toggle.

{{% details title="Example" closed="true" %}}

> [!NOTE]
> See why the `GameObject` gets enabled and disabled alone with the `UV Tile` [here](#extra-performance).

![](/images/docs/avatar-optimization/uv-tile-discard/step5.png "Toggle Off")
![](/images/docs/avatar-optimization/uv-tile-discard/step6.png "Toggle On")

{{% /details %}}

{{% /steps %}}

## Extra performance

> [!WARNING]
> This is something I (AwA) do, I've only tested this with Direct Blendtrees, not with the layer toggle method.
>
> From my limited amount of heavily edited and custom avatars, it does slightly improve performance in GPU limited scenarios. Although I encourage anyone to disprove or validate this approach with scientific testing.

If you hide the entire mesh with `UV Tile Discard`, it would also be good to disable the `GameObject`. This way the skinned mesh renderer doesn't need to also calculate the weights of a mesh that you won't see anyway.

To do this I simply enable and disable the `GameObject` along with the `UV Tile` I want to discard.
![](/images/docs/avatar-optimization/uv-tile-discard/step5.png "Toggle Off")
![](/images/docs/avatar-optimization/uv-tile-discard/step6.png "Toggle On")
