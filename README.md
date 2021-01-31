# apt-watch-upgradable

Check for available updates on Debian/Ubuntu based systems and send an email if so.

Needs `apt` to be installed!

## Installation

    git clone https://github.com/K-Ko/apt-watch-upgradable.git
    cd apt-watch-upgradable
    composer update -a

Copy settings file

    cp .env.dist .env

Adjust settings in `.env`

    Usage: ./apt-watch-upgradable [options]

    Options:
            -a      Send always an email, also if no upgrade is avaliable
            -d      Download packages but NOT install
            -h      This help

## crontab

    @daily sudo /path/to/apt-watch-upgradable -d
    #
    # Catch email errors
    #@daily sudo /path/to/apt-watch-upgradable >> /path/to/apt-watch-upgradable.log
