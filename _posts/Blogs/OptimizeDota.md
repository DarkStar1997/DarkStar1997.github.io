#	Optimizing Dota 2 Performance on Linux with Vulkan on NVIDIA Graphics Cards

*Tags:*

<img align="left" width="30" height="30" src="/assets/icons/gaming.jpg"> &nbsp; Gaming<br/>
<img align="left" width="30" height="30" src="/assets/icons/nvidia.png"> &nbsp; NVIDIA<br/>
<img align="left" width="30" height="30" src="/assets/icons/vulkan.png"> &nbsp; Vulkan<br/>
<img align="left" width="30" height="30" src="/assets/icons/dota.png"> &nbsp; Dota<br/>

Gaming on the **Linux** platform is extremely underrated and is often completely *rejected* by most gamers when it comes to high-FPS gaming. In this blog, I will present a stark contrast to the above idea. The game of [Dota 2](https://www.dota2.com/play/) does not need any introduction, and being a Linux enthusiast and a Dota addict, I'd love to share a few simple tips on optimizing Dota 2 performance on Linux.

*Spoilers:* As I will demonstrate, after following the steps given in this blog you should have a significantly higher FPS compared to Dota running on Windows on identical hardware (about 30-40 FPS, depending on your graphics card).

##	Requirements

*	NVIDIA Graphics card with Vulkan support and a Linux Distro
*	Your graphics drivers are updated and working correctly
*	I'll assume that you have got [Steam](https://store.steampowered.com/) installed with [Dota 2](https://www.dota2.com/play/) up and running.

##	Let's Get to the Real Business

As stated in the title, we will be needing [Vulkan](https://www.khronos.org/vulkan/). At the time of writing, my NVIDIA Driver version is 430.26 running on *Arch Linux* as shown below:

```
[rohan@archlinux ~]$ nvidia-smi 
Mon Jun 24 21:42:46 2019       
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 430.26       Driver Version: 430.26       CUDA Version: 10.2     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|===============================+======================+======================|
|   0  GeForce GTX 1050    Off  | 00000000:01:00.0 Off |                  N/A |
| N/A   50C    P3    N/A /  N/A |    230MiB /  4042MiB |      0%      Default |
+-------------------------------+----------------------+----------------------+
                                                                               
+-----------------------------------------------------------------------------+
| Processes:                                                       GPU Memory |
|  GPU       PID   Type   Process name                             Usage      |
|=============================================================================|
|    0       786      G   /usr/lib/Xorg                                183MiB |
|    0      1003      G   ...uest-channel-token=13847652062622588702    47MiB |
+-----------------------------------------------------------------------------+
[rohan@archlinux ~]$ uname -r
5.1.12-arch1-1-ARCH
```

To install the NVIDIA graphics drivers and Vulkan support, please find the installation instructions for your respective distro. If you are running Arch Linux, you can install the latest nvidia graphics drivers and vulkan support with the command `sudo pacman -S nvidia-dkms vulkan-icd-loader`. What makes the 430 driver special is that, it received notable performance improvements for [Vulkan](https://www.khronos.org/vulkan/). The installation of [Steam](https://store.steampowered.com/) is also straightforward for most distros. If you are on Arch, follow [these](https://wiki.archlinux.org/index.php/Steam) instructions to install [Steam](https://store.steampowered.com/). In my experience, you might need [nvidia-utils](https://www.archlinux.org/packages/extra/x86_64/nvidia-utils/) and [lib32-nvidia-utils](https://www.archlinux.org/packages/multilib/x86_64/lib32-nvidia-utils/) to get [Steam](https://store.steampowered.com/). With [Steam](https://store.steampowered.com/) up and running, installing and running [Dota 2](https://www.dota2.com/play/) should be a piece of cake. To monitor your FPS turn on the [Steam](https://store.steampowered.com/) FPS counter by opening [Steam](https://store.steampowered.com/) and going to Steam -> Settings -> In-Game and adjust the *In-game FPS counter* to your liking.