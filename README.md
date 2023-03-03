# Developer Apps | Utilities | Educational Links | and more...

- [Terminal Utilities](#terminal-utilities)
- [Educational Links](#educational-links)
- [Apps](#apps)
- [IDEs](#ides)
- [Tools](#tools)
- [MacOS Specific Apps](#macos-specific-apps)
- [MacOS Local Dev Setup](#macos-local-dev-setup)

## Terminal Utilities

- [Bashrc Generator](http://bashrcgenerator.com/) - Generate your .bashrc/PS1 bash prompt easily with a drag and drop interface.
- [Doitlive](https://github.com/sloria/doitlive) - Tool reads a file of shell commands and replays them in a fake terminal session for live presentations.
- [GoAccess](https://github.com/allinurl/goaccess) - Real-time web log analyzer that provides HTTP statistics for servers via terminal and browser for *nix systems. 
- [The Fuck](https://github.com/nvbn/thefuck) - Corrects errors in previous console commands.

## Educational Links

- [Awesome](https://github.com/sindresorhus/awesome) - Awesome lists about all kinds of interesting topics.
- [Computer Things Explained](https://jvns.ca/) - Learn more about computer tools, networking, containers, etc. 
- [Computer Zines](https://wizardzines.com/) - Useful programming comics.
- [How HTTP Works](https://howhttps.works/) - Explanation of why HTTPS is crucial for the future of the web and how it all works together.

## Apps 

- [Chrome Browser](https://www.google.com/chrome/)
    - [OneTab](https://chrome.google.com/webstore/detail/onetab/chphlpgkkbolifaimnlloiipkdnihall?hl=en) - allows you to quickly close out your tabs, categorize them into lists, and reopen them at a later time, saving you a lot of memory
    - [Momentum](https://momentumdash.com/) - personal touch to new Chrome tabs
    - [JSON Viewer](https://chrome.google.com/webstore/detail/json-viewer/gbmdgpbipfallnflgajpaliibnhdgobh?hl=en-US)
    - [uBlock Origin](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm?hl=en)
    - [Encoder / Decoder](https://chrome.google.com/webstore/detail/encoder-decoder/mjcdbmdlmjbjmpenpepgcpnmapclkaah?hl=en)
    - [Eye Dropper](https://chrome.google.com/webstore/detail/eye-dropper/hmdcmlfkchdmnmnmheododdhjedfccka?hl=en)
- [Brave Browser](https://brave.com/download/) - No ads
- [Sublime](https://www.sublimetext.com/) - Text Editor 
    - Install package control > material theme > set theme
- [Google Drive](https://www.google.com/drive/download/) - Google drive as a file helper 
- [Beyond Compare](https://www.scootersoftware.com/) - File / folder comparison tool 
- [Postman](https://www.postman.com/) - REST API Client
- [Docker](https://www.docker.com/products/docker-desktop/) - Container deployment

## IDEs

- [IntelliJ](https://www.jetbrains.com/idea/) - Ultimate Edition
- [VS Code](https://code.visualstudio.com/)

## Tools

- [Create UML diagrams, mindmaps, tree diagrams, flowcharts, network diagrams](https://www.diagrams.net/)

## MacOS Specific Apps

- [Albert](https://www.alfredapp.com/) - Better version of Spotlight
    - [Setup to open using cmd + space](https://www.alfredapp.com/help/troubleshooting/cmd-space/)
- [Hidden Bar](https://apps.apple.com/us/app/hidden-bar/id1452453066?mt=12) - Hide menu bar items for a clean look
- [Calibre](https://calibre-ebook.com/) - Manage e-books for Kindle, etc
- [Alt Tab](https://alt-tab-macos.netlify.app/) - Better version of alt-tab
- [App Cleaner](https://freemacsoft.net/appcleaner/) - Remove lingering files from apps 
- [Gifski](https://apps.apple.com/us/app/gifski/id1351639930?mt=12) - Convert videos to gifs 
- [Spectacle](https://www.spectacleapp.com/) - Move and resize windows
- [CopyClip](https://apps.apple.com/us/app/copyclip-clipboard-history/id595191960?mt=12) - Manage clipboard
- [KeepingYouAwake](https://keepingyouawake.app/) - Prevents your Mac from going to sleep 

## MacOS Local Dev Setup

```
# install homebrew
xcode-select --install
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# install tools via brew
- brew install
    - git
        - setup .gitconfig --> git config --global --edit
            [user]
            name = Zarin Lokhandwala
            email = zelok786@gmail.com
    - maven
    - wget
    - java
        - https://johnathangilday.com/blog/macos-homebrew-openjdk/
            - export JAVA_HOME=$(/usr/libexec/java_home -v 11)
            - path+=$JAVA_HOME/bin
        - https://gist.github.com/gwpantazes/50810d5635fc2e053ad117b39b597a14
    - python@3.10
        - export PATH="/usr/local/opt/python@3.10/bin:$PATH"
	    - install virtualenv
            - /usr/local/opt/python@3.10/bin/pip3 install virtualenv
	    - how to use venv
            - https://gist.github.com/pandafulmanda/730a9355e088a9970b18275cb9eadef3

# install mongodb
- https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-os-x/
- create alias
    - brew services start mongodb/brew/mongodb-community

# install zsh 
- https://ohmyz.sh/#install
- change shell if need be
    - chsh -s $(which zsh)
- use powerlevel10k
    - https://www.linkedin.com/pulse/5min-guide-awesome-terminal-rafa-oliveira/
	    - git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
	    - ZSH_THEME="powerlevel10k/powerlevel10k"

- plugins for zsh
    -  https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md	
        plugins=(
            git sublime vscode jsontools 
        )	

# setup SSH keys
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh

# setup golang 
- https://jimkang.medium.com/install-go-on-mac-with-homebrew-5fa421fc55f5
- brew install golang
    - mkdir -p $HOME/go/{bin,src,pkg}
    - in .zshrc add:
        export GOPATH=$HOME/go
        export GOROOT="$(brew --prefix golang)/libexec"
        export PATH="$PATH:${GOPATH}/bin:${GOROOT}/bin"
```