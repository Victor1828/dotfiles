# My Dotfiles
Clone repo into new hidden directory.

```
# Use SSH (if setup)...
git clone git@github.com:Victor1828/dotfiles.git ~/.dotfiles

# Or use HTTPS and change remotes later
git clone https://github.com/Victor1828/dotfiles.git ~/.dotfiles
```

Create symlinks in the Home directory to the files in the repo.

```
# There are better and less manual ways to do this,
# investigate install scripts and bootstraping tools.

ln -s ~/.dotfiles/.zshrc ~/.zshrc
```

Install Homebrew, followed by the software listed in the Brewfile.

```
# This could also be in an install script.

# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Then pass in the Brewfile location...
brew bundle --file ~/.dotfiles/Brewfile

# ...or move to this directory first.
cd ~/.dotfiles && brew bundle
```

## TODO List
- Learn how to use **defaults** to record and restore System Preferences and other configurations.
- Organize these growing steps into multiple script files.
- Automate the symlinking and run script files with a bootstraping tool like [Dotbot](https://github.com/anishathalye/dotbot).
