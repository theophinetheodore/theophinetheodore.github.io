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

# hugo command to serve the website locally
# for editing and previewing
hugo serve

# hugo command to build
# you could lose the '-d docs' part by
# setting publishDir to 'docs' in hugo.toml
hugo build --minify -d docs --buildFuture -e production
```

a mistake i did is,
i pushed the `hugo serve` output directly into production,
and the rss.xml had http://localhost:1313 as the baseURL.
therefore, learnt to use hugo build separately.
(i used to do it before, but i just forgot about it.)

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

---

as for the custom domain, i had this issue where i'd set the custom domain in github repo settings and it'd be working, until i delete the `docs/` directory and generate a new one. but then when i'm about to push, i have some git conflict, and i'll run a git pull and push. but the custom domain would stop working.

turns out, i have to have a file named CNAME with the custom domain inside `docs/`. so i dropped a CNAME into `static/` so when i run `hugo build`, it'd just drop the file into `docs/`.

