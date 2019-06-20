# Using Meld merging tool on Mac Mojave

```
brew tap homebrew/cask
brew cask install meld
```

* If meld doesn't start while executing from terminal, try [this](https://github.com/yousseb/meld/issues/70#issuecomment-479199105):

Modify the `/usr/local/Caskroom/meld/3.19.2-r6,osx-15/meld.wrapper.sh` script installed by brew to the following

```
#!/bin/sh
rm -rf ~/Library/Saved\ Application\ State/org.gnome.meld.savedState
exec '/Applications/Meld.app/Contents/MacOS/Meld' "$@"
```
