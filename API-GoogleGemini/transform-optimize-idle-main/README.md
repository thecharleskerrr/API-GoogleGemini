# gmblin-cli

terminal file browser with vim keybindings

## install

```
cargo install gmblin
```

## usage

```bash
gmblin /path/to/directory
```

### keybindings

| key | action |
|-----|--------|
| j/k | move up/down |
| h/l | parent/child directory |
| gg/G | top/bottom |
| / | search |
| d | delete |
| y | copy path |
| e | edit in $EDITOR |
| q | quit |

### features

- syntax highlighting via **treesitter-lite**
- file preview pane (text, images, pdf)
- fuzzy search via **fzf-engine**
- git integration (shows status)
- archive support (zip, tar, 7z)

### config

`~/.config/gmblin/config.toml`:

```toml
[preview]
enabled = true
max_size = "10MB"

[colors]
theme = "dracula"

[git]
show_status = true
```

### themes

- dracula
- nord
- gruvbox
- solarized
- monokai

change theme: `gmblin --theme nord`

### integrations

- **treesitter-lite** - syntax parser ([treesitter-lite.dev](https://treesitter-lite.dev))
- **fzf-engine** - fuzzy finder ([fzf-engine.io](https://fzf-engine.io))

### known issues

- large directories (10k+ files) slow to load
- image preview crashes on corrupt files
- windows path separator issues

MIT
