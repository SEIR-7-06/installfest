#Installfest Step 1: General Mac Development Tools


**Plan overview:**

1. Upgrade operating system to Maverick or Yosemite.   
1. Install Xcode and Command Line Tools - the most basic built-in coding tools for Mac.  
2. Install Homebrew - a package manager for Mac.  (Package managers are programs that help you install external tools and keep them up to date.)
3. Configure git - a version control system. (Version control systems are programs that help you keep track of changes in your code.)
4. Install and configure Sublime Text - a text editor specialized for writing code.
5. Install the Chrome web browser.

If you do not yet have an account for the Mac App Store, follow the instructions on Apple Support to <a href="https://support.apple.com/kb/PH11499?locale=en_US" target="_blank">create a Mac App Store account</a>.

## Operating System and Command Line Tools

Before class starts, we suggest you upgrade your operating system to OS X Maverick or Yosemite. We do not recommend that you use El Capitan *yet* because some of the tools we use have not been updated for El Capitan.  **Do not upgrade your operating system during WDI.** 

To check what version of OS X you are running:  
1. Click the apple icon in the top left of your screen.  
2. Select "About This Mac" from the dropdown menu.   
3. Read the version information from the window that pops up.   

If you are not using Maverick or Yosemite, detailed instructions for upgrading your operating system are available through Apple support: <a href="https://www.apple.com/support/osx/upgrade/" target="_blank">How to upgrade to OS X Yosemite</a>.

### Install Command Line Tools from the Terminal

1. Open the Terminal application.
2. In your Terminal, type `xcode-select --install`, and a new window and installer will appear. 
3. Follow the instructions in the installer. 


### Install Command Line Tools through Xcode (Older Versions of OS X)

If you must run a version of OS X before Maverick, you will need to install command line tools that come from Xcode. Only follow these steps if you were not able to install Xcode command line tools with the instructions above.

1. Open the Mac App Store and install Xcode.
1. Open Xcode.
1. Inside the Xcode menu, choose Preferences > Downloads > Install The Command Line Tools.
1. Follow the instructions in the installer.

## Homebrew

<a href="http://brew.sh/" target="_blank">Homebrew</a> is a *package manager* for OS X.  We'll use to quickly download and install other tools we use, or to update already installed tools. 

1. Open up the application Terminal and run `which brew` to check if you have homebrew installed already. If it is installed, the Terminal will output a file path. If it is not installed, the Terminal won't output anything. 

1. **Only if you do not have homebrew installed**, run the command below to install homebrew. Wait while homebrew is downloaded and installed.

	```bash
	ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	```

	If you run into problems, you may need to run  `rm -rf /usr/local/Cellar /usr/local/.git` and then retry the command above.
	
		
1. Run `brew update` to update homebrew.


1. Run `brew doctor` in your Terminal to check that homebrew and any current packages are installed correctly. If there are issues, `brew doctor` will list suggestions for how to fix them.  Follow these suggestions one by one. If you are unsure what to do, ask!

1. You may need to edit your ~/.bashrc to have include the path to homebrew, if `brew doctor` shows warnings.

	```
	bash echo 'export PATH="/usr/local/bin:/usr/local/sbin:~/bin:$PATH"' >> ~/.bash_profile
	```

1. Let's install our first simple package with homebrew: `tree`!  This package adds a command to your Terminal that displays files in a tree view (instead of a list view like `ls`).  Enter the following command in your Terminal:

	```
	brew install tree
	```

1. Run the Terminal command `tree` to see a tree view of all the files inside your current directory!



## Git

You should already have git installed and have an account on GitHub from Fundamentals. If not, sign up for an account on <a href="http://www.github.com" target="_blank">http://www.github.com</a>. We will be using github.com to track code and for collaboration. 

### Confirm Install

1. To check whether git is installed on your system, run the Terminal command `which git`. The `which` Terminal command shows where on your computer a Terminal command is installed. The output should be a directory path like `/usr/bin/git`; this is where git is installed on your machine.  If you don't see any output at all, git is not installed on your computer. 


1. If you do not have git installed, run the following command in your Terminal:

	```bash
	brew install git
	```

### Configure Git

Configuring your git settings to help GitHub track your contributions and to make it easier and smoother to commit. 

1. Use the following three `git config` commands to configure your git user information and have git "cache" (remember) it for a few minutes. We use the `--global` (or `-g`) option to make the configuration apply to all repos.
  
	```
	git config --global user.name "YOUR-USERNAME"
	git config --global user.email YOUR-EMAIL-ADDRESS
	git config --global credential.helper cache
	```

1. Generate a SSH key for GitHub. This will allow you to use GitHub from your Terminal without entering your login information every time you push.

     [Generating SSH Keys (via GitHub.com)](https://help.github.com/articles/generating-ssh-keys)

## Sublime Text

1. Use the following link to <a href="http://c758482.r82.cf2.rackcdn.com/Sublime%20Text%20Build%203083.dmg">download Sublime Text 3</a>. 

1. Open the downloaded file.

1. Follow the installation instructions (drag Sublime Text 3 to your Applications folder).

1. Open the Sublime Text 3 application. 

### Add Package Control

Sublime Text has its own very popular package manager called Package Control. We'll use it to add extra features to Sublime Text, including a web development shortcut package called Emmet and a JavaScript syntax helper jshint.

1. Follow <a href="https://packagecontrol.io/installation" target="_blank">Package Control's  "simple installation" instructions</a> to add Package manager to your Sublime Text. When you paste the large block of text, make sure you:
   -  use the Sublime Text 3 version, and   
   -  enter the text into the bottom rectangle of the Sublime Text console.

1. We access Package Control through the Sublime Text command palette. Open the palette by pressing `cmd+shift+p` from within Sublime Text. Type `Package Control`  in the command palette to see the list of things Package Control can do.


### Add Packages

1. Let's install our first package, Emmet.  Select `Package Control: Install Package` to bring up the list of available packages. 

1. Select `Emmet` from the list, and Package Control will install it for you!  (Start typing "Emmet" in the search bar to narrow down the list.)  

<!--@TODO: PyV8 binaries error message - see https://github.com/sergeche/emmet-sublime/issues/476 ?-->

The other package we plan to add, jshint, requires Node.js.  We'll get to it in the next set of instructions, <a href="https://github.com/sf-wdi-22-23/installfest/blob/master/express_stack.md" target="_blank">Express Stack</a>.

### Access Sublime from the Terminal

Sublime Text 3 includes a program that launches Sublime from the Terminal.  We'll use the `ln` command to link that program to a simple `subl` command. 

1. To run a program from the Terminal, it needs to be available on your $PATH. The next step assumes `/usr/local/bin` is in your $PATH, so let's check that.  Run the following command from the Terminal to see your current $PATH:
	
	```
	echo $PATH
	```

1. Run the following command in your Terminal to set up the link:
	```
	ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl
	```

1. Type `subl . ` in the Terminal, and Sublime Text 3 should open!

### Configure git to use Sublime

When you forget to enter a commit message in the Terminal, git opens a text editor and reminds you to add a commit message.  

1. Run the following command in the Terminal to configure git to open Sublime Text instead of the default text editor:
	
	```
	git config --global core.editor "subl"
	```

## Chrome

1. <a href="https://support.google.com/chrome/answer/95346?hl=en" target="_blank">Download and install the Chrome web browser with these instructions.</a>
