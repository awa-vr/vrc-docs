---
title: Texture Size
---

A big part of avatar download and VRAM sizes are textures. Reducing the size and/or quality of these textures can drastically decrease your avatar's download/upload and VRAM sizes. Although this can be a bit annoying and tedious.

## Introduction

Although you can just use the import setting directly in unity to change texture size and quality texture by texture, this gets annoying quite fast. Something like [Thry's Avatar Performance Tools](https://github.com/Thryrallo/VRC-Avatar-Performance-Tools) can definitely help narrow down the big ones, but it's still slow.
I recommend using `Avatar Texture Tool` from [Whiteflare's Avatar Tools](https://github.com/whiteflare/AvatarTools).

## Setup

1. Add `https://whiteflare.github.io/vpm-repos/vpm.json` to VCC.

## Usage
1. To open the `Avatar Texture Tool` go to `Tools > whiteflare > Avatar Texture Tool` in the top bar, this will open a new window.
2. Now select your avatar, the easiest way to do is by dragging your avatar into the `Root object` slot. Or by clicking the little target thing and searching for your avatar.

You should now see something like this:
![](/images/docs/avatar-optimization/texture-size/step1.png)
It may look like a lot but don't worry I'll explain the most important and useful ones.

- <span style="color:red;">Texture Name</span>: Name as in your assets files
- <span style="color:mediumspringgreen;">VRAM</span>: Amount of VRAM used by the texture, this depends on the size and quality settings of the texture
- <span style="color:cornflowerblue;">Size</span>: Size of the texture that will be used by the avatar (This won't affect the size of the source texture)
- <span style="color:blueviolet;">Compression/Quality</span>: How good the compression is, lower compression usually means smaller size but at receded visual quality (Think about for example YouTube compression)
- <span style="color:gold;">Total Texture VRAM</span>: The total VRAM used by textures, this is also the statistic VRChat shows as `Texture Memory`. (Note: This is **not** the total amount of VRAM used by an avatar, meshes and other things also use VRAM, but generally to a lesser extent)