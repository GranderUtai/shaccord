# Shaccord
Microtonal chord visualisation program based on L4mplight's works  
interface inspired by FL Studio and Capcut
> [!CAUTION]
> as this is a prerelease, it might crash anytime so save super frequently. also files made in this version may be incompatible with future versions

> [!IMPORTANT]
> for now you can only load projects, audio and themes by *dragging* the file *on the window*

> [!WARNING]
> **load any audio first** before editing to prevent most issues.

## Features
- realtime chord rendering
- timeline
- playback camera
- staves
- theme editor
- save/load projects obviously

## what this version does _Not_ have that you might expect
- cut/copy/paste
- undo/redo
- clip dragging (use selection, ctrl+shift+D, then delete old clip)
- rendering mode

## File formats
.shp > project  
.shm > theme  
.shx > project+theme package (not implemented yet)

## Controls
<kbd>Space</kbd> - play/pause \
<kbd>Enter</kbd> - restart \
<kbd>N</kbd> - new clip \
<kbd>Delete</kbd> - delete clip \
<kbd>Ctrl</kbd>+<kbd>D</kbd> - duplicate last clip \
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>D</kbd> - duplicate selected clip \
<kbd>,</kbd> / <kbd>.</kbd> - previous/next clip \
<kbd>←</kbd> / <kbd>→</kbd> - back/forward measure \
and some basic ones like \
<kbd>Ctrl</kbd>+<kbd>N</kbd> - new project \
<kbd>Ctrl</kbd>+<kbd>S</kbd> - save \
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd> - save as

## Formula syntax
to create chords you have[^1] to express them via a formula.[^2] its not that hard so i hope you can easily understand it\
some examples are: `2+4+` for AhChyMy, `3+2+(2+3+)`[^3] for AhChyScyLyChyli, etc\
`2+`: first you write the dimension number, then the sign (`+`/`-`). notes like this branch off the root note.\
`2+(3-)`: use ()s to inquire nesting. you can leave the ( unclosed if theres no more stuff after it\
`2+++`: reduplicate the sign, as a shorthand for `2+(2+(2+`\
`2+-`: mixing `+` and `-`, they will branch from the same parent note\
`3+2++(3+)`: nesting after reduplication also works\
`/2+` `2+'+`: apply attributes either before the number or before the sign. its up to preference (all attributes are listed below)\
`>R 2+3+`: to apply attributes to the root note, use `R`, `!` or `0`, (but `R` is recommended) like a dimension number\
`2+ 4^3v`: use `^` and `v` to offset the chord by an interval\
spaces are ignored and may be used for readability

### Note attribute list
`/` - mute (dotted note) \
`'` - tension (blue note) \
`"` - tension2 (pink note) \
`>` - bass (triangle) \
`<` - rbass (triangle, _but from the right side_)

[^1]: Visual editor akin to Ish's is planned
[^2]: Nafchaclap/chordonym support planned
[^3]: after a future fix, you will be able to put ()s midway through sigh chains, so `3+2+(3+)+` would be valid

### Formula usage in staves
declare an interval and an offset. lets take `2+ 4^` for an exmaple, as its very common.\
`2+` is the **interval**, so there will be a line every Chy starting from Ah in both directions\
`4^` is the **offset**, meaning this will move all stave lines by My.\
of course, you can mix everything up: `2+3- 5^4v`, `6+2^^^1-3v5v`, and it would still work, but those are some absurd examples i dont think anyones going to genuinely use those\
` ` leave the stave formula field empty to make a single Ah stave line\
enter `R` to make a wide one. experimentle
