# mac :computer:
Personal guide for setting up a mac

## Step 1: Install macOS
I highly recommend to start fresh with a clean install of the latest version of macOS. Check [here](https://support.apple.com/en-ph/HT204904) for the latest guide on how to do so.


## Step 2: Download and Install XCode
- You can download and install XCode from the Mac App Store. Just search for "xcode" and it should come up as the first result.

    **NOTE: Before proceeding to the next step, open XCode after installation as it will install additional tools, I also recommend to restart your mac after.**
- Install XCode command line tools
    ```sh
    xcode-select --install
    ```

## Step 3: Install [Homebrew](https://brew.sh/)
- Get [Homebrew](https://brew.sh/) which is a package manager for macOS.

## Step 4: Configure Terminal
1. Install iTerm2
    ``` sh
    brew tap cask
    brew install iterm2 --cask
    ```
2. Using iTerm2, install [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh)

    **NOTE: Be sure to accept change into using Z shell (zsh)**
3. Set iTerm as default terminal
4. Install iTerm shell integrations


## Step 5: Install Essential Command Line Tools
``` sh
brew install git
brew install node
brew install mas
brew install m-cli
```

## Step 6: Install and configure [asdf](https://asdf-vm.com/#/)
1. Install `asdf`
    ```sh
    # https://asdf-vm.com/#/core-manage-asdf
    brew install asdf

    # Add to shell
    echo -e "\n. $(brew --prefix asdf)/asdf.sh" >> ~/.zshrc
    ```
1. Install asdf plugins
    ```sh
    asdf plugin-add nodejs
    asdf plugin-add python
    asdf plugin-add java https://github.com/halcyon/asdf-java.git
    ```
2. Install latest (stable) versions
    ```sh
    asdf install nodejs latest:14
    asdf install python latest
    # Java 8 is required for Cordova/Ionic
    asdf install java adoptopenjdk-8.0.275+1
    ```
3. Set global plugin versions
    ```sh
    asdf global nodejs system
    asdf global python system
    # Add to .zshcrc - . ~/.asdf/plugins/java/set-java-home.zsh
    asdf global java adoptopenjdk-8.0.275+1
    ```

## Step 7: Install zsh themes and plugins
1. Install [pure](https://github.com/sindresorhus/pure)
    ```sh
    npm install --global pure-prompt
    ```
2. Configure `pure` integration to `oh-my-zsh`
    - https://github.com/sindresorhus/pure#oh-my-zsh
3. Install fonts
    ```sh
    brew install font-hack-nerd-font --cask
    brew install font-inconsolata-dz-for-powerline --cask
    ```
4. Install iTerm Profile
    - Filename: `itermprofiles.json`
    - Guide: https://stackoverflow.com/questions/35211565/how-do-i-import-an-iterm2-profile
5. Set iTerm advanced settings
    - General -> Height of top and bottom margins in terminal panes = 12
    - General -> Width of left and right margins in terminal panes = 20
6. Install zsh plugins
    - https://github.com/zsh-users/zsh-autosuggestions
    - https://github.com/zsh-users/zsh-syntax-highlighting
7. Check the `.zshrc` file for other configurations
8. Restart iTerm for the changes to take effect


## Step 8: Install Casks
```
# browsers
brew install google-chrome --cask
brew install brave-browser --cask
brew install safari-technology-preview --cask
brew install firefox-developer-edition --cask

# developer tools
brew install docker --cask
brew install postico --cask
brew install mysqlworkbench --cask
brew install ngrok --cask
brew install postman --cask
brew install gradle
brew install android-sdk --cask

# text editors
brew install visual-studio-code --cask
brew install sublime-text --cask

# utilities
brew install kap --cask
brew install 1password --cask
brew install omnidisksweeper --cask
brew install teamviewer --cask
brew install android-file-transfer --cask

# communications
brew install franz --cask
brew install discord --cask
brew install skype --cask

# drivers
brew tap homebrew/cask-drivers
brew install logitech-g-hub --cask
brew install blue-sherpa --cask
sudo installer -pkg /usr/local/Caskroom/blue-sherpa/20200810/BlueSherpa-20200810.pkg -target /Applications

# etc
brew install steam --cask
brew install spotify --cask
brew install vlc --cask

# gems
gem install colorls
```

## Step 9: Install App Store Apps
```sh
mas install 425955336 # Skitch
mas install 1037126344 # Apple Configurator 2
mas install 803453959 # Slack
mas install 497799835 # Xcode
mas install 441258766 # Magnet
mas install 425424353 # The Unarchiver
mas install 409203825 # Numbers
mas install 409183694 # Keynote
mas install 409201541 # Pages
```

## Step 10: Configure git
1. Setup ssh keys - https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
2. Copy `.gitconfig` and `.gitignore_global` files into home directory
3. Update `.gitconfig/user.email`


## Step 11: Configure editors
1. Visual Studio Code
    - Sync settings via https://code.visualstudio.com/docs/editor/settings-sync
    - https://shageevan.medium.com/vs-codes-in-built-terminal-is-slow-or-laggy-on-macos-big-sur-d5867a7d9771
2. Sublime Text


## Step 12: Setup developer tools
1. Setup java/android development tools
    - Install tools
        ```sh
        # Install
        sdkmanager "tools" "platform-tools" "extras;android;m2repository" "extras;google;m2repository" "build-tools;30.0.3" "platforms;android-30"

        # Accept licenses
        sdkmanager --licenses
        ```
    - Set environment variables
        ```sh
        # ~/.zshrc
        export ANDROID_HOME="/usr/local/share/android-sdk"
        export ANDROID_SDK_ROOT="/usr/local/share/android-sdk"
        export ANDROID_HOME="/usr/local/share/android-sdk"
        export ANDROID_SDK_ROOT="/usr/local/share/android-sdk"
        export PATH=$ANDROID_HOME/tools:$PATH
        export PATH=$ANDROID_HOME/platform-tools:$PATH
        export PATH=$ANDROID_HOME/build-tools/30.0.3:$PATH
        ```


## Step 13: Configure browsers


## Step 14: System Settings and Background
- https://github.com/rgcr/m-cli
- https://github.com/herrbischoff/awesome-macos-command-line


## Step 15: Email and Calendar


### Roadmap
1. Incorporate homebrew/bundle
    - NOTE: Initial Brewfile is included in the repo

### Credits
- [laptop](https://github.com/thoughtbot/laptop)
- [mac_os](https://github.com/bkuhlmann/mac_os)
- [mac_os-config](https://github.com/bkuhlmann/mac_os-config)
