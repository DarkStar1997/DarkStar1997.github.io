---
layout: post
title: Optimizing Dota 2 Performance on Linux with Vulkan on NVIDIA Graphics Cards
tags: [Gaming, Dota, Vulkan, NVIDIA]
---


Gaming on the **Linux** platform is extremely underrated and is often completely *rejected* by most gamers when it comes to high-FPS gaming. In this blog, I will present a stark contrast to the above idea. The game of [Dota 2](https://www.dota2.com/play/) does not need any introduction, and being a Linux enthusiast and a Dota addict, I'd love to share a few simple tips on optimizing Dota 2 performance on Linux.

*Spoilers:* As I will demonstrate, after following the steps given in this blog you should have a significantly higher FPS compared to Dota running on Windows on identical hardware (about 30-40 FPS, depending on your graphics card).

##	Requirements

*	NVIDIA Graphics card with Vulkan support and a Linux Distro
*	Your graphics drivers are updated and working correctly
*	I'll assume that you have got [Steam](https://store.steampowered.com/) installed with [Dota 2](https://www.dota2.com/play/) up and running.

##	Let's Get to the Real Business

As stated in the title, we will be needing [Vulkan](https://www.khronos.org/vulkan/). At the time of writing, my NVIDIA Driver version is 430.26 running on *Arch Linux* as shown below:

![nvidia config](https://imgur.com/Ot33yen.png)

To install the NVIDIA graphics drivers and Vulkan support, please find the installation instructions for your respective distro. If you are running Arch Linux, you can install the latest nvidia graphics drivers and vulkan support with the command `sudo pacman -S nvidia-dkms vulkan-icd-loader`. What makes the 430 driver special is that, it received notable performance improvements for [Vulkan](https://www.khronos.org/vulkan/). The installation of [Steam](https://store.steampowered.com/) is also straightforward for most distros. If you are on Arch, follow [these](https://wiki.archlinux.org/index.php/Steam) instructions to install [Steam](https://store.steampowered.com/). In my experience, you might need [nvidia-utils](https://www.archlinux.org/packages/extra/x86_64/nvidia-utils/) and [lib32-nvidia-utils](https://www.archlinux.org/packages/multilib/x86_64/lib32-nvidia-utils/) to get [Steam](https://store.steampowered.com/) running. With [Steam](https://store.steampowered.com/) up and running, installing and running [Dota 2](https://www.dota2.com/play/) should be a piece of cake. To monitor your FPS turn on the [Steam](https://store.steampowered.com/) FPS counter by opening [Steam](https://store.steampowered.com/) and going to Steam -> Settings -> In-Game and adjust the *In-game FPS counter* to your liking. Now opening Dota, going to Settings -> Video, under options, the rendering API should be *OpenGL* as shown:

![OpenGL config](https://imgur.com/GExarRb.png)

We are almost done!!! In order to enable *Vulkan*, a few more steps need to be performed. Quit Dota go to the Steam Library page. Right click on *Dota 2*, click on *View Downloadable Content*, move to the *DLC* tab and check the option *Dota 2 - Vulkan Support*. You'll immediately see a download has started.

![Downloadable Content 1](https://imgur.com/YeiKxNP.png)

![Downloadable Content 2](https://imgur.com/mhSJble.png)

Meanwhile as the Download progresses, again go to the *Steam Library* page, right click on *Dota 2*, click on *Properties* and under the *General* tab click on *SET LAUNCH OPTIONS* and add the following options: **-vconsole -vulkan** and close it.

![Properties](https://imgur.com/oX7TwCc.png)

![Set Launch Options](https://imgur.com/v9R3pTZ.png)

![Launch Options](https://imgur.com/rsAygYz.png)

On opening Dota 2, under Settings -> Video, your rendering API should now be Vulkan as shown:

![Vulkan API in use](https://i.imgur.com/j8tnwPj.png)

On the right side of the page, under rendering, to your surprise, under rendering, you will find a new option **Compute Shaders**. Check that option as it will also help a lot in increasing your Dota 2 performance.

![Compute Shaders](https://imgur.com/VNxHSwp.png)

As you can see, the above screenshot was taken on my laptop with an NVIDIA 1050 GPU and has the *Game Screen Rendering Quality* to be at *100%*. The maximum FPS was auto-detected to be at 150 fps. That's all you had to do. Now enjoy the game of Dota 2 to the fullest!!!

##	Results

I have tried these settings on quite a few laptops with varying NVIDIA Graphics cards. On a laptop with NVIDIA GeForce GTX 1050 4 GB VRAM variant, **Arch Linux** (same specs as mine) with **Vulkan** and the above steps applied, the average FPS varies from **100** to **110** whereas on **Windows** running **DirectX 12**, the average FPS was about **60 - 65**. On my laptop I have only Linux installed, and the average FPS with **Vulkan** is identical. On a laptop with NVIDIA 1060 6 GB variant, the **Vulkan** performance under **Arch Linux** was about **120** FPS whereas on **Windows** with **DirectX 12**, it was about **80 - 85** FPS. But on using **OpenGL** on **Arch Linux** instead of **Vulkan**, it dropped to **90** FPS. Thus you can see that there is a significant improvement on using **Vulkan** in Linux for Dota 2. All these facts hints at one common fact that - gaming performance is steadily improving on Linux and with [Valve](https://www.valvesoftware.com/en/) trying their best to push Linux gaming and providing immense support to the Linux gaming community with their Steam [Proton](https://github.com/ValveSoftware/Proton) API, things are simply getting better and better. What can be better than having a Linux Distro which we can tweak for optimum performance with our own free will? Enough small talk, I simply can't wait to get back to Dota. Meanwhile, have a look at the following video (no audio present) where I have demonstrated the process step by step.


<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://player.vimeo.com/video/344208790' frameborder='0' webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe></div>
