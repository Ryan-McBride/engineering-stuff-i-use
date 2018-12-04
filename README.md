# Software Engineering Tools I use

This repo are my personal setup steps for getting a new machine ready for coding, blogs I read, podcasts I listen to, and other things relating to my career. The tools are node-leaning beacuse javascript is typically what I use the most.

* [OSX Setup](#osx-setup)
* [iOS Setup](#ios-setup)
* [Home Network](#home-network)
* [Recommended Reading](#recommended-reading)
* [Programming Podcasts](#programming-podcasts)
* [Music For Getting Stuff Done](#music-for-getting-stuff-done)


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
  * Privacy Badger
  * Dark Reader

### iTerm2

iTerm2 is my favorite terminal emulator, second only to Cathode, which no one should _actually_ use.

Download the newest version of [iTerm](http://iterm2.com/)

Preferences:
  General
  
  * Confirm closing multiple sessions OFF
  * Confirm "Quit iTerm2 (Cmd+Q)" command OFF

  Appearance
  * Theme [dracula](https://draculatheme.com/iterm/)

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

If you use my dotfiles, it will throw a bunch of errors unless you have [Vundle](https://github.com/VundleVim/Vundle.vim) installed. Run :PluginInstall on first run.

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

### VPN

I generally don't feel safe connecting to public wifi unless I'm also using a VPN. This basically encrypts your traffic to another location, so that the local network, and the network's ISP can't see your personal information. This doesn't provide absolute protection, but can give you some added security when using public networks. It also gives you the benefit of giving yourself a US IP address when you're travelling internationally, so that you can use US Netflix, Hulu, etc.  The service I use for this is [trust.zone](https://trust.zone). It's relatively cheap and has great speeds.

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
  * [Marta](https://marta.yanex.org/)
    Like finder but good
  * [Postman](https://www.getpostman.com/)
    Making API requests and mock servers

## iOS Setup

What phone you want to use is incredibly personal to you. I happen to like using iPhones. I used to use Android because they were more customizable, cheaper, and generally more open, but I switched to iPhone when ease of use, started to outweigh need for weird customization options for me. I was also tired of how Android phones would all come with their own weird flavor of Android, that wouldn't get updates until sometimes months after they came out on Android core. I guess that's not a problem with the Pixel phones but I'm not sold. I currently use an iPhone 8 plus.

### System Update

Just like your computer, you should always keep your phone up to date. There are the occasional regression bugs but in general updates keep your phone secure.

**Settings > General > Software Update**

### System Preferences

These are going to be highly dependant on you, but for security tips I recommend reading [this blog post](https://spreadprivacy.com/iphone-privacy-tips/) by DuckDuckGo.

### Apps

I don't really want to just list all the apps I use because that changes a lot and most of them are pretty common, but I will say that I always use Lyft over Uber. Uber has proven that they are a toxic brogrammer culture that I don't want to contribute to.

## Home Network

Again, this is going to be very custom to your tastes, but there are some things that I can't live without.

### Fastest Internet available in your area

Internet speeds are not something you want to cheap out on. I'm lucky enough to get Gigabit speeds and I highly recommend it.

### Stand Alone Wireless Router

Combo modem/routers are sometimes 'good enough' but they always perform poorly compared to stand alone routers. I like the Airport Extreme. Whatever router you get be sure to change the admin username and password, and set a long but easy to remember password.

Don't open any ports unless you need to, but you probably won't need to. If you're running something that requires you to open ports for incoming connections, you should probably just use AWS instead.

### LAN

LAN is always faster than wifi. Always use lan if possible, especially if your work is sensitive to lag. It's a pain to pull cable all over a house, but you'll be happy once you have. There's plenty of information on getting started on the [home networking subreddit](https://www.reddit.com/r/HomeNetworking/).

### Home Server

I run a home server for things like Plex and Resilio Sync. I like using a Mac Mini for this because I can just plug it in and forget about it. You could also use something like a raspberry pi but I've found them underpowered for almost anything I've ever used them for.

## Recommended Reading

Reference material is a collection of resources that you aren't likely to read front to back, but reference as needed

Reading material is stuff you read. You know. Like books and stuff.

### Reference Material
  * [30 Seconds of CSS](https://atomiks.github.io/30-seconds-of-css/)
  * [Practical Vim](https://www.amazon.com/Practical-Vim-Edit-Speed-Thought/dp/1680501275/ref=sr_1_1?s=books&ie=UTF8&qid=1519755674&sr=1-1&keywords=practical+vim)
  * [Modern Vim](https://www.amazon.com/Modern-Vim-Development-Environment-Neovim/dp/168050262X/ref=sr_1_4?s=books&ie=UTF8&qid=1519755534&sr=1-4&keywords=practical+vim) (Not Yet Available)
  * [Mostly Adequate Guide to Functional Javascript](https://github.com/funpress/mostly-adequate-guide-to-fp)

### Reading Material
  * [Brotopia](https://www.amazon.com/Brotopia-Breaking-Boys-Silicon-Valley/dp/0735213534/ref=sr_1_1?ie=UTF8&qid=1519755440&sr=8-1&keywords=brotopia)
  * [The Code Book](https://www.amazon.com/Code-Book-Science-Secrecy-Cryptography/dp/0385495323/ref=sr_1_1?s=books&ie=UTF8&qid=1519755469&sr=1-1&keywords=the+book+of+code&dpID=51S0aQLkDCL&preST=_SY291_BO1,204,203,200_QL40_&dpSrc=srch)
  * [fivebooks.com's Best 5 Books for Programming + Compsci](https://fivebooks.com/best-books/programming-computer-science-ana-bell/)
  
## Programming Podcasts
  * Command Line Heroes
  * Software Engineering Daily
  
## Music for Getting Stuff Done
I can't listen to podcasts while coding because it's too distracting. I lean towards music without lyrics, but there are exceptions.

  * [musicforprogramming.net](http://www.musicforprogramming.net/)
  * [YouTube Vaporwave](https://www.youtube.com/results?search_query=vaporwave)
  * [My Work Spotify Playlist](https://open.spotify.com/user/nullofundefined/playlist/2d3seTxgFiIbYnPMXQZBSY?si=-dMwDMaQRG63GQ5lWL4KlQ)
