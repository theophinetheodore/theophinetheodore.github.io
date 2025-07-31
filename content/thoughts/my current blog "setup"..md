---
title: my current blog "setup".
date: 2025-07-30T08:00:00
---
well, i use [hugo](https://gohugo.io/) with the [typo](https://github.com/tomfran/typo) theme.
i initially wanted to make my own theme, so i yanked [eric murphy's starter theme](https://github.com/ericmurphyxyz/hugo-starter-theme).
but then i realized i don't want to make a whole new theme,
figure everything out,
so i found typo and stuck with it.
i just wanna get started with writing.

i'm using github pages.
since i'm using hugo, i looked up ways to host a hugo website in github pages.
and all these blogs have stuff about YAMLs and github actions
and workflows and stuff.
and i was like, nah, man, i don't wanna do this stuff.

then i figured out github pages can fetch the website files
either from the root (/) of the repository or from the docs directory.
so now i just do this:

```
# zoxide shortcut to go the repository, or just cd
z blog

# hugo serves the website and builds it in docs/
# Ctrl-c when over
hugo serve --minify -d docs --buildFuture
```

and then just do the git stuff: adding, committing, pushing.
no need of workflows and stuff.
one less thing to take care of.

---

i use [obsidian](https://obsidian.md) to write my notes.
i would like to switch, cause electron.

i tried to find another editor that is nice and simple
and has vim keybindings.
tried other stuff: kwrite, daino notes, ghostwriter, all that.
none of em click.

and writing in neovim with a mono font doesn't cut it anymore.

so i'm using obsidian.
but gotta say, obsidian is pretty comfy.
using it with [gitlab sans](https://gitlab-org.gitlab.io/frontend/fonts/) typeface and [mono-black](https://github.com/ZeChArtiahSaher/obsidian-mono-black) theme.
i use this combo in every vault of mine.
