
* Install Brew from terminal - takes 2 minutes
* Homebrew-Cask extends Homebrew 
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

brew tap caskroom/cask
# my fav, like terminator - multi panel terminals
brew cask install iterm2
```

* Cmd Tools
```bash
brew install watch 
brew install wget 
brew install curl 
brew install tar 
brew install zip 
brew install unzip
brew install git
brew install python
brew install jq
brew install go  
brew install openshift-cli 
brew install gnu-sed

brew cask install textmate
brew install fswatch

watch --version
wget --version
curl --version
tar --version
zip --version
git --version
python --version
jq --version
go version
oc version

ls -al /usr/local/opt/gnu-sed/libexec/gnubin
PATH="/usr/local/opt/gnu-sed/libexec/gnubin:$PATH"
```
* customize gedit following http://www.linuxandubuntu.com/home/how-to-make-gedit-more-programmer-friendly

```text
select Preferences - Under View tab tick:
# Display line numbers
# Highlight current line
# Highlight matching brackets
# Under Font & Colors tab:

Choose your own color scheme; one that suits your taste. However, heavy programmers usually tend to go for the dark color scheme as its easier on eyes.
Finally under Plugins tick:
# External Tools
# Snippets

```
* we will install node using nvm later
* (optional) follow to get python3 and make it default https://wsvincent.com/install-python3-mac/
```bash
brew install python3
python3 --version
phyton3

```

### Install httpie
```bash
brew install httpie
# test using
http put httpbin.org/put hello=world
```

## SDKMAN - - My favourite
* https://sdkman.io/install
* read usage - https://sdkman.io/usage
* For later easy ref from your home dir to all SDKs , you can create a friendly symlink as
* ln -s /Users/jsmit/.sdkman/candidates ~/SDK_HOME
* Note: jsmit = replace with your username
```bash
curl -s "https://get.sdkman.io" | bash
#open new window run
source "/Users/rajeshpradeshik/.sdkman/bin/sdkman-init.sh"
sdk version

sdk version

sdk list java | grep 8
sdk install java 8.0.265.hs-adpt
sdk install java 11.0.8.hs-adpt 

sdk install maven 3.6.3
sdk install ant 1.10.8
sdk install sbt 1.3.13
sdk install gradle 6.6.1

sdk install scala 2.13.3
sdk install groovy 3.0.5
sdk install spark 2.4.6

# set defaults
sdk default java 8.0.265.hs-adpt

sdk default maven 3.6.3
sdk default ant 1.10.8
sdk default sbt 1.3.13
sdk default gradle 6.6.1

sdk default scala 2.13.3
sdk default groovy 3.0.5
sdk default spark 2.4.6
```

### Setup SDKMAN init at bashrc
* copy .bashrc from github to ~/.bashrc
* append following at top of ~/.bash_profile
```bash
if [ -f ~/.bashrc ]; then
   source ~/.bashrc
fi

# confirm following exists at end of .bash_profileexport SDKMAN_DIR="/Users/rajeshpradeshik/.sdkman"
[[ -s "/Users/rajeshpradeshik/.sdkman/bin/sdkman-init.sh" ]] && source "/Users/rajeshpradeshik/.sdkman/bin/sdkman-init.sh"

# open new terminal and test bashrc and bash_profile all working good? as follows:
env | grep HOME
ln -s $HOME/.sdkman/candidates ~/SDKMAN_ROOT
```

## Customize GitPrompt
* followed from https://github.com/magicmonty/bash-git-prompt
```bash
cd ~
git clone https://github.com/magicmonty/bash-git-prompt.git ~/.bash-git-prompt --depth=1

# confirm following is already added to .bashrc
if [ -f "$HOME/.bash-git-prompt/gitprompt.sh" ]; then
    GIT_PROMPT_ONLY_IN_REPO=1
    source $HOME/.bash-git-prompt/gitprompt.sh
fi

# test its working by changing into git repo sample
cd ~/.bash-git-prompt
```

### Customize terminal
* Choose "Terminal" from top menu bar - Preferences
* In Profiles-tab choose "Red Sands" and select "default button" at bottom of list to save selection.
* change font-size to 14; 
* cursor block and Blink enable; 
* click on Brown Bg Color to pop-up set Opaque of BG to 95%
* window tab - change window size from 80x24 to 90x24

### Customize iTerm2 - My favourite
* https://iterm2.com/features.html
* brew cask install iterm2
* Customize using https://sourabhbajaj.com/mac-setup/iTerm/
* text-thin Strokes=dropDown alwyas;changeFont=13pt;BlinkingCurson=check
* export CLICOLOR=1 line to your ~/.bash_profile file for nice coloring of listings
* Create Launch icon in Dock for iterm2

#### Edit "Default" Profile
* Colors tab - enable: smart box cursor color; ColorPresets: choose "Solorized Dark"
* Text Tab: Cursor=Box; Blinking=Yes; Use thin strokes blah=Always (from dropdown); change font to 16, since keepin gthis on 4k monitor
* Window Tab: Size change from : 80x24 to 120x24

### Git Password cache
```bash
# for one hour it is 3600, for 12 hours=43200
git config --global credential.helper 'cache --timeout 43200'
```

### Install UnArchiver
* https://apps.apple.com/app/the-unarchiver/id425424353?ls=1&mt=12

### Install Postman
* https://www.getpostman.com/downloads/

### Install Wireshark (optional)
* from https://www.wireshark.org/download.html