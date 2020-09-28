# Math Unicode keyboard overlay for Linux
Overlays keyboard layout with mathematical symbols.

Your keyboard layout will look like this:
![mth-Layout](/images/mth_Sep_2020.png)

It is not an optimal solution if you are using a keyboard other than the US - all special symbols turned by AltGr or AltGr + Shift will be altered.

Checked on Ubuntu 20.04 after a failed attempt to install math layout with [this method](https://blog.math.coffee/post/20180921/keyboard-layout/).

If you have Mac or Windows [this](http://insti.physics.sunysb.edu/~siegel/unicode.html) should work.

## Install
Download mth file from this repo.

Paste it to /usr/share/X11/xkb/symbols. In terminal:

```
sudo cp /path/to/file/mth /usr/share/X11/xkb/symbols
```

Do not change file to mth.txt or alike.

## Turn on
In the terminal. Make sure the new XKB file is used by running:

```
sudo dpkg-reconfigure xkb-data
```

Apply:
```
setxkbmap -layout mth
```

Changes will apply immediately.

## Turn off
Change your keyboard layout in system preferences.

## Tweaking
Tweak by editing the mth file manually. It's pretty straightforward.

In terminal:
```
sudo gedit /usr/share/X11/xkb/symbols/mth
```

To preview whole keyboard:
```
gkbd-keyboard-display -l mth
```

## Disclaimer
I have almost no idea why & how it is working. Feedback welcome.

## Thanks
Thanks to [Clive](https://blog.math.coffee/post/20180921/keyboard-layout/). I have based my mth file on his mdc (Math Dot Coffee).

I have found the setxkbmap solution [here](https://blog.lobraun.de/2020/03/09/Umlauts-on-US-Keyboard-Layouts-on-Ubuntu-with-XKB/).
