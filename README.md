# mac
Personal guide for setting up a mac

## Step 1: Install macOS
I highly recommend to start fresh with a clean install of the latest version of macOS. Check [here](https://support.apple.com/en-ph/HT204904) for the latest guide on how to do so.

## Step 2: Download and Install XCode
You can download and install XCode from the Mac App Store. Just search for "xcode" and it should come up as the first result.

**Note: Before proceeding to the next step, open XCode after installation as it will install additional tools, I also recommend to restart your mac after.**

## Step 3: Install [Homebrew](https://brew.sh/) and command line tools
Get [Homebrew](https://brew.sh/) which is a package manager for macOS, and install these essential command line tools first:
``` sh
brew install git
brew install wget
brew install node
```

## Step 4: Configure Terminal
1. Install iTerm2
    ``` sh
    brew tap cask
    brew cask install iterm2
    ```
1. Using iTerm2, install [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh). **Be sure to accept change into using Z shell (zsh)**
3. Install themes **TODO**
4. Install plugins **TODO**
5. Install zsh profile **TODO**

## Step 5: Install Brewfile
1. Install Homebrew tap **TODO**
    ``` sh
    brew tap Homebrew/bundle
    ```
2. Install Brewfile **TODO**

## Step 6: Configure editors
1. VSCode
2. Atom
3. Sublime


### Credits
- [laptop](https://github.com/thoughtbot/laptop)
- [mac_os](https://github.com/bkuhlmann/mac_os)
- [mac_os-config](https://github.com/bkuhlmann/mac_os-config)
