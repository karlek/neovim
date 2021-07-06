[![Neovim](https://raw.githubusercontent.com/neovim/neovim.github.io/master/logos/neovim-logo-300x87.png)](https://neovim.io)

Yo!

This is my ugly fork where I try if it's possible to add a histogram feature for
key presses / mappings.

The idea is a spin-off from IntelliJ's add-on which suggests key bindings for
tasks that are performed inefficiently.

A successful implementation would enlighten users what bad habits they have (I
assume `j`/`k` abusage will be highlighted) and suggestions/learnings are
presented.

## Background

My knowledge of Vim internals is non-existent, so this project is currently
being developed similarly to a random walk.

Right now I'm investigating/studying:

- `state_enter`
- `[mode]_execute`
- `src/nvim/README.md`
- Can't I just hook a central point where mappings are parsed instead of where
  key presses are parsed to actions, seems my first poc is one level too low down
  the hierarchy?

## Roadmap

- Level 1: Log each key press to CSV
- Level 2: Log executed mappings to CSV
- Level 3: Log plugin mappings to CSV
- Level 4: Log commands (:) & searches
- Level 5: Somewhat productify with sqlite / representation layer

