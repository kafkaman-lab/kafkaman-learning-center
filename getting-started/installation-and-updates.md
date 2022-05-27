# Installation and updates

<br />

Kafkaman is available as a native desktop app for Mac (Intel and M1), Windows (32-bit / 64-bit), and Linux (64-bit) operating systems.

To get the latest version of the Kafkaman desktop app, visit the [download page](https://github.com/Kafkaman-lab/kafkaman-app/releases) and select for your platform.

## Contents

* Installing Kafkaman on the desktop
    * [Mac](#installing-Kafkaman-on-mac)
    * [Windows](#installing-Kafkaman-on-windows)
    * [Linux](#installing-Kafkaman-on-linux)
* [Updating Kafkaman](#updating-Kafkaman)
* [Troubleshooting your Kafkaman installation](#troubleshooting-your-kafkaman-installation)

<br />

## Installing Kafkaman on Mac

Kafkaman is available for macOS 10.11 (El Capitan) and later.

1. [Download](https://github.com/Kafkaman-lab/Kafkaman-app/releases) the latest Kafkaman app.

    > Make sure to download the **Mac Apple Chip** version if you have a Mac with the M1 processor.

1. If your browser downloads the file as a ZIP file, find the file in the **Downloads** folder and unzip it.
1. In the **Downloads** folder, double-click the `Kafkaman` file to install it.
1. When prompted, move the file to your __Applications__ folder. This will ensure that future updates can be installed correctly.

> You may encounter a "Library not loaded" error if you unzip and install Kafkaman using a third-party archiving app. Use the default Archive Utility for Mac to unzip the file.

## Installing Kafkaman on Windows

Kafkaman is available for Windows 7 and later.

1. [Download](https://github.com/kafkaman-lab/kafkaman-app/releases) the latest Kafkaman app.
1. Select and run the `.exe` file to install Kafkaman.

> Kafkaman v9.4 is the last version of the Kafkaman app that supports both 32-bit and 64-bit Windows. All versions of the Kafkaman app following v9.4 will only work on 64-bit Windows. You can continue to use Kafkaman v9.4 and earlier on 32-bit Windows.

## Installing Kafkaman on Linux

You can install Kafkaman on Linux by manually downloading it, using the [Snap](https://snapcraft.io/kafkaman) store link, or with the command `snap install Kafkaman`.

To install manually, [download](https://github.com/Kafkaman-lab/kafkaman-app/releases) and unzip the app, for example into the `Downloads` directory.

To start the app from a launcher icon, create a desktop file, naming it `Kafkaman.desktop` and saving it in the following location:

```shell
~/.local/share/applications/Kafkaman.desktop
```

Enter the following content in the file, replacing `/path/to/Downloads` with the location of the file, and save it:

```shell
[Desktop Entry]
Encoding=UTF-8
Name=Kafkaman
Exec=/path/to/Downloads/Kafkaman/app/Kafkaman %U
Icon=/path/to/Downloads/Kafkaman/app/resources/app/assets/icon.png
Terminal=false
Type=Application
Categories=Development;
```

> Kafkaman supports the following distributions:
>
> * Ubuntu 14.04 and newer
> * Fedora 24
> * Debian 8 and newer
>
> The support of certain Linux distributions depends on if they're supported by Electron. Refer to [Electron's documentation](https://www.electronjs.org/docs/tutorial/support#linux).
>
> It's recommended you install [Snap](https://snapcraft.io/kafkaman) as it includes all the libraries that the app needs and they're bundled with the app itself.
>
> Avoid starting Kafkaman using the `sudo` command, as it will create permission issues on the files created by Kafkaman.
>
> Make sure you have read/write permission for the `~/.config` folder where Kafkaman stores information.
>
> If you are an Ubuntu 18 user, you will also need to install the `libgconf-2-4` package with the command `apt-get install libgconf-2-4`

## Updating Kafkaman

The native Kafkaman apps will notify you when a major update is available. For other updates you will see a dot on the settings icon. If the indicator is red instead of orange, it indicates a failed update.


## Troubleshooting your Kafkaman installation

If you encounter any issues installing and running Kafkaman, check out the following tips. If these don't help, please refer to the installation posts on the [community forum](https://github.com/kafkaman-lab/kafkaman-app) and create a new post if your issue isn't already covered.
