---
title: my wayland situation.
date: 2025-07-27
---
## pros of wayland (for me)

- pinch-to-zoom works in chromium based browsers.
- waydroid.
	- tried doing it in xorg with cage and weston, won't recommend
- touchpad gestures work.
	- i don't have any use for it though
- things are smoother and brighter? or am i imagining?

## wayland "showstoppers" for me, personally

- gtk4 applications freeze the whole KDE Plasma desktop for some reason?
- ~~can't paste images in clipboard into chat applications.~~ (works now ig)
- ~~panels appear stacked on top of each other instead of left, right, center.~~ (fixed)
- gramps crashes.
- maim doesn't work. (i need a screenshot tool that returns something other than 0 if it's cancelled, and everything else - flameshot, spectacle returns 0 even if cancelled).
- grim doesn't work in kwin-wayland, because some wlr unstable protocol lacking. (not wlroots' fault, but a hundred implementations exist).
	- and who names these tools? i mean, grim, slurp, scrot... oh my God.
- issues with anydesk and rustdesk.
- no simplescreenrecorder :(
	- well, not a wayland issue, but SSR is just too good

