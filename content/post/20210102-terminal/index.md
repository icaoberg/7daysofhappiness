---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Life changing command"
subtitle: "Asked myself a dumb question and found an answer"
summary: "Asked myself a dumb question and found an answer"
authors: ["icaoberg"]
tags: ["blogging"]
categories: ["pet projects"]
date: 2021-01-02T11:22:18
lastmod: 2021-01-02T11:22:18
featured: true
draft: false
image:

  caption: "Daily Post"
  focal_point: "Smart"
  preview_only: true
---

![Gif](https://media0.giphy.com/media/u99fFT1YBzyco/giphy.gif?cid=ecf05e47zdopl412ugcvrvmblznmvc2g569peost0xscnjku&rid=giphy.gif)

Lately I have been doing some bash programming that creates or edits images with [ImageMagick](https://imagemagick.org/index.php). I run these very straightforward scripts on Terminal but you know, opening an image from Terminal is lame.

So I wondered, could I open Finder from Terminal at the current working directory. The answer was simple and life changing.

{{< code "python" >}}open .
{{< /code >}}
