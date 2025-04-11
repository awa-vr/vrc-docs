---
title: Stencil
---

Stencils allow you to paint an image onto a texture on an object.
![](/images/docs/blender/texture-painting/stencil/preview.gif)

## Setup

{{% steps %}}

### Object's material and UV map

Make sure you have an image in the object's material you want to put a stencil on. Next make sure the object you want to paint on has a good unwarped UV map.

### Creating a new brush
Go to the `Texture Paint` tab, and add a new brush.
   ![](/images/docs/blender/texture-painting/stencil/step1.png)

### Setting up the brush
Select the newly added brush (Maybe also give this brush a useful name), and change the texture mapping from `View Plane` to `Stencil`.
   ![](/images/docs/blender/texture-painting/stencil/step2.png)

### Add a texture
Add a new texture to the brush.
   ![](/images/docs/blender/texture-painting/stencil/step3.png)
Now open the texture tab and open your desired texture.
   ![](/images/docs/blender/texture-painting/stencil/step4.png)
   {{% /steps %}}

## Movement

| Shortcut                | Description        |
| ----------------------- | ------------------ |
| `<right-click>`         | Move the stencil   |
| `Shift + <right-click>` | Scale the stencil  |
| `Ctrl + <right-click>`  | Rotate the stencil |

## Painting

To paint just paint like you normally would. All settings like `Symmetry` also work the same with stencils.

> [!TIP]
> Set the brush falloff to 1 over the entire brush radius.
> ![](/images/docs/blender/texture-painting/stencil/step5.png)
