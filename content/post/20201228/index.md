---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Updating Singularity recipes"
subtitle: "Publishing to GitHub"
summary: "I am uploading my recipes, scripts and images to GitHub"
authors: ["icaoberg"]
tags: ["blogging"]
categories: ["programming"]
date: 2020-12-28T23:14:13
lastmod: 2020-12-28T23:14:13
featured: true
draft: false
image:

  caption: "Daily Post"
  focal_point: "Smart"
  preview_only: true
---

I am a huge fan of Singularity to deploy software on HPC clusters. But lately I have been playing around with Spack. Spack is amazing as well, but sometimes Singularity works better for legacy software or software that has the potential to become legacy.

However Spack has the potential to allow us to build and deploy nontraditional software on an HPC cluster. For example, I use many simple tools to generate reports. With Singularity I use

* [chalk-animation](https://github.com/icaoberg/singularity-chalk-animation)
* [chalk-cli](https://github.com/icaoberg/singularity-chalk-cli)
* [lazygit](https://github.com/icaoberg/singularity-lazygit)
* [mc](https://github.com/icaoberg/singularity-mc)

However I found it easier to deploy the following in Spack

* [boxen](https://github.com/sindresorhus/boxen-cli)
* [sparkly-cli](https://github.com/sindresorhus/sparkly-cli)
* [gitmoji](https://github.com/carloscuesta/gitmoji-cli)
* [is-up-cli](https://github.com/sindresorhus/is-up-cli)
* [carbon-now-cli](https://github.com/mixn/carbon-now-cli)
* [is-online-cli](https://github.com/sindresorhus/is-online-cli)

or with the help of the above

* [glow](https://github.com/charmbracelet/glow)

Spack is really powerful as long as the compilers you require are already present (in case you do not have admin access to install or update software that lives outside of the Spack install).
