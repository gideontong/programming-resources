# Setting Up a Pi at UCSD

## Getting Ready

*This guide is written for the Raspberry Pi Zero W. More details and pictures for any Pi coming soon.*

You'll need:

* Raspberry Pi
* MicroSD Card
* SD Card Reader
* Power Cable (mciroUSB for Pi Zero)
* Power Adapter (5V 2A or 5 3A)
* Windows Computer (*Other guides coming soon?*)

Download the following files and programs to your computer:

* [Raspbian](https://www.raspberrypi.org/downloads/raspbian/): I reccomend [Raspbian Buster Lite](https://downloads.raspberrypi.org/raspbian_lite_latest) although you can use the desktop version if you want.
* [Etcher](https://www.balena.io/etcher/): Install this program after downloading.
* A Code Editor (Like [Notepad++](https://notepad-plus-plus.org/) or [VS Code](https://code.visualstudio.com/)): Notepad will not work because Linux and Windows end lines in text files differently.
* A SSH Terminal (Like [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/)): You might already have a similar tool built in.

## Gathering Information

You'll need your Raspberry Pi's MAC address in order to register it with ResNet and get the Pi running online 24/7. To do this, follow these steps to install Raspbian on your Pi:

1. Plug in your SD card reader into your computer with your microSD card plugged in. You may need an SD card adapter.

2. Run balenaEtcher and select the Raspbian image you downloaded, and select the target as the microSD card you just plugged in. Press Flash!

3. Wait for the process to complete, and verify there are no errors. If there are errors, try steps 1-2 again.

4. Your microSD card will now appear on your computer as multiple drives, including some Windows can't read. If any popup opens up that asks you to format a disk, select cancel. Open up the drive that is labeled "boot" and create a new blank file called `ssh`.

5. Then, open up your code/text editor of choice and create a file that says:

    ```conf
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1
    country=US

    netwrork={
        ssid="testformypi"
        scan_ssid=1
        psk="mycoolpi1234"
    }
    ```

6. Go to your computer's **Settings**, click on **Network & Internet**, then click **Mobile Hotspot**. Click **Edit**, then set your **Network name** to `testformypi` and your **Network password** to `mycoolpi1234`. If you look at step 5, you can see where these come from. You can set them to anything you want as long as they match and don't have spaces or weird characters. If Network band is an option, try to set it to 2.4 GHz. If your internet disconnects in a future step, come back and set it to Any available or 5 GHz instead.

7. Plug in your Raspberry Pi to power and turn on your **Mobile hotspot** on your computer by toggling the box that says **Share my Internet connection with other devices**.

8. In a few moments, your Raspberry Pi should pop up in your computer's settings under a table as `raspberrypi`. There will be also a column called MAC address and IP address. Make a note of the MAC address of the Raspberry Pi by taking a screenshot or writing it down somewhere.

9. Turn off your computer's Mobile hotspot and unplug your Raspberry Pi and proceed to the next section.

## Preparing a Remote Connection

If you want to skip ahead and prepare something before doing this section, I reccomend doing step 1 of [Getting Online](#Getting-Online). You'll need to do this section before doing the rest of Getting Online.

I'll update this section soon with information that'll help you.

Todo:

* Updating Hostname
* Updating Login Credentials
* Setting Up a Domain
* Setting Up Dynamic DNS
* Opening a SSH Port

## Getting Online

Now that we have the MAC address, we want to register it with ResNet in order to keep the Raspberry Pi connected online.

1. Visit the ResNet portal page by clicking [this link](https://wheatley.ucsd.edu/jump/resnet_reg_form/). You'll need to log in with your UCSD credentials and then you'll be presented with a form to register your device. Fill out the form truthfully, you can put Raspberry Pi as your device type and fill out the same MAC address you saved earlier. Capitialization in your MAC address does not matter.

2. In a few hours, you will get an email from someone at the help desk saying your device has been registered. During this time, plug in your microSD card back into your computer.

3. Just like before, you will see some popups asking you to format the disks you plugged in. Press cancel.

4. Open up the drive that is called "boot" and look for a file called wpa_supplicant. If you find it, delete it. Then make a new one. If you can't find it, just make a new one.

5. Inside the code/text editor of your choice, write the following into your text editor:

    ```conf
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1
    country=US

    netwrork={
        ssid="RESNET-6TH-RESHALLS"
        key_mgmt=NONE
    }
    ```

    Do note that if you don't live in the Sixth College Residential Halls, you'll have to put the name of the wireless network for your dorm instead that provides internet access without a password.

At this point, you'll want to remotely connect to your Raspberry Pi. But I'll fill out the preparing a remote connection section first.

Todo:

* Remotely Connecting to a Pi
* Entering Basic Commands in a Terminal

## Uploading Files

You can upload files using SSH. I'll describe how to do that in the future.

Todo:

* Uploading Files

## Running Files

You can run your Python files by typing something like `python3 main.py`. But more information to come in the future.

### Make It a Service

Turns out your script closes when you close your terminal. Here's how to make it run forever. (Information coming soon.)

Todo:

* Making `systemd` services
* Using `screen` to your advantage
