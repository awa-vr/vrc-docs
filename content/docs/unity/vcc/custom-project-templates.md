---
title: Custom Project Templates
weight: 300
---

With [custom project templates](https://vcc.docs.vrchat.com/guides/using-project-template-repos) you can have a project with all the tools you use already installed when you create the project.
![](/images/docs/unity/vcc/custom-project-templates/preview.png)

## AwA's Avatar Template

Of course I have a custom template with the tools I always use (most of the tools in [Useful Repos and Tools](../useful-repos)). You can find it [here](https://github.com/awa-vr/VCC-templates). You can edit it freely, or just use as is.

### Install

{{% steps %}}

### Download

Download the [latest release package](https://github.com/awa-vr/VCC-templates/releases/latest). `Source code (zip)`
![](/images/docs/unity/vcc/custom-project-templates/step1.png)

### Move files

Unzip the `.zip`. Press `Win + R` and paste `%LocalAppData%\VRChatCreatorCompanion`, or open explorer and paste it in the path input. This will open a new window. Create a new folder called `Templates` and move all the files inside of it.

The folder should look like this when you're done. (don't worry if you don't see the `.git` folder)
![](/images/docs/unity/vcc/custom-project-templates/step2.png)

### Add repos to VCC

`https://awa-vr.github.io/vrc-tools-vpm/index.json`

<a class="button-link" href="vcc://vpm/addRepo?url=https://awa-vr.github.io/vrc-tools-vpm/index.json">Add repo</a>

`https://rurre.github.io/vpm/index.json`

<a class="button-link" href="vcc://vpm/addRepo?url=https://rurre.github.io/vpm/index.json">Add repo</a>

`https://whiteflare.github.io/vpm-repos/vpm.json`

<a class="button-link" href="vcc://vpm/addRepo?url=https://whiteflare.github.io/vpm-repos/vpm.json">Add repo</a>

`https://vpm.thry.dev/index.json`

<a class="button-link" href="vcc://vpm/addRepo?url=https://vpm.thry.dev/index.json">Add repo</a>

`https://vpm.razgriz.one/index.json`

<a class="button-link" href="vcc://vpm/addRepo?url=https://vpm.razgriz.one/index.json">Add repo</a>

`https://vcc.vrcfury.com`

<a class="button-link" href="vcc://vpm/addRepo?url=https://vcc.vrcfury.com">Add repo</a>

`https://poiyomi.github.io/vpm/index.json`

<a class="button-link" href="vcc://vpm/addRepo?url=https://poiyomi.github.io/vpm/index.json">Add repo</a>

`https://gabsith.github.io/GabSith-VCC-Listing/index.json`

<a class="button-link" href="vcc://vpm/addRepo?url=https://gabsith.github.io/GabSith-VCC-Listing/index.json">Add repo</a>

> [!NOTE]
> You also need to add Adjerry's Face Tracking Repo to use the FT template.
>
> `https://adjerry91.github.io/VRCFaceTracking-Templates/index.json`
> 
> <a class="button-link" href="vcc://vpm/addRepo?url=https://adjerry91.github.io/VRCFaceTracking-Templates/index.json">Add repo</a>

> [!TIP]
> Check out the [Adding a repo to VCC](../adding-repo-to-vcc) guide if the `Add Repo` button doesn't work.

{{% /steps %}}
