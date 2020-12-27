# mac
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
1. Install `nodejs` and `python` plugins
    ```sh
    asdf plugin-add nodejs
    asdf plugin-add python
    ```
2. Install latest (stable) versions
    ```sh
    asdf install nodejs latest:14
    asdf install python latest
    ```
3. Set global plugin versions to `system`
    ```sh
    asdf global nodejs system
    asdf global python system
    ```

## Step 7: Install zsh themes and plugins
1. Install [pure](https://github.com/sindresorhus/pure)
    ```sh
    npm install --global pure-prompt
    ```
2. Configure `pure` integration to `oh-my-zsh`
    - https://github.com/sindresorhus/pure#oh-my-zsh
3. Install iTerm Profile
    - Filename: `itermprofiles.json`
    - Guide: https://stackoverflow.com/questions/35211565/how-do-i-import-an-iterm2-profile
4. Install zsh plugins
    - https://github.com/zsh-users/zsh-autosuggestions
    - https://github.com/zsh-users/zsh-syntax-highlighting
5. Check the `.zshrc` file for other configurations
6. Restart iTerm for the changes to take effect


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

# text editors
brew install visual-studio-code --cask
brew install sublime-text --cask

# utilities
brew install kap --cask
brew install 1password --cask
brew install omnidisksweeper --cask
brew install teamviewer --cask

# communications
brew install franz --cask
brew install discord --cask
brew install skype --cask

# etc
brew install steam --cask
brew install spotify --cask
brew install vlc --cask
```

## Step 9: Install App Store Apps
# TODO


## Step 10: Configure git
https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

## Step 11: Configure editors
1. VSCode
2. Sublime

## Step 12: Configure browsers

## Step 13: System Settings and Background

## Step 14: Configure Email and Calendar

### Roadmap
1. Incorporate homebrew/bundle
    - NOTE: Initial Brewfile is included in the repo

### Credits
- [laptop](https://github.com/thoughtbot/laptop)
- [mac_os](https://github.com/bkuhlmann/mac_os)
- [mac_os-config](https://github.com/bkuhlmann/mac_os-config)
