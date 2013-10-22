This document explains how to get your computer ready for development at Startup Institute.  Code or commands you’re supposed to type are `highlighted`. Ex: `$ ls -la`

# XCode:
## Step 1: Install xCode (if it is not already installed)
Click here to download [XCode](https://developer.apple.com/xcode/)

### XCode explained
Xcode is Apple’s development environment. You need it installed before you can install anything else. It comes with tools used to compile programs from source.
These are code compilation tools that you can access from the command line. Apple currently uses a compiler called LLVM. Another (very) popular compiler is GCC. There are a few programs that may require GCC instead of LLVM. 

## Step 2: Install XCode command line tools
1. Open up XCode from your applications folder
2. Go to the toolbar: Click Preferences → Downloads → Check install command line tools

### Troubleshooting:
Issues with GCC / XCode on OS X Mountain Lion: ([link](http://robots.thoughtbot.com/post/27985816073/the-hitchhikers-guide-to-riding-a-mountain-lion))

# Homebrew:
## Step 3: Open up the terminal 
“Terminal” is a program that comes with all OS X systems. Open Spotlight (⌘+Space) then type “terminal” to find it.

## Step 4: Install Homebrew
The first thing we will use the terminal for is to install a program called Homebrew, which is a utility that makes it easy to install other programs you need. To install Homebrew, copy this line into your terminal:

```shell
$ ruby -e "$(curl -fsSkL raw.github.com/mxcl/Homebrew/go)”
```

### Homebrew explained
Homebrew is a "package manager" that manages repositories of popular software. For more on package managers and the details of Homebrew, check out [this tutorial](http://mac.tutsplus.com/tutorials/terminal/homebrew-demystified-os-xs-ultimate-package-manager/) (not required for this install.)

## Step 5: Add Homebrew to your PATH
Insert the Homebrew directory at the top of your PATH environment variable by copying the following commands into terminal:

```shell
$ echo "export PATH=/usr/local/bin:$PATH" >> ~/.bash_profile
$ source ~/.bash_profile
```

### PATH explained
When you install a program using Homebrew, it puts that program at /usr/local/bin.  The first line above `“echo "export PATH=/usr/local/bin:$PATH" >> ~/.bash_profile”` tells your computer to prepend the /usr/local/bin folder before the rest of your PATH.  This causes the program version that Homebrew installs to execute before any others (potentially with the same name), that might have been installed earlier.

The second line applies and refreshes those changes.

Your “PATH” is a list of directories on your computer.  When you execute a command, “terminal” will attempt to find the location of that command by traversing down this list from beginning to end. Thus, the order of those directories matter. For example, if you type git<ENTER> into Terminal, it will look through the list of folders until it finds that command, and then execute it.  For more details on PATH, check out [this article](http://kb.iu.edu/data/acar.html).

## Step 6: brew doctor
```shell
$ brew doctor<ENTER>
```

Follow the instructions until it says “your system raring to brew”

### brew doctor explained
Homebrew comes with a sweet utility that checks your system to make sure everything is set up properly. If you have a new system, you shouldn’t have much trouble. If you’ve been tinkering in the past, there may be a couple things that need to be updated.

Basically it ensures that /usr/local/bin is clean and under the control of Homebrew. It also makes sure you have the correct compilers, and there are no conflicting programs installed on your system. Most issues can be fixed by trying to type the commands they suggest.

# Version Control with Git and Github:
## Step 9: Create a GitHub account
If you haven't already, go to www.github.com and make an account. Keep your username and email professional; if you have a handle that you use other places, use it here too.  If you don’t, it’s a good idea to use some combination of your first name and last name.

## Step 10: Install Git on your computer
Use brew to install git
`$ brew install git`

In this one line, you will automatically download the program (Git) from Homebrew's repositories, compile it, and install it.

### Git explained
Git is a popular version control system (VCS). Understanding version control, and using it well is a very valuable skill.  You’re Git knowledge will affect your ability to a) collaboratively create web applications, b) communicate with your team, b) track the history of your work, c) and revert mistakes.  Git is a challenging tool, but worth the battle.  We'll dive deeper into Git and GitHub throughout the program.

# GitHub explained
GitHub is an extremely popular company that makes it very easy to host Git repositories (ie, this is where you put your code so that many people can work on it together).

Almost all major open source projects are hosted on Github, which makes it an important tool for your toolbelt.  Because so many developers use Github, your public Github profile is often viewed as a professional portfolio.  It’s a good way for employers and community members to see what projects you’ve contributed to, what you’re interested in, and your skill level.  It’s often the first place employers will look when beginning the interview process, and can serve as a résumé replacement.

## Step 11: Configure GitHub 
Follow [these](https://help.github.com/articles/set-up-git#set-up-git) instructions.

## Step 12: Set up SSH access to Git
Now we’ll set up SSH keys for GitHub.  Go [here](https://help.github.com/articles/generating-ssh-keys#platform-mac) and follow those instructions.

### SSH explained
Before you can use GitHub, you must first enter in your basic credentials, and then setup a way to securely communicate with their servers.  

SSH (Secure Shell) is a network protocol for secure data communication.   You’ll hear people say “I shelled into that server.”  What they mean is, “I used the SSH protocol to securely connect with a remote computer so that I could run commands on it.”  We won’t get into SSH much during this course, but it’s good to understand the basics.

# Heroku
## Step 13: Set up a Heroku account and install the Heroku tools:
Follow the instructions here: https://devcenter.heroku.com/articles/quickstart 

### Heroku explained
Heroku is a PasS (Platform as a Service) provider, that integrates closely with Git.  You can push a (properly configured) Git repository to Heroku, and it will take care of a bunch of deployment work for you.  PasS providers like Heroku are useful tools, but have some limitations.  We'll dive more into Heroku and other options throughout the course; for now, you'll just need to have the toolbelt installed.


# Sublime
## Step 14: Download the Sublime 2 install for Mac from [here](http://www.sublimetext.com/2)

### Sublime explained
Sublime is the recommended text editor.  You don’t have to use Sublime. If you have another editor you like, you can stick with that.  Sublime provides a lot of cool community plugins that can make you more efficient as a coder.

## Step 14: Add Sublime’s command line tools (copy-paste this)
`$ ln -s /Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl`
This allows you to run sublime from the command line by running subl<ENTER>.

# RVM
## Step 15: Install RVM

From the [RVM install page](https://rvm.io/rvm/install/), we get this command: 
`$ \curl -L https://get.rvm.io | bash`

Check that it worked:  
`which ruby`

That should show you something with `/.rvm` in the path, like this:  
`/Users/chaz/.rvm/rubies/ruby-1.9.3-p143/bin/ruby`

If you see that, then run this:  
`rvm rubygems latest`

If you don't see `/.rvm` when you run `which ruby`, try this:
`$ echo '[[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm"' >> ~/.bash_profile`  
`$ source ~/.bash_profile`

If you see ruby-1.9.3 when you run `which ruby`, then you're good to go.  If not, then run these commands.
`$ rvm install 1.9.3`

`$ rvm use 1.9.3`

`$ rvm --default 1.9.3`

`$ rvm rubygems latest`

# Additional Resources
"Installing Rails from the RailsApp project": http://railsapps.github.io/installing-rails.html  
"How to Install Xcode, Homebrew, Git, RVM, Ruby & Rails on Snow Leopard, Lion, and Mountain Lion": http://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/