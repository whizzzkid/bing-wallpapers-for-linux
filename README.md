# Bing Wallpapers For Linux
This enables bing wallpaper on linux, specifically debian based distros.

## Installation Instruction (Ubuntu, Mint and other Debian based distros.
This should be simple.

    sudo add-apt-repository ppa:whizzzkid/bingwallpaper
    sudo apt-get update
    sudo apt-get install bingwallpaper

## Using Script directly.
Just download or clone this repo. Run:

    $ bingwallpaper

But this would keep on running as we check every 3 hours for new wallpaper. So it's better to do it this way:

    $ bingwallpaper &>/dev/null &

## Run Once
To update the wallpaper only once (Instead of checking every 3 hours), Run:

    $ bingwallpaper -1

## Setting Up Cron
Do not use sudo, as it will set up the cron for root, which will not change the wallpaper for the current user. To edit crontab for current user do:

    $ crontab -u $USER -e

We would only need to run it once, because cron will be re-running this, so:

    $ * */6 * * * bingwallpaper true >/dev/null 2>&1

This will run this every 6 hours. You can use [this link](http://www.crontab-generator.org/) for reference.

*Note: If you installed this package from apt, then disable the startup script setup by default. Go to startup applications and remove 'bingwallpaper'*

## Contributing
Feel free to make changes and send PR, I'll be aaccepting them.

## License
GPLv2

## PPA
https://launchpad.net/~whizzzkid/+archive/ubuntu/bingwallpaper
