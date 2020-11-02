## Android SDK setup for Mac
1. Install homebrew: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
2. Install Android Studio: `brew cask install android-studio`
3. Run Android Studio and setup required packages
4. Update your bash/zsh profile:
```
export ANDROID_HOME="/Users/$USER/Library/Android/sdk"
export PATH="${PATH}:$ANDROID_HOME/emulator:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools"
export ANDROID_BT_VERSION="$(ls -tr $ANDROID_HOME/build-tools | sort | tail -1)"
export PATH="$PATH:$ANDROID_HOME/build-tools/$ANDROID_BT_VERSION"
```
## Issues
### Android Emulator: network doesn't work on Mac
1. GoTo Apple Icon -> System Preferences -> Network
2. Click on the gear icon and select 'Set Service Order'
3. Bring an active interface before other interfaces.
4. Restart the Android Emulator.
