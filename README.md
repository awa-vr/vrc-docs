# VRC Docs

This is the source code for my VRChat docs/guide site.

🔗 Site: [https://awa-vr.github.io/vrc-docs/](https://awa-vr.github.io/vrc-docs/)

# Contributing

There are no Contributing Guidelines for now. But if you want to contribute be sure it's in a similar style of the rest of the site.

# Development

This project uses the [Hextra theme](https://github.com/imfing/hextra) for [HUGO](https://gohugo.io/).

Pre-requisites: [HUGO](https://gohugo.io/getting-started/installing/), [Go](https://golang.org/doc/install), [Git](https://git-scm.com/)

```shell
# Clone the repo
git clone https://github.com/awa-vr/vrc-docs

# Change directory
cd vrc-docs

# Start the server
hugo mod tidy
hugo server --logLevel debug --disableFastRender -p 1313
```
