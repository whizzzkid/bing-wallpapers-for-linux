# Bing Wallpapers For Linux
This enables bing wallpaper on linux, specifically debian based distros.

Forked from https://github.com/whizzzkid/bing-wallpapers-for-linux

## Supported Desktop Environments

- Gnome
- Cinnamon
- Unity
- Xfce

## Using Script directly.
Just download or clone this repo. Run:

    $ bingwallpaper

But this would keep on running as we check every 3 hours for new wallpaper. So it's better to do it this way:

    $ bingwallpaper &>/dev/null &

## Run Once
To update the wallpaper only once (Instead of checking every 3 hours), Run:

    $ bingwallpaper -1

## Setting Up Cron
To setup regular checks for new wallapers, edit crontab for the current user, using:

    $ crontab -u $USER -e

, and add this line:

    0 */6 * * * bingwallpaper -1 > /dev/null 2>&1

This will run every 6 hours. You can use [this link](http://www.crontab-generator.org/) for reference.

## License
GPLv2

