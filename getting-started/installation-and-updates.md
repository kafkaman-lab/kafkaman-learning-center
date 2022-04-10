kafkaman is available as a native desktop app for Mac (Intel and M1), Windows (32-bit / 64-bit), and Linux (64-bit) operating systems.

To get the latest version of the kafkaman desktop app, visit the [download page](https://github.com/kafkaman-lab/kafkaman-app) and select for your platform.

## Contents

* Installing kafkaman on the desktop
    * [Mac](#installing-kafkaman-on-mac)
    * [Windows](#installing-kafkaman-on-windows)
    * [Linux](#installing-kafkaman-on-linux)
* [Updating kafkaman](#updating-kafkaman)
* [Troubleshooting your kafkaman installation](#troubleshooting-your-kafkaman-installation)

## Installing kafkaman on Mac

kafkaman is available for macOS 10.11 (El Capitan) and later.

1. [Download](https://github.com/kafkaman-lab/kafkaman-app) the latest kafkaman app.

    > Make sure to download the **Mac Apple Chip** version if you have a Mac with the M1 processor.

1. If your browser downloads the file as a ZIP file, find the file in the **Downloads** folder and unzip it.
1. In the **Downloads** folder, double-click the `kafkaman` file to install it.
1. When prompted, move the file to your __Applications__ folder. This will ensure that future updates can be installed correctly.

> You may encounter a "Library not loaded" error if you unzip and install kafkaman using a third-party archiving app. Use the default Archive Utility for Mac to unzip the file.

## Installing kafkaman on Windows

kafkaman is available for Windows 7 and later.

1. [Download](https://github.com/kafkaman-lab/kafkaman-app) the latest kafkaman app.
1. Select and run the `.exe` file to install kafkaman.

> kafkaman v9.4 is the last version of the kafkaman app that supports both 32-bit and 64-bit Windows. All versions of the kafkaman app following v9.4 will only work on 64-bit Windows. You can continue to use kafkaman v9.4 and earlier on 32-bit Windows.

## Installing kafkaman on Linux

You can install kafkaman on Linux by manually downloading it, using the [Snap](https://snapcraft.io/kafkaman) store link, or with the command `snap install kafkaman`.

To install manually, [download](https://github.com/kafkaman-lab/kafkaman-app) and unzip the app, for example into the `Downloads` directory.

To start the app from a launcher icon, create a desktop file, naming it `kafkaman.desktop` and saving it in the following location:

```shell
~/.local/share/applications/kafkaman.desktop
```

Enter the following content in the file, replacing `/path/to/Downloads` with the location of the file, and save it:

```shell
[Desktop Entry]
Encoding=UTF-8
Name=kafkaman
Exec=/path/to/Downloads/kafkaman/app/kafkaman %U
Icon=/path/to/Downloads/kafkaman/app/resources/app/assets/icon.png
Terminal=false
Type=Application
Categories=Development;
```

> kafkaman supports the following distributions:
>
> * Ubuntu 14.04 and newer
> * Fedora 24
> * Debian 8 and newer
>
> The support of certain Linux distributions depends on if they're supported by Electron. Refer to [Electron's documentation](https://www.electronjs.org/docs/tutorial/support#linux).
>
> It's recommended you install [Snap](https://snapcraft.io/kafkaman) as it includes all the libraries that the app needs and they're bundled with the app itself.
>
> Avoid starting kafkaman using the `sudo` command, as it will create permission issues on the files created by kafkaman.
>
> Make sure you have read/write permission for the `~/.config` folder where kafkaman stores information.
>
> If you are an Ubuntu 18 user, you will also need to install the `libgconf-2-4` package with the command `apt-get install libgconf-2-4`

## Updating kafkaman

The native kafkaman apps will notify you when a major update is available. For other updates you will see a dot on the settings icon. If the indicator is red instead of orange, it indicates a failed update.


## Troubleshooting your kafkaman installation

If you encounter any issues installing and running kafkaman, check out the following tips. If these don't help, please refer to the installation posts on the [community forum](https://github.com/kafkaman-lab/kafkaman-app) and create a new post if your issue isn't already covered.
