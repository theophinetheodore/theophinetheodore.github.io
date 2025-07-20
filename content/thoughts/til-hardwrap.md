---
title: "TIL hardwrap."
date: 2025-07-20
---

i have this writing style of
breaking stuff into lines.
i don't do paragraphs.
i like it this way.

but that means i have to run this after i complete writing something:

```vimscript
:%s:$:  :g
```

that's two spaces.
basically what it does is, add two spaces to the end of every line.

i think markdown requires either two spaces,
or a backslash,
or a `<br>`.

but today i came across this thing called **hardwraps**.

in your `hugo.toml` file, add this:
```toml
[markup]
  [markup.goldmark]
    [markup.goldmark.renderer]
          hardWraps = true
```

and no need of hacks anymore.
i could just write in obsidian and hit `:w`.