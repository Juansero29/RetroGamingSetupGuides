# Motorstorm Complete Setup Guide

> ✔ Good to know: while setting up RPCS3, you can seek precise values in the configuration using the mouse-wheel or use preset values with drag and drop

A complete guide on setting up motorstorm on a modern PC as of 2022

- [Motorstorm Complete Setup Guide](#motorstorm-complete-setup-guide)
  - [Pre-requisites](#pre-requisites)
    - [Mandatory](#mandatory)
  - [My PC Setup](#my-pc-setup)
  - [Install](#install)
  - [Playing Online](#playing-online)
    - [Using PSONE Servers](#using-psone-servers)
      - [RPCN Account Creation](#rpcn-account-creation)
      - [Setting up RPCS3 to use PSONE MotorStorm server](#setting-up-rpcs3-to-use-psone-motorstorm-server)
    - [Using PSORG](#using-psorg)
      - [Setting up RPCS3 to use PSORG MotorStorm server](#setting-up-rpcs3-to-use-psorg-motorstorm-server)
  - [Best settings for my PC setup](#best-settings-for-my-pc-setup)
  - [Custom Configuration](#custom-configuration)
    - [1440p and 60fps+ - Always playable at 60fps+ but with car stuttering](#1440p-and-60fps---always-playable-at-60fps-but-with-car-stuttering)
    - [1440p + 30fps+ - Not playable (~17fps max) and weird physics but no car stuttering](#1440p--30fps---not-playable-17fps-max-and-weird-physics-but-no-car-stuttering)
  - [Patch Manager](#patch-manager)
  - [Advice And Troubleshoot](#advice-and-troubleshoot)
    - [Unlocking 60fps and 4K](#unlocking-60fps-and-4k)
      - [4K](#4k)
      - [60FPS](#60fps)
    - [SCE\_NP\_DRM\_ERROR\_LICENSE\_NOT\_FOUND Error](#sce_np_drm_error_license_not_found-error)
  - [Links fore more info](#links-fore-more-info)
    - [Mediafire update (Youtube)](#mediafire-update-youtube)
    - [Reddit Update Discussion](#reddit-update-discussion)
    - [MotorStorm RPCS3 Recommended Settings](#motorstorm-rpcs3-recommended-settings)

## Pre-requisites

### Mandatory

- An install of [RPCS3](https://rpcs3.net/download) with the required PS3 firmware
- I currently don't know which are the minimum PC specs to run this game smoothly

## My PC Setup

- A nice PC, my personal setup is a PC with a RTX 3080, an intel i7-10700K CPU and 16GB of RAM. Game works fine at 1440p and 60FPS (apart from car stuttering issue)

## Install

1. Download the game from one of the torrents, if you want all the DLC prefer the US version `MotorStorm Complete (BCUS98155)`. If you don't care about DLC and want the Vanilla OG experience go with `MotorStorm (BCES00006)`
1. Once your game is downloaded, open RPCS3
1. From RPCS3
   1. Click on File > Add Games
   1. Browse to the folder containing `PS3_GAME`, `PS3_UPDATE` and `PS3_DISC.SFB`
   1. Click OK
   1. The game will be added to the RPCS3 library
1. Double click `Motorstorm`
1. Compilation of PPU modules will start
1. Once finished, the game will start and installation will be completed

## Playing Online

1. Open RPCS3
1. Go to Configuration > RPCN
1. Follow the [steps to create an RPCN account](https://wiki.rpcs3.net/index.php?title=Help:Netplay) (you will need an e-mail and an username)
1. Right click on `Motorstorm`
1. Click `Create custom configuration` or if you have already added a custom configuration `Change custom configuration`
1. Click on "Network"
1. Then setup PSONE or PSORG servers
1. After setting up, open the game and go to ONLINE
1. For PSORG an update will be done in-game, let it finish, it make take some time (20~30 minutes)
   1. If there's an error on first connection, then click retry, it will work after that
1. Find a lobby usually hosted by people on the discord channels and join
1. Enjoy!

### Using PSONE Servers

#### RPCN Account Creation

1. You will need to [get to the official PSONE discord channel](https://discord.com/invite/uhZuGX9)
1. Accept the rules, get your roles and stuff and then head to "SUPPORT" category and to the `#ticket-support` channel
1. If you have a PSN account, link it on the `#bots` channel so that they are more likely to accept your account creation
1. Click on `Create ticket`
1. In the ticket, send a message like this `Hey! My RPCN username is USERNAME_YOU_USED_IN_RPCN_ACCOUNT and I want to be whitelisted to play MotorStorm 🙂 Thanks`
1. Wait a couple of hours/days till you get white listed
1. Close the ticket once connection is OK

#### Setting up RPCS3 to use PSONE MotorStorm server

1. On the `Change custom configuration > Network` window
1. Change your Network Status to Connected and PSN Status to RPCN
1. Change DNS to `185.194.142.4`
1. Change IP/Hosts/Switches to `185.194.142.4`

### Using PSORG

#### Setting up RPCS3 to use PSORG MotorStorm server

No account creation or username whitelisting must be done with PSORG servers

1. On the `Change custom configuration > Network` window
1. Change your Network Status to Connected and PSN Status to RPCN
1. Change DNS to `5.161.41.41`
1. Change IP/Hosts/Switches to `1.1.1.1`

## Best settings for my PC setup

## Custom Configuration

For setting up with this settings, first create a custom configuration and reset all to default. Then apply the following values to the specified parameters in the specified windows. These are the only ones that change from the defaults. The game will then boot with this custom settings when you double-click it from the library.

### 1440p and 60fps+ - Always playable at 60fps+ but with car stuttering

| Window Name | Parameter Name                         | Parameter Value  | Reason                                                                                |
| ----------- | -------------------------------------- | ---------------- | ------------------------------------------------------------------------------------- |
| GPU         | Resolution Scale (Disable Strict Mode) | 200% (2560x1440) | 1440p resolution                                                                      |
| GPU         | Write Color Buffers                    | Checked          | Fixes issue of game 3D images not showing                                             |
| Advanced    | GPU > Read Color Buffers               | Checked          | Fixes issue of game 3D images not showing                                             |
| Advanced    | VBlank Frequency                       | 60Hz or 90hz     | Having checked the `Unlock FPS` patch, it caps the game at 60FPS => causes stuttering |

### 1440p + 30fps+ - Not playable (~17fps max) and weird physics but no car stuttering

| Window Name | Parameter Name                         | Parameter Value  | Reason                                                                                                     |
| ----------- | -------------------------------------- | ---------------- | ---------------------------------------------------------------------------------------------------------- |
| CPU         | PPU Decoder > Interpreter (static)     | Selected         | Removes car stuttering but really lags on some tracks. There's also random occasions when boost won't work |
| GPU         | Resolution Scale (Disable Strict Mode) | 200% (2560x1440) | 1440p resolution                                                                                           |
| GPU         | Write Color Buffers                    | Checked          | Fixes issue of game 3D images not showing                                                                  |
| Advanced    | VBlank Frequency                       | 60hz             | Having checked the `Unlock FPS` patch                                                                      |

## Patch Manager

I have all patches installed. Some people may prefer to keep Motion Blur, or no. Do as you like.

## Advice And Troubleshoot

### Unlocking 60fps and 4K

#### 4K

1. Click on MotorStorm > Change Custom Configuration > `GPU`
1. On the section `Resolution Scale (Disable Strict Mode)` choose your desired resolution
1. For 1440p I go with `200% (2560x1440)`, if you have the beast to run 4K, then go with `300% (3840x2160)`.

#### 60FPS

> ⚠ Warning! As of 29/11/2022 unlocking FPS on the game will cause that your car will stutter troughout the races! This is a compatibility issue with RPCS3 currently active. You can [follow its resolution here](https://github.com/RPCS3/rpcs3/issues/8376)

1. Right click on MotorStorm > Manage Game Patches
1. You need to check `Unlock FPS`
1. Then click on MotorStorm > Change Custom Configuration > Advanced
1. On the right-bottom side of the window you will see `VBlank Frequency` , this setting is equivalent to the MAX FPS CAP of the game
1. Set it up to your liking. With 60 or 90 are the best values.

### SCE_NP_DRM_ERROR_LICENSE_NOT_FOUND Error

- If you come accross a SCE_NP_DRM_ERROR_LICENSE_NOT_FOUND error, you will need to remove any trace of BCES00006 in your RPCS3 installation folder (ex. in all dev_hdd\* folders). this can be caused after trying to install MotorStorm Complete (BCUS98155) when you had installed base MotorStorm (BCES00006) before. If this doesn't work, try to uninstall and reinstall RPCS3 and reinstalling MotorStorm

## Links fore more info

### Mediafire update (Youtube)

- [PS3 Motorstorm 3.1 Update! Time Attack and DLC now playable RPCS3 emulator - youtube.com](https://www.youtube.com/watch?v=p8kGAhlFREE)
- [BCES00006.rar - mediafire.com](https://www.mediafire.com/file/ub5bo9jkk2j2pst/file)

### Reddit Update Discussion

- [Where to find MotorStorm Update - reddit.com](https://www.reddit.com/r/ps3piracy/search/?q=motorstorm&restrict_sr=1&sr_nsfw=&include_over_18=1)

### MotorStorm RPCS3 Recommended Settings

- [MotorStorm - RPCS3 Wiki](https://wiki.rpcs3.net/index.php?title=MotorStorm)
