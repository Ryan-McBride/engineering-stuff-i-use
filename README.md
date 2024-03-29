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

You should always keep any system you're using up to date. Yes, sometimes there are regression bugs (thanks apple) but in general it's the best way to protect yourself from malware.

To update OSX:

*Apple Icon > Software Update...*

### System preferences.

Basic system preferences that I always always change.

Security & Privacy
  FileVault
  * Turn on Filevault
  * Use a key instead of an iCloud account to unlock
  * Store key in password manager
  
  Firewall
  * Turn on Firewall

Trackpad
  Point & Click
  * Look up & data detetors: ON | Force Click with one finger
  * Secondary click: ON | Click with two fingers
  * Tap to click: OFF
  * Click: MEDIUM
  * Tracking speed: FAST
  * Force Click and haptic feeback: ON

  Scroll & Zoom
  * Scroll direction natural: OFF
  * Zoom in or out: ON
  * Smart zoom: ON
  * Rotate: ON

  More Gestures
  * Swipe between pages: OFF // causes me to sometimes go back in browser by accident which is really annoying
  * Swipe between full-screen apps: ON | Swipe left or right with three fingers
  * Notification Center: ON | Swipe left from the right edge with two fingers
  * Mission Control: ON | Swipe up with three fingers
  * App Exposé: OFF
  * Launchpad: OFF
  * Show Desktop: ON | Spread with thumb and three fingers

Keyboard
  * Key Repeat FASTEST
  * Delay Until Repeat SHORT

Dock
  (I almost never use the dock so I make it as out of the way as possible)
  * Size SMALL
  * Magnification OFF
  * Automatically hide and show the Dock ON 

### Firefox

I prefer firefox, I don't really like using google things unless I have to. Never mind the fact that I still use google sheets 100 times a day 💀

Download [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/)

Settings:

  General
  * Tabs > Open links in tabs instead of new windows
    
  Search
  * Use the address bar for search and navigation
  * Default Search Engine > DuckDuckGo

Add ons:

  * [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin) | Blocks ads
  * [Privacy Badger](https://addons.mozilla.org/en-US/firefox/addon/privacy-badger17/)
  * [HTTPS Everywhere](https://addons.mozilla.org/en-US/firefox/addon/https-everywhere/)
  * [Vimium-ff](https://addons.mozilla.org/en-US/firefox/addon/vimium-ff/) | vim keybindings in the browser

Theme:

  * [Dracula Dark Theme by RaphGL](https://addons.mozilla.org/en-US/firefox/addon/dracula-dark-colorscheme/)

### iTerm2

Download the newest version of [iTerm](http://iterm2.com/)

Preferences:
  General
  
  * Confirm closing multiple sessions OFF
  * Confirm "Quit iTerm2 (Cmd+Q)" command ON

  Appearance
  * Theme [dracula](https://draculatheme.com/iterm/)

  Profiles
    Text
      * Cursor BOX
      * Blinking Cursor ON
      * Font 13pt Hack Regular ([Hack](https://github.com/source-foundry/Hack) is my favorite monospaced font. It's also open source)

Oh My ZSH:
  OSX comes with ZSH now, so install [this](https://ohmyz.sh/) for ease of prettification

Bash Profile:
  My bash profile is available in [GitHub](https://github.com/Ryan-McBride/dotfiles)

### Homebrew

[Homebrew](https://brew.sh/) is my (and most other devs I know's) favorite osx package manager. Just follow the installation instructions on the website.

Packages to install:
  neovim
  bash-completion
  pyenv
  wget

### Git

You should already have Git installed from the Homebrew section. To configure your git config, enter the following terminal commands:

```
$ git config --global user.name "Your Name Here"
$ git config --global user.email "your_email@here.com"
$ git config --global credential.helper osxkeychain
```

### NeoVim

NeoVim is my text editor of choice. Specifically I use a bundle called [nvChad](https://nvchad.com/). My config files are available in [GitHub](https://github.com/Ryan-McBride/dotfiles)

### AWS Cli tool

The [AWS CLI](https://aws.amazon.com/cli/) tool is the best way to interact with aws programatically. For example, there is no way to clone an S3 bucket to your local machine, without this tool.

  `$ pip install awscli`

### Node

If you're going to be developing in Node, you'll want to set up NVM so you can easily switch between Node versions for different projects.

[Installation Instructions](https://github.com/creationix/nvm)

### Apps

This is just a list of apps that I generally always have installed

  * [Bitwarden](https://bitwarden.com)
    Open source password manager that has better free tier options than 1Password. Highly Highly recommend hosting your own instance rather than storing your data on bitwarden servers. Setup is very easy.
  * [Alfred](https://www.alfredapp.com/)
    Like Spotlight but a lot faster cleaner, and customizable.
  * [Resilio Sync](https://www.resilio.com/individuals/)
    Non-hosted dropbox.
  * [Rectangle](https://rectangleapp.com/)
    Window management. A fork of Spectacle which is deprecated.
  * [Karabiner-Elements](https://github.com/tekezo/Karabiner-Elements)
    I basically just use this to turn off my laptop keyboard when I plug in my usb keyboard. I use a mechanical keyboard because I'm a loser.
  * [Marta](https://marta.yanex.org/)
    Like finder but good
  * [Postman](https://www.getpostman.com/)
    Making API requests and mock servers
  * [Burp Suite](https://portswigger.net/burp/communitydownload)
    A useful tool for intercepting and changing browser requests. It does other stuff too but that's what I use it for the most. Invaluable for testing

## iOS Setup

What phone you want to use is incredibly personal to you. I happen to like using iPhones. I used to use Android because they were more customizable, cheaper, and generally more open, but I switched to iPhone when ease of use, started to outweigh need for weird customization options for me. I was also tired of how Android phones would all come with their own weird flavor of Android, that wouldn't get updates until sometimes months after they came out on Android core. I guess that's not a problem with the Pixel phones but I'm not sold. I currently use an iPhone Xs Max.

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
  * [Modern Vim](https://www.amazon.com/Modern-Vim-Development-Environment-Neovim/dp/168050262X/ref=sr_1_4?s=books&ie=UTF8&qid=1519755534&sr=1-4&keywords=practical+vim)
  * [Mostly Adequate Guide to Functional Javascript](https://github.com/funpress/mostly-adequate-guide-to-fp)
  * [The Art of the Command Line](https://github.com/jlevy/the-art-of-command-line)

### Reading Material
  * [The Code Book](https://www.amazon.com/Code-Book-Science-Secrecy-Cryptography/dp/0385495323/ref=sr_1_1?s=books&ie=UTF8&qid=1519755469&sr=1-1&keywords=the+book+of+code&dpID=51S0aQLkDCL&preST=_SY291_BO1,204,203,200_QL40_&dpSrc=srch)
  * [Brotopia](https://www.amazon.com/Brotopia-Breaking-Boys-Silicon-Valley/dp/0735213534/ref=sr_1_1?ie=UTF8&qid=1519755440&sr=8-1&keywords=brotopia)
  * [fivebooks.com's Best 5 Books for Programming + Compsci](https://fivebooks.com/best-books/programming-computer-science-ana-bell/)
  
## Programming Podcasts
  * Command Line Heroes
  * Software Engineering Daily
  
## Music for Getting Stuff Done
I can't listen to podcasts while coding because it's too distracting. I lean towards music without lyrics, but there are exceptions.

  * [musicforprogramming.net](http://www.musicforprogramming.net/)
  * [YouTube Vaporwave](https://www.youtube.com/results?search_query=vaporwave)
  
