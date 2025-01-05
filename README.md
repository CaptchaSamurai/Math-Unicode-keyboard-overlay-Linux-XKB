# Math keyboard layout for X Window System (e.g. Ubuntu 22)
The customized math keyboard layout is designed to streamline your mathematical writing everywhere.
With a few easy steps, you will be able to type ∀, ℕ, Σ, ∫, ω and other math symbols as easily as you type alphabet letters.

![mth-Layout](/images/mth_v4_Nov_2023.png)

If you don't have Linux check out math keyboard overlay for [Mac](http://insti.physics.sunysb.edu/~siegel/unicode.html) or [Windows](https://web.archive.org/web/20230503051817/https://terathon.com/blog/a-mathematical-keyboard-layout/).

The following instructions are checked for Ubuntu 20.04 and 22.04. 

## Installation
Download <a id="raw-url" href="https://github.com/CaptchaSamurai/Math-Unicode-keyboard-overlay-Linux-XKB/blob/master/mth">mth file</a> from this repository.

Paste it to /usr/share/X11/xkb/symbols:

```
sudo cp /path/to/file/mth /usr/share/X11/xkb/symbols
```

To change the keyboard overlay execute the following command:

```
setxkbmap -layout mth
```

Changes apply immediately.

## Quickly switch between keyboards
To switch quickly between layouts you can assign a keyboard shortcut (Settings → Keyboard → Shortcuts) to the following command:

```
setxkbmap -layout <name of a keyboard layout, like "mth" or "us">
```

You can also change your keyboard layout by hand in the System → Keyboard → Input Sources.

## Tweaking layout
Edit the mth file (don't forget to make a backup copy):

```
sudo gedit /usr/share/X11/xkb/symbols/mth
```

To preview layout:
```
gkbd-keyboard-display -l mth
```

## Potential issues
The `mth` file has no extension. Do **not** add any extension to this file, like `mth.txt`.

## Problem with Wayland
I don't know how to install a new layout in Wayland (e.g. Ubuntu 24 uses it). I have tried adding mth file as above and then editing /usr/share/X11/xkb/rules/evdev.xml in an obvious way as this post from [stigok blog](/usr/share/X11/xkb/rules/evdev.xml) suggest. This didn't work. Suggestions appreciated!

## History
The mth layout evolves. You can find deprecated layouts [here](https://github.com/CaptchaSamurai/Math-Unicode-keyboard-overlay-Linux-XKB/tree/master/old_layouts). 

## Thanks 🙌
Shout out to Clive from the Math Dot Coffee blog (which, as of 2023, no longer exists) — `mth` layout is based on their `mdc` layout.

I learned about `setxkbmap` on lobrun.de blog, which, as of 2023, no longer exists.
