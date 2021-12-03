# MacOS tips and tricks

## Always show/hide the hidden files in Finder

```shell
# To show
defaults write com.apple.Finder AppleShowAllFiles true

# To hide
defaults write com.apple.Finder AppleShowAllFiles false

# Restart Finder after that
killall Finder
```

## Delete all executable files in Mac command line

```shell
find . -maxdepth 1 -perm -111 -delete
```