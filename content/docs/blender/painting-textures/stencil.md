---
title: Stencil
---

## Introduction

Stencils allow you to paint an image onto a texture on an object.
![](/images/docs/blender/texture-painting/stencil/preview.gif)

## Setup

1. Make sure you have an image in the object's material you want to put a stencil on.
2. Make sure the object you want to paint on has a good unwarped UV map.
3. Go to the `Texture Paint` tab.
4. Add a new brush.
   ![](/images/docs/blender/texture-painting/stencil/step1.png)
5. Select the newly added brush. (Maybe also give this brush a useful name)
6. Change the texture mapping from `View Plane` to `Stencil`.
   ![](/images/docs/blender/texture-painting/stencil/step2.png)
7. Add a new texture to the brush.
   ![](/images/docs/blender/texture-painting/stencil/step3.png)
8. Open the texture tab and open your desired texture.
   ![](/images/docs/blender/texture-painting/stencil/step4.png)

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
