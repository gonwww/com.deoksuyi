DEOKSUYI.COM (c) by Gon Y. of Deoksu-Yi
---------------------------------------
DEOKSUYI.COM is licensed under a Creative Commons 
Attribution-NonCommercial-NoDerivatives 4.0 International License.

You should have received a copy of the license along with this
work. If not, see <http://creativecommons.org/licenses/by-nc-nd/4.0/>.


VERSION HISTORY
---------------
For each version, save at https://web.archive.org/save/deoksuyi.com
- 1.0.0 / Feb 24, 2019 / Init 
- 1.1.0 / Mar  3, 2019 / Clean all; leave just a logo.


IMAGE URL CONVENTION
--------------------

- `deoksuyi.com/dsyim.svg`
- `deoksuyi.com/dsyim`
    - `/r` - raw
        - `/black.svg`
        - `/white.svg`
        - `/gray.svg`
        - ...
    - `/s` - small
        - `/b.png` -- black PNG
        - `/b.svg` -- black SVG
        - `/w.png` -- black PNG
        - `/w.svg` -- black SVG
    - `/m` - medium
        ...
    - `/l` - large
        ...

USAGE
-----

`dsyimtool.sh ./dsyim.svg ./dsyim/`

Using base image of `dsyim.svg`, create variants on `./dsyim/` directory.


CONVERTING SVG TO PNG
---------------------

1. Dependencies
    1. Install X Code: `xcode-select --install`
    2. Install Lib RSVG: `brew install librsvg`
2. Usage
    1. `rsvg-convert -h 32 icon.svg > icon-32.png`
    2. this will create an image with 32px height; width to be determined 
        automatically.
3. Note
    1. For linux, install librsvg by `sudo apt-get install librsvg2-bin`

WEBSITE SCREENSHOT
------------------

1. OSX
    1. Install Webkit2PNG `brew install webkit2png`
    2. `webkit2png https://gonyyi.com`
    3. `webkit2png -W 1200 https://news.google.com`
        1. Set width to 1200px
2. For linux
    1. With display
        1. `sudo apt-get install cutycapt`
        2. `cutycapt --url=http://www.gonyyi.com --out=gyy.png --min-width=1920 --min-height=1080`
    2. Without display
        1. `sudo apt-get install cutycapt`
        2. `sudo apt-get install xvfb` -- for X display
        3. OR `xvfb-run --server-args="-screen 0, 1280x1200x24" cutycapt --url=https://gonyyi.com --out=gyy.png`
        
