## Dotfiles for my [fish shell](http://fish.sh) :fish:

[![](https://img.shields.io/github/license/mbbroberg/fishfiles?style=flat-square)](https://www.tldrlegal.com/l/lgpl-3.0)
[![](https://img.shields.io/twitter/follow/mbbroberg?color=blue&label=ask%20me%20about%20dotfiles&style=flat-square)](https://twitter.com/mbbroberg)

## Update

I no longer need this repository. My [new dotfile setup](https://github.com/mbbroberg/dotfiles) uses [chezmoi](https://github.com/twpayne/chezmoi) and I now track my fisher fishfile in the same directory structure.

## Original 

This repository is my version of [laughedelic/fish](https://github.com/laughedelic/fish). Here's how it works: 

I'm using the [fisher](https://github.com/jorgebucaran/fisher) plugin manager. It creates symlinks for _all_ plugin functions in `~/.config/fish/functions/`, so it's rather inconvenient to store your own functions at the same place. This is why I moved my functions and the config out and installed it as a plugin:

- I create my functions in `~/Develop/mbbroberg/fishfiles/functions/`
- I put my config (`~/.config/fish/config.fish`) as a snippet in `~/Develop/mbbroberg/fishfiles/conf.d/`
- then just I install it with fisher: `fisher install ~/Develop/mbbroberg/fishfiles`
- every time I add new stuff, I do `fisher update ~/Develop/mbbroberg/fishfiles` (or `fisher rm` + `fisher install`)

It's quite convenient way of managing custom fish configuration, because it allows you to have your own things separate from the fish/fisher autogenerated stuff. 

### Limitations

For now, if you use `alias -s` to save functions on the fly, you'll need to manually copy them to this directory to back them up. 
