## Step 1: Download VirtualBox at [this link](http://download.virtualbox.org/virtualbox/4.3.0/VirtualBox-4.3.0-89960-Win.exe)

### Virtual Box explained
Virtual Machines (VM) are basically an operating system within an operating system.  It allows you to "host" another type of OS (Ubuntu in this case), while still maintaining your current OS.  For more on the details of a VM, check out [this article](https://en.wikipedia.org/wiki/Virtual_machine) (Not required reading to finish installing with this walkthrough).

## Step 2:  Follow these instructions to create a Virtual Ubuntu Machine
1. Open Oracle VirtualBox and click on "New" then "Next".
2. You must type in a name like "Ubuntu Virtual Machine" in the "Name" field.
3. For "Operating System" Linux must be selected and for "Version" is Ubuntu -- for 64-bit Ubuntu the version is "Ubuntu (64 bit)". Once you are done click "Next".
4. Use the slider to allocate RAM memory -- 512MB is recommended according to Ubuntu, but 1GB will provide better performance -- then click "Next".
5. Click "Next", "Next" and "Next" to use the recommended VirtualBox settings.
6. Use the slider to set the virtual disk image size for Ubuntu -- it should be at least 5GB per Ubuntu recommendations, but allocate at least double to avoid running out of free space.
7. From "Location" place the virtual disk image on a drive/partition that has more free space than allocated at step no. 5, then click "Next".
8. Click "Create" then "Create" again.
9. To power on the Ubuntu virtual machine just click "Start".
10. Validate the prompt (OK) then click "Next".
11. Use the button on the right of "Media Source" to select the Ubuntu ISO file, click "Open" then "Next".
12. Click "Start" to trigger the Ubuntu install process and validate any prompt.
13. Select the language then click on "Install Ubuntu".
14. Check "Download updates while installing" and "Install this third-party software" to get MP3 decoding, then click "Continue".
15. Since the installation is done on a virtual machine you can leave the default option "Erase disk and install Ubuntu" then click "Continue" and "Install now".
16. Select your location and click "Continue".
17. Select your keyboard layout -- if you are unsure you can use the default options and click "Continue".
18. Type in the "Name" and "Your computer's name" at which point Ubuntu will automatically select a username -- you can leave it as is or change it -- then type in your password and confirm it.
19. Select "Log in automatically" if you do not want to enter a password each time you log in, instead of "Require my password to log in" that is the default option.
20. Click "Continue" then "Restart now" and press Enter if you are requested to at the end of the install process.

# Version Control with Git and Github:
## Step 3: Create a GitHub account
If you haven't already, go to www.github.com and make an account. Keep your username and email professional; if you have a handle that you use other places, use it here too.  If you don’t, it’s a good idea to use some combination of your first name and last name.

## Step 4: Install Git on your computer
Use `apt-get` to install git
`$ sudo apt-get install git`

In this one line, you will automatically download the program (Git) from Ubuntu's repositories, compile it, and install it.

### apt-get explained
`apt-get` is a "package manager" that manages repositories of software, and makes getting that software trivial.  You'll use it for getting a number of tools throughout the course.  For more details on `apt-get`, see the [Ubuntu page on Apt](https://help.ubuntu.com/community/AptGet/Howto).

### Git explained
Git is a popular version control system (VCS). Understanding version control, and using it well is a very valuable skill.  You’re Git knowledge will affect your ability to a) collaboratively create web applications, b) communicate with your team, b) track the history of your work, c) and revert mistakes.  Git is a challenging tool, but worth the battle.  We'll dive deeper into Git and GitHub throughout the program.

### GitHub explained
GitHub is an extremely popular company that makes it very easy to host Git repositories (ie, this is where you put your code so that many people can work on it together).

Many major open source projects are hosted on Github, which makes it an important tool for your toolbelt.  Because so many developers use Github, your public Github profile is often viewed as a professional portfolio.  It’s a good way for employers and community members to see what projects you’ve contributed to, what you’re interested in, and your skill level.  It’s often the first place employers will look when beginning the interview process, and can serve as a résumé replacement.

## Step 5: Configure GitHub 
Follow [these](https://help.github.com/articles/set-up-git#set-up-git) instructions.

## Step 6: Set up SSH access to Git
Now we’ll set up SSH keys for GitHub.  Go [here](https://help.github.com/articles/generating-ssh-keys#platform-mac) and follow those instructions.

### SSH explained
Before you can use GitHub, you must first enter in your basic credentials, and then setup a way to securely communicate with their servers.  

SSH (Secure Shell) is a network protocol for secure data communication.   You’ll hear people say “I shelled into that server.”  What they mean is, “I used the SSH protocol to securely connect with a remote computer so that I could run commands on it.”  We won’t get into SSH much during this course, but it’s good to understand the basics.

# Heroku
## Step 7: Set up a Heroku account and install the Heroku tools:
Follow the instructions here: https://devcenter.heroku.com/articles/quickstart 

### Heroku explained
Heroku is a PasS (Platform as a Service) provider, that integrates closely with Git.  You can push a (properly configured) Git repository to Heroku, and it will take care of a bunch of deployment work for you.  PasS providers like Heroku are useful tools, but have some limitations.  We'll dive more into Heroku and other options throughout the course; for now, you'll just need to have the toolbelt installed.

# Sublime
## Step 8: Download the Sublime 2 install for Mac from [here](http://www.sublimetext.com/2)

### Sublime explained
Sublime is the recommended text editor.  You don’t have to use Sublime. If you have another editor you like, you can stick with that.  Sublime provides a lot of cool community plugins that can make you more efficient as a coder.

## Step 9: Add Sublime’s command line tools (copy-paste this)
`$ ln -s /Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl`
This allows you to run sublime from the command line by running `$ subl<ENTER>`.

# RVM
## Step 10: Install RVM

From the [RVM install page](https://rvm.io/rvm/install/), we get this command: 
`$ \curl -L https://get.rvm.io | bash`

Check that it worked:  
`which ruby`

That should show you something with `/.rvm` in the path, like this:  
`/Users/chaz/.rvm/rubies/ruby-1.9.3-p143/bin/ruby`

If you see that, then run this:  
`rvm rubygems latest`

If you don't see `/.rvm` when you run `which ruby`, try this:
`$ echo '[[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm"' >> ~/.bashrc`  
`$ source ~/.bashrc`

If you see ruby-1.9.3 when you run `which ruby`, then you're good to go.  If not, then run these commands.
`$ rvm install 1.9.3`

`$ rvm use 1.9.3`

`$ rvm --default 1.9.3`

`$ rvm rubygems latest`