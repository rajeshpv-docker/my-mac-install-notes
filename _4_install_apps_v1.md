### Install Slack 
* from apps.apple.com using appleid r8@gmail/A_41
* use channel= xyinc.slack.com login with r.p@xy.com/A_41

### Firefox browser
* Follow steps at https://support.mozilla.org/en-US/kb/how-download-and-install-firefox-mac
* After install login into firefox account to get bookmarks synced from old
* https://accounts.firefox.com/ r8@gmail/A_41 to sync book mark

### Google Chrome Browser
* follow steps at https://support.google.com/chrome/answer/95346?co=GENIE.Platform%3DDesktop&hl=en-GB
* Login with gmail account it will sync bookmarks and extensions between old/new for you. !

### Mongo Client 
* get latest download link from https://nosqlbooster.com/downloads
```bash
cd ~/Downloads
wget  https://nosqlbooster.com/s3/download/releasesv5/nosqlbooster4mongo-5.1.14.dmg
# open finder into Downloads, double click and copy the app in to /Applications
# later eject/trash the downloaded image
# create app launch Icon for NoSqlBooster
# enter license if you have one
```

### (optional) DBeaver - My Fav
* dbeaver.io https://dbeaver.io/files/dbeaver-ce-latest-macos.dmg

### (optional) SoapUI
* https://www.soapui.org/getting-started/installing-soapui/installing-on-mac.html
* https://www.soapui.org/downloads/latest-release.html

### (optional) Postman - My Fav
* https://www.getpostman.com/apps

### (optional) To Map Shared folder - Goto Finder App
* Go “Gonnect to Server” from secure get ur shared folder on windows NAS
* \\nas05059pn\homedirs_nc004\rpradesh

### Install CE version of IntelliJ
* http://www.jetbrains.com/idea/download/download-thanks.html?platform=mac&code=IIC
* In first flash/pop-up window , there is "configure" at bottom of dialog
* Install plugins choosing from drop down - scala, LiveEditTool, Bashsupport, Docker Integration, Markdown support, XPath-SxltViewer

### Customize IntelliJ
* Follow https://www.jetbrains.com/help/idea/sdk.html Configure Java SDK 11 as default
* By Choosing "Structure for New Projects" and select "SDK's" below Platform Settings
* To set default Maven Runner - choose from. "Configure" CHOOSE - "Run Config templates for new Projects"
* Select Maven from the left list - select "General" from right tab
  * check on- always update snapshots
  * Uncheck - "Use Project Settings" - point to SDKMAN Maven 3.6.1
* Choose "Edit VM Options" to change Xms and Xmx to 1128 and 1750m and save it, it gets saved to ~/Library/Preferences/IdeaIC2019.2/idea.vmoptions
* Appearance & Behavior
* Appearance 
* Change custom font to - .SFNSText-regular and 14pt
* Enable - Show Memory Indicator
* Editor - font change to Menlo 16pt
* Editor - General - Uncheck - Copy as rich text by default
* For "Profile" Default IDE, uncheck "Spelling" to off

### Docker Install
* Login docker using docker hub id rajeshpv/a1
* Goto https://hub.docker.com/editions/community/docker-ce-desktop-mac
* Click on blue button "Focker for Mac" stable version
* Then double click docker.img in ~/Downlods hence copy to Applications like any other App
* Goto ~/Application in Finder and double-click Docker icon, it will prompt for admin password
* Then you should see "Whale" icon running in top menu-bar
* Open new terminal run 
* docker version
* docker run hello-world

### Install NVM
* https://github.com/nvm-sh/nvm

```bash
mkdir /Users/$USER/.nvm
# make sure scripts are put in ~/.bashrc as above github wiki says
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash

# open new terminal and run 
nvm --version

# Let us list available node versions
nvm ls-remote v10.16.3
nvm ls-remote v12.8.1

nvm install v10.16.3
node -v
npm -v

nvm install v12.8.1
node -v
npm -v

```

### Install VSCode
* To Install Plugins followed https://dev.to/deepu105/my-vs-code-setup-making-the-most-out-of-vs-code-4enl
* To Chnge font size in vscode https://stackoverflow.com/questions/33701933/how-do-i-change-visual-studio-code-environments-font-size

```bash
brew cask install visual-studio-code

# excel and csv viewer
code --install-extension grapecity.gc-excelviewer
```

### Plugins install, followed from https://dev.to/deepu105/my-vs-code-setup-making-the-most-out-of-vs-code-4enl
* JetBrains IDE Keymap - I am used to Idea so (install from code ide ) = code --install-extension sudox.vscode-jetbrains-keybindings
    - https://code.visualstudio.com/api/references/contribution-points#contributeskeybindings
* Close HTML/XML tag =   code --install-extension Compulim.compulim-vscode-closetag 
* ESLint = code --install-extension dbaeumer.vscode-eslint
* Prettier = code --install-extension esbenp.prettier-vscode
* (optional) JS Prettier = code --install-extension dai-shi.vscode-es-beautifier
* (optional) Adds Java language support. > code --install-extension redhat.java
* (optional) Adds lightweight Java debugging support. > code --install-extension vscjava.vscode-java-debug
* Docker = code --install-extension ms-azuretools.vscode-docker
* Terraform = code --install-extension mauve.terraform
* Markdown = code --install-extension yzhang.markdown-all-in-one
* PlantUML = code --install-extension jebbs.plantuml
* Yaml = code --install-extension redhat.vscode-yaml
* ChangeCase = code --install-extension wmaurer.change-case
* (optional) Test Explorer UI = code --install-extension hbenl.vscode-test-explorer
* Git supercharged = code --install-extension eamodio.gitlens GitLens — 
    - USe this link to hide GitLens extra anno "GitLens: Open Settings" - https://github.com/eamodio/vscode-gitlens/issues/54#issuecomment-391221230 disable "Current Line Blame" and "Code Lens" section
    - https://stackoverflow.com/questions/45858604/how-can-one-discard-individual-changes-in-a-file-in-visual-studio-code

### Bash Upgrade to latest
* Followed from https://itnext.io/upgrading-bash-on-macos-7138bd1066ba

```bash
bash --version
brew install bash
# To verify the installation,
which -a bash
# check new one is active
bash --version

# add shell to whitelist at end - /usr/local/bin/bash
sudo vi /etc/shells

# Set Default Shell for User
chsh -s /usr/local/bin/bash
# Set Default Shell for Root
sudo chsh -s /usr/local/bin/bash
# reopen new terminal window and test
echo $BASH_VERSION

# the shebang line like this:
# #!/usr/local/bin/bash
echo $BASH_VERSION

## or best
# #!/usr/bin/env bash
echo $BASH_VERSION

``` 
-rw-r--r--   1 rajeshpradeshik  staff  1166 Sep 30 15:42 _1_pre_requisite-v1.md
-rw-r--r--   1 rajeshpradeshik  staff  3096 Sep 30 15:42 _2_customize_system_prefs.md
-rw-r--r--   1 rajeshpradeshik  staff  4759 Sep 30 15:42 _3_install_tools_v1.md
-rw-r--r--   1 rajeshpradeshik  staff  6298 Sep 30 15:42 _4_install_apps_v1.md