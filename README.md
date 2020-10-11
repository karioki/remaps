# Remapping

It's not perfect but I've been using it now for a long time.

So it modifies some keys:

Key        |Single Press |Hold (Modifier)
-----------|-------------|-------------------
Space Bar  |Space        |Super or Window Key
CapsLock   |ESC          |Ctrl
Enter      |Enter        |Ctrl
LeftShift  |Underscore   |LeftShift
RightShift |Dash         |RightShift

So in a short summary, this will give Control keys access to the pinkies in addition to ESC.
And will use two Shift keys for frequently used but hard to reach keys
(at least for me, you can use them for other keys).
Last but not least the Space Bar act as Super key which can be super useful.

# Usage

This will only work with locale set to "en_US.UTF-8".
[This](https://wiki.archlinux.org/index.php/locale) can be helpful for managing locale.
You need to install package [xcape](https://github.com/alols/xcape) first then:

```
cd <path-to-this-repo>
sh remaps
```

Add above in your startup programs for daily usage.

# Some problems

* `super + space` will not work if you some binding to it.  You can reassign that binding.
* Very rarely, in some programs when you type `<space> <some-key>` this can go wrongly as `super + <the-key>`. This is mainly due to slow xcape or human error.

# Note

If you were using some other mappings or did some modification to
this script you may need to reload it properly:

```
cd <path-to-this-repo>
setxkbmap -layout us -option; killall xcape; sh remaps
```

# Limitation

Works under Linux and Xorg only.  Most of the desktop distros should be fine.
Dwm and i3 are fine too.
