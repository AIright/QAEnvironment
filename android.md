## Android setup
1. `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
2. `brew cask install android-studio`
3. Run Android Studio and setup required packages
4. Update your bash/zsh profile:
```
export ANDROID_HOME="/Users/$USER/Library/Android/sdk"
export PATH="${PATH}:$ANDROID_HOME/emulator:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools"
export ANDROID_BT_VERSION="$(ls -tr $ANDROID_HOME/build-tools | sort | tail -1)"
export PATH="$PATH:$ANDROID_HOME/build-tools/$ANDROID_BT_VERSION"
```
