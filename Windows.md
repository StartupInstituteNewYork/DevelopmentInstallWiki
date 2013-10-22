This document explains how to get your computer ready for development at Startup Institute.  Code or commands you’re supposed to type are `highlighted`. Ex: `$ ls -la`

For students with a Windows operating system, we recommend either a) installing a Virtual Linux machine by following the [[Setting Up A Virtual Box]] instructions, or b) Dual-Booting with Windows and Linux.  Developing Rails applications on Windows machines can be a pain, so you should do either a) or b) above.  If, for some reason you can't do that, then follow the instructions below.

# Setting up Rails on Windows
**If you set up a Virtual Machine or Dual Boot, then you don't need to follow these instructions; your install is complete.**

# Ruby
##  Step 1: Download Ruby from railsinstaller.org

Click [here](http://rubyforge.org/frs/download.php/76862/railsinstaller-2.2.1.exe) to download, open the .exe, and follow those instructions.

**The Rails Installer will give you Ruby, Rails, and Git.**

### Git explained
Git is a popular version control system (VCS). Understanding version control, and using it well is a very valuable skill.  You’re Git knowledge will affect your ability to a) collaboratively create web applications, b) communicate with your team, b) track the history of your work, c) and revert mistakes.  Git is a challenging tool, but worth the battle.  We'll dive deeper into Git and GitHub throughout the program.

### GitHub explained
GitHub is an extremely popular company that makes it very easy to host Git repositories (ie, this is where you put your code so that many people can work on it together).

Almost all major open source projects are hosted on Github, which makes it an important tool for your toolbelt.  Because so many developers use Github, your public Github profile is often viewed as a professional portfolio.  It’s a good way for employers and community members to see what projects you’ve contributed to, what you’re interested in, and your skill level.  It’s often the first place employers will look when beginning the interview process, and can serve as a résumé replacement.

## Step 2: Configure GitHub 
Follow [these](https://help.github.com/articles/set-up-git#set-up-git) instructions.

## Step 3: Set up SSH access to Git
Now we’ll set up SSH keys for GitHub.  Go [here](https://help.github.com/articles/generating-ssh-keys#platform-mac) and follow those instructions.

### SSH explained
Before you can use GitHub, you must first enter in your basic credentials, and then setup a way to securely communicate with their servers.  

SSH (Secure Shell) is a network protocol for secure data communication.   You’ll hear people say “I shelled into that server.”  What they mean is, “I used the SSH protocol to securely connect with a remote computer so that I could run commands on it.”  We won’t get into SSH much during this course, but it’s good to understand the basics.

# Heroku
## Step 4: Set up a Heroku account and install the Heroku tools:
Follow the instructions here: https://devcenter.heroku.com/articles/quickstart 

### Heroku explained
Heroku is a PasS (Platform as a Service) provider, that integrates closely with Git.  You can push a (properly configured) Git repository to Heroku, and it will take care of a bunch of deployment work for you.  PasS providers like Heroku are useful tools, but have some limitations.  We'll dive more into Heroku and other options throughout the course; for now, you'll just need to have the toolbelt installed.

# Sublime
## Step 4: Download the Sublime 2 install for Windows from [here](http://www.sublimetext.com/2)

### Sublime explained
Sublime is the recommended text editor.  You don’t have to use Sublime. If you have another editor you like, you can stick with that.  Sublime provides a lot of cool community plugins that can make you more efficient as a coder.