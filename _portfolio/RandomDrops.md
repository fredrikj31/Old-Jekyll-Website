---
title: "Random Drops - Minecraft Plugin"
header:
  teaser: "https://bugs.mojang.com/secure/attachment/33980/2013-06-28_21.27.55.png"

toc: true
toc_label: "My Table of Contents"
toc_icon: "cog"

tags:
  - Java
  - Spigot
---

Random Drops, is a Minecraft plugin I made a afternoon in the weekend. I wanted to see how it felt to program Minecraft plugins, and how a random drop plugin would be in Minecraft.

So I created a local Minecraft server to host the plugin, and I started programming it. It didn't take as long as I expected, as the Minecraft items, was held in a list. So I used a random number generator, to generate a number between 0 and the length of the list with the items in, and afterwards give the item to the player, that broke the block.