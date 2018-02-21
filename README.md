# Software Engineering Tools I use

This repo are my personal setup steps for getting a new machine ready for coding, blogs I read, podcasts I listen to, and other things relating to my career. The tools are node-leaning beacuse javascript is typically what I use the most.

* [OSX Setup](#osx-setup)
* iOS Setup
* Ryan's Recommended Reading
* Programming Podcasts
* Music For Getting Stuff Done
* Home Network

## OSX Setup

### System update

You should always keep any system you're using up to date. Yes, sometimes there are regression bugs (thanks apple) but in general it's the best way to protect yourself from malware. Stop using windows XP because your friends friend once said that 10 is insecure.

To update OSX:

*Apple Icon > Software Update...*

### System preferences.

Basic system preferences that I always always change.

Trackpad
  Point & Click
  * Secondary click ON
  * Tap to click OFF
  * Tracking speed FAST

  Scroll & Zoom
  * Natural Scrolling OFF

  More Gestures
  * Swipe between pages OFF (causes me to sometimes go back in browser by accident)

Keyboard
  * Key Repeat FASTEST
  * Delay Until Repeat SHORT

Dock
  (I almost never use the dock so I make it as out of the way as possible)
  * Size SMALL
  * Magnification OFF
  * Automatically hide and show the Dock ON 

### Firefox

My favorite browser is Firefox. Ever since they release FF Quantum the performance has been as good if not better than Chrome, with the added benefit of Mozilla not selling all your browsing information to ad companies. I like to use their Beta builds but that might not be for everybody.

Download the Beta version of [Firefox](https://www.mozilla.org/en-US/firefox/channel/desktop/)

Preferences:

  General
  * When Firefox Starts > Show your home page
  * Tabs > Open links in tabs instead of new windows
    
  Search
  * Use the address bar for search and navigation
  * Default Search Engine > DuckDuckGo

Add ons:

  * uBlock Origin
  * simple-modify-headers
  * Vimium-ff

### iTerm2

iTerm2 is my favorite terminal emulator, second only to Cathode, which no one should _actually_ use.

Download the newest version of [iTerm](http://iterm2.com/)

Preferences:
  General
  
  * Confirm closing multiple sessions OFF
  * Confirm "Quit iTerm2 (Cmd+Q)" command OFF

  Appearance
  * Theme DARK

  Profiles
    General
    
  * Send text at start: set_http_proxy (My work environment requires setting proxy settings each new session, do not set this if you don't need to)
    Text
  * Cursor BOX
  * Blinking Cursor ON
  * Font 13pt Hack Regular ([Hack](https://github.com/source-foundry/Hack) is my favorite monospaced font. It's also open source)

Bash Profile:
  My bash profile is available in [GitHub](https://github.com/Ryan-McBride/dotfiles)

### Homebrew

[Homebrew](https://brew.sh/) is my (and most other devs I know's) favorite osx package manager. Just follow the installation instructions on the website.

Packages to install:
  git
  vim
  bash-completion
  python
  python3

### Git

You should already have Git installed from the Homebrew section. To configure your git config, enter the following terminal commands:

```
$ git config --global user.name "Your Name Here"
$ git config --global user.email "your_email@here.com"
$ git config --global credential.helper osxkeychain
```

### Vim

Vim is my text editor of choice. It's not for everyone. Install the latest version of Vim via homebrew. My .vimrc is available in [GitHub](https://github.com/Ryan-McBride/dotfiles)

[Vim-anywhere](https://github.com/cknadler/vim-anywhere) is an app that basically lets you quickly open a vim window, edit text, and paste it into any text field you're working with. Great for longform text fields.


### Python

System python is dumb so you should always install Python from Homebrew before messing with stuff. It also installs pip. You should already have Python and Pip installed from the Homebrew section.

Configuring Pip
```
$ pip install --upgrade setuptools
$ pip install --upgrade distribute
$ pip install --upgrade pip
```

Executable scripts from Python packages you install will be put in `/usr/local/share/python`, so let's add it to the `$PATH`. To do so, we'll create a `.path` text file in the home directory.

```
$ cd ~
$ subl .path

```
And add these lines to .path:

```
PATH=/usr/local/share/python:$PATH
export PATH

```
Save the file and open a new terminal to take the new `$PATH` into account (everytime you open a terminal, `.bash_profile` gets loaded).

### AWS Cli tool

The [AWS CLI](https://aws.amazon.com/cli/) tool is the best way to interact with aws programatically. For example, there is no way to clone an S3 bucket to your local machine, without this tool.

  `$ pip install awscli`

### Node

If you're going to be developing in Node, you'll want to set up NVM so you can easily switch between Node versions for different projects.

[Installation Instructions](https://github.com/creationix/nvm)

### Apps

This is just a list of apps that I generally always have installed

  * [1Password](https://1password.com/)
    Password management. I use their non-hosted solution because I don't trust storing all my passwords on a company's server
  * [Alfred 3](https://www.alfredapp.com/)
    Like Spotlight but a lot faster cleaner, and customizable.
  * [Resilio Sync](https://www.resilio.com/individuals/)
    Non-hosted dropbox.
  * [Spectacle](https://www.spectacleapp.com/)
    Window management. Basically Size-up but open source
  * [Slack](https://slack.com/)
    Chat app that your company will probably make you use. It's okay though.
