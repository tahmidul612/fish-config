# Setup Fish Shell

> [Fish](https://fishshell.com/) is a smart & user-friendly command line shell for Linux, macOS, and the rest of the family. Unlike other shells, which disable certain features by default to save system resources, Fish enables all features by default—finally, a command line shell for the 90s!

A curation of plugins, prompts, and other treasures for the [friendly interactive shell](https://fishshell.com). This page is not an official Fish project. We do not to advertise for profit. Want to have your project featured here? [Send us a pull request](https://github.com/jorgebucaran/awesome-fish/fork).

## Official Resources

- [Official Site](https://fishshell.com)
- [GitHub Repository](https://github.com/fish-shell/fish-shell)
- [Try in browser!](https://rootnroll.com/d/fish-shell/) 🍤

## Community Resources

- [r/fishshell](https://www.reddit.com/r/fishshell)
- [Gitter Channel](https://gitter.im/fish-shell/fish-shell)
- [StackOverflow `#fish`](https://stackoverflow.com/questions/tagged/fish)
- [The Fish Cookbook](https://github.com/jorgebucaran/cookbook.fish) 🍣

---

## Install [Fish](https://fishshell.com) (Ubuntu)

```console
sudo apt-add-repository ppa:fish-shell/release-3
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install fish
chsh -s $(which fish)
fish_add_path -m ~/.local/bin
```

## Fonts

### [Nerd-Fonts](https://github.com/ryanoasis/nerd-fonts) - Iconic font aggregator, collection, & patcher

Install FiraCode

```console
git clone --filter=blob:none --sparse git@github.com:ryanoasis/nerd-fonts
cd nerd-fonts
git sparse-checkout add patched-fonts/FiraCode
./install.sh FiraCode
```

## Plugins

### [Fisher](https://github.com/jorgebucaran/fisher) - Manage functions, completions, bindings, and snippets from the CLI

```console
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
```

### [fzf](https://github.com/PatrickF1/fzf.fish) - Ef-🐟-ient key bindings for [`junegunn/fzf`](https://github.com/junegunn/fzf). ([Alternative](https://github.com/jethrokuan/fzf))

Install dependencies

- [fzf](https://github.com/junegunn/fzf)

```console
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

- [fd](https://github.com/sharkdp/fd)

```console
sudo apt install fd-find
ln -s $(which fdfind) ~/.local/bin/fd
```

- [bat](https://github.com/sharkdp/bat)

```console
sudo apt install bat
ln -s /usr/bin/batcat ~/.local/bin/bat
```

Finally install fzf with Fisher

```console
fisher install PatrickF1/fzf.fish
```

### [Sponge](https://github.com/andreiborisov/sponge) - Clean command history from typos automatically

```console
fisher install meaningful-ooo/sponge
```

#### ⛔ Purge only on exit

Sometimes you want to ignore `sponge_delay` variable and access the whole history of the current session. In such cases you can instruct Sponge to purge entries only on shell exit with `sponge_purge_only_on_exit` variable:

```fish
set sponge_purge_only_on_exit true
```

### [Autopair](https://github.com/jorgebucaran/autopair.fish) - Auto-complete matching pairs in the Fish command-line. ([Alternative](https://github.com/laughedelic/pisces))

```console
fisher install jorgebucaran/autopair.fish
```

### [Getopts](https://github.com/jorgebucaran/getopts.fish) - CLI options parser (alternative to the [`argparse`](https://fishshell.com/docs/current/cmds/argparse.html) builtin)

```console
fisher install jorgebucaran/getopts.fish
```

### [Virtualfish](https://github.com/adambrenecki/virtualfish) - Virtualenv wrapper

1. `python -m pip install virtualfish`
2. `vf install`
3. [Add VirtualFish to your prompt](https://virtualfish.readthedocs.org/en/latest/install.html#customizing-your-fish-prompt)
4. `vf new myvirtualenv; which python`

## Prompts

### [Tide](https://github.com/IlanCosman/tide) - A modern prompt manager for Fish

```console
fisher install IlanCosman/tide@v5
```
