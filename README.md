# Math Unicode keyboard overlay for Linux
Overlays keyboard layout with mathematical symbols.

![mth-Layout](/images/mth_Jan_2021.png)

Checked on Ubuntu 20.04 after a failed attempt to install math layout with [this method](https://blog.math.coffee/post/20180921/keyboard-layout/).

There is analog thing for [Mac](http://insti.physics.sunysb.edu/~siegel/unicode.html) and [Windows](http://terathon.com/blog/a-mathematical-keyboard-layout/).

## Install
Download <a id="raw-url" href="https://github.com/CaptchaSamurai/Math-Unicode-keyboard-overlay-Linux-XKB/blob/master/mth">mth file</a> from this repo.

Paste it to /usr/share/X11/xkb/symbols:

```
sudo cp /path/to/file/mth /usr/share/X11/xkb/symbols
```

Do not add extension to the file, like mth.txt.

## Turn on
Make sure the XKB is used:

```
sudo dpkg-reconfigure xkb-data
```

Apply:
```
setxkbmap -layout mth
```

Changes will apply immediately.

## Quickly move between keyboards
```
setxkbmap -layout <name of your previous keyboard layout>
```

To move quickly between layouts you can assign keyboard shortcut to "setxkbmap -layout xyz" commands. Simply go to: Settings → Keyboard Shortcus.

You can also manually change your keyboard layout in the System Settings.

## Tweaking layout
Tweak by editing the mth file manually. It's pretty straightforward.

```
sudo gedit /usr/share/X11/xkb/symbols/mth
```

To preview the whole keyboard:
```
gkbd-keyboard-display -l mth
```

## Disclaimer
I have almost no idea how it is working. Feedback is welcomed.

## Thanks 🙌
Thanks to [Clive](https://blog.math.coffee/post/20180921/keyboard-layout/). I have based my mth file on his mdc (Math Dot Coffee).

I have found the setxkbmap solution [here](https://blog.lobraun.de/2020/03/09/Umlauts-on-US-Keyboard-Layouts-on-Ubuntu-with-XKB/).
