# Raspberry Pi 3 B+ Headless Setup

## Intro

I recently got a Raspberry Pi (CanaKit Ultimate Starter Kit from MicroCenter). Prior to purchasing, I didn't do much homework on additional things I may need to get it up and running using my MacBook Pro, as I was told you could boot it without a keyboard or a mouse. Indeed, you can, and it's dirt simple.

Most of the setup tutorials assume you have both, so here's how to setup a Raspberry Pi 3 B+ if you don't have a keyboard or a mouse.

## `vim`
As you go along, you're gonna need to fire up `vim` on the Pi in a few spots. If you're a little rusty on `vim`, here's a [quick guide](https://www.howtoforge.com/vim-basics) that should help you along if you get stuck. I found these `vim` commands handy:

`:x` or `:wq` to save and exit

`:q!` to exit WITHOUT saving

`dd` to delete a line

`d5d` to delete 5 lines


## [Video: Headless setup for Mac OS](https://www.youtube.com/watch?v=Ct9XwyYvmbU)
* At the 5m30s mark in the video, the narrator configured `wpa_supplicant.conf`, which did not work for me accessing an Apple Time Capsule.
* This setup worked for me:

    ```
    country=US
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1

    network={
        ssid="NETWORK-NAME"
        psk="NETWORK-PASSWORD"
    }
    ```
* These steps described in that video will get you onto a WiFi network, nothing more.

## [Video: Raspberry Pi VNC Screen sharing on a Mac](https://www.youtube.com/watch?v=2iVK8dn-6x4)
* This video takes you through how to setup screen sharing on a Mac.
* There is no need to install additional software on your Mac for VNC.
* [GitHub: How to setup Raspberry Pi VNC Screen Sharing on a Mac](https://github.com/HackerShackOfficial/Raspberry-Pi-VNC-Mac)
