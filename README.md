# Dotfiles for Ubuntu 💜

My preferred starting configuration for Ubuntu Desktop. Current version 20.04 Focal Fossa.

The [installation script included](https://github.com/victoriadrake/dotfiles/blob/ubuntu-20.04/scripts/install.sh) will install a suggested serving of programs and applications, found within the `scripts/` directory. Please verify that you want these before running the script.

Add or delete files in `scripts/install.sh` and `scripts/programs/` to modify your installation.


## Included `scripts/`

- `symlink.sh` sets up symbolic links in `$HOME`
- `aptinstall.sh` owns Ubuntu repository installs
- `programs.sh` leverages progressive command line installation of other software
- `desktop.sh` champions granular executive desktop environment settings
- `setup.sh` facilitates the scalable and proactive deliverables of running all the scripts and `apt upgrade`

## Usage

After installing your fresh OS, do:

[Create your SSH key](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh)

```sh
git clone git@github.com:jonyeezs/dotfiles.git

# Or use HTTPS
git clone https://github.com/jonyeezs/dotfiles.git
```

You may optionally like to pass the `--depth` argument to clone only a few of the [most recent commits](https://github.com/victoriadrake/dotfiles/commits/master).


```sh
cd dotfiles/scripts/
./setup.sh
```

Then restart your terminal to see changes, or run:

```sh
cd ~
source .bashrc
```

### Saving and loading configuration settings

Optionally, load `settings.dconf` with:

```sh
dconf load /org/gnome/ < .config/dconf/settings.dconf
```

Back up new settings with:

```sh
dconf dump /org/gnome/ > .config/dconf/settings.dconf
```

Run `man dconf` on your machine for more.

## Recommended additions

- GNOME Tweaks
- [Emoji Selector](https://extensions.gnome.org/extension/1162/emoji-selector/) ❤️✨🦄
- [Clipboard Indicator](https://extensions.gnome.org/extension/779/clipboard-indicator/)
