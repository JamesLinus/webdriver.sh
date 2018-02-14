# webdriver.sh

![webdriver.sh screenshot](https://github.com/vulgo/webdriver.sh/raw/master/Images/screenshot.png "webdriver.sh screenshot")

Bash script for managing Nvidia's web drivers on macOS High Sierra.

## Installing

Install webdriver.sh easily with [Homebrew](https://brew.sh)

```
brew tap vulgo/repo
brew install webdriver.sh
```

## Example Usage

#### Install or update drivers

```
sudo webdriver
```

Install/update to the latest available Nvidia web drivers for your current version of macOS

#### Install a specific driver version

```
sudo webdriver -u URL
```

Install the drivers from the package at URL (without version checks). There is a nice list of available drivers/URLs maintained [here](http://www.macvidcards.com/drivers.html).

#### Uninstall

```
sudo webdriver -r
```

Removes Nvidia's web drivers from your system

#### Patch drivers to load on a different version of macOS

```
sudo webdriver -m [build]
```

Modify the installed driver's NVDARequiredOS. If no [build] is provided for option -m, the installed macOS's build version string will be used.

#### Show help

```
webdriver -h
```

Display help, lists all available options

## Configuration

The current web drivers will be uninstalled when you install new drivers, you can remove additional files by editing \<homebrew prefix\>/etc/webdriver.sh/uninstall.conf

## F.A.Q.

#### Is webdriver.sh compatible with regular or other third party methods of driver installation?

Yes, use webdriver.sh at any time, before or after using any other method of driver installation.

#### Does webdriver.sh install the Nvidia preference pane?

No, you can install it at any time via Nvidia's installer package - webdriver.sh works fine alongside it or without it.

#### Will webdriver.sh mess with Nvidia's installer or 'repackage' the driver?

No, there are [other tools](https://www.google.com/search?q=nvidia+web+driver+repackager) available for doing this.  [NvidiaWebDriverRepackager](https://github.com/Pavo-IM/NvidiaWebDriverRepackager)

#### What about uninstalling, without repackaging won't there be problems?

No, Nvidia's own installer runs a perl script that removes everything installed by webdriver.sh.

#### Can't i just uninstall the drivers using webdriver.sh?

Yes, sudo webdriver -r

#### Does webdriver.sh install things to the wrong place?

No.

## License

webdriver.sh is free software licensed under the terms of the GPL version 3 or later
