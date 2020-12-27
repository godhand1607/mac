# mac
Personal guide for setting up a mac

## Step 1: Install macOS
I highly recommend to start fresh with a clean install of the latest version of macOS. Check [here](https://support.apple.com/en-ph/HT204904) for the latest guide on how to do so.

## Step 2: Download and Install XCode
You can download and install XCode from the Mac App Store. Just search for "xcode" and it should come up as the first result.

**Note: Before proceeding to the next step, open XCode after installation as it will install additional tools, I also recommend to restart your mac after.**

## Step 3: Install [Homebrew](https://brew.sh/) and command line tools
Get [Homebrew](https://brew.sh/) which is a package manager for macOS.

## Step 4: Configure Terminal
1. Install iTerm2
    ``` sh
    brew tap cask
    brew cask install iterm2
    ```
2. Using iTerm2, install [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh). **Be sure to accept change into using Z shell (zsh)**

## Step 5: Install CLI apps
``` sh
brew install git
brew install wget
brew install node
brew install m-cli
```

## Step 6: Install zsh themes and plugins
1. Install themes **TODO**
2. Install plugins **TODO**
3. Install zsh profile **TODO**


## Step 7: Install casks and app store apps
# TODO

## Step 8: Install Brewfile
1. Install Homebrew tap **TODO**
    ``` sh
    brew tap Homebrew/bundle
    ```
2. Install Brewfile **TODO**

## Step 9: Configure git
https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

## Step 10: Configure editors
1. VSCode
2. Sublime



### Credits
- [laptop](https://github.com/thoughtbot/laptop)
- [mac_os](https://github.com/bkuhlmann/mac_os)
- [mac_os-config](https://github.com/bkuhlmann/mac_os-config)
