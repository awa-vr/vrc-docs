---
title: Testing
type: docs
prev: docs/avatar-optimization
next: docs/avatar-optimization/skinned-meshes
weight: 1000
---

> [!CAUTION]
> Work In Progress

Testing an avatar's performance can be hard inside of VRChat, so we're gonna do it in the unity editor. This isn't perfect for a few reasons, but at least we'll have a consistent place to test without having to worry about VRChat updates.

## How to test
In unity's game view is a handy button `stats`, this gives you all the realtime info over the performance like FPS, CPU frame time, GPU frame time, batches, skinned meshes, and so on.

When testing you should be using something like [Gesture Manager](https://github.com/BlackStartx/VRC-Gesture-Manager), this is so the animators run, and performance you see in unity somewhat reflects the performance in VRChat.

Testing performance should ideally be done when having all the same programs open, so don't just one time have VRChat running in the background and another time not.
