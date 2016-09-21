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

## Contributing
Feel free to make changes and send PR, I'll be aaccepting them.

## License
GPLv2

## PPA
https://launchpad.net/~whizzzkid/+archive/ubuntu/bingwallpaper
