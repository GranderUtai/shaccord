# Shaccord
Microtonal chord visualisation program based on L4mplight's works  
interface inspired by FL Studio and Capcut

## Features
- theme editor
- i meannn

## what this version does _Not_ have what you might expect
- rendering
- stability
- clip dragging (use selection then ctrl+shift+D)
- cut/copy/paste
- undo/redo

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
<kbd>Ctrl</kbd>+<kbd>N</kbd> - save \
<kbd>Ctrl</kbd>+<kbd>S</kbd> - save \
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd> - save as

## Formula syntax
to create chords you have[^1] to express them via a formula. its not that hard so i hope you can easily understand it\
some examples are: `2+4+` for AhChyMy, `3+2+(2+3+)`[^2] for AhChyScyLyChyli, etc\
`2+` | first you write the dimension number, then the sign (`+`/`-`). notes like this branch off the root note.\
`2+(3-)` | use ()s to inquire nesting. _you can leave the ( unclosed if theres no more stuff after it, that wont affect anything._\
`2+++` | reduplicate the sign, as a shorthand for `2+(2+(2+`\
`3+2++(3+)` | nesting after reduplication also works\
`/2+` `2+'+` | apply attributes either before the number or before the sign. its up to preference (all attributes are listed below)\
`>R 2+3+` | to apply attributes to the root note, use `R` (or `!` or `0`, but `R` is recommended) like a dimension number\
`2+ 4^3v` | use `^` and `v` to offset the chord by an interval

### Note attribute list
`/` - mute (dotted note) \
`'` - tension (blue note) \
`"` - tension2 (pink note) \
`>` - bass (triangle) \
`<` - rbass (triangle, _but from the right side_)

[^1]: Nafchaclap/chordonym support planned
[^2]: after a future fix, you will be able to put ()s midway through sigh chains, so `3+2+(3+)+` would be valid
