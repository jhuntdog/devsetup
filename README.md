devsetup
========

Basic repo for notes about setting up a new pc for app development


## <a id="top"></a>Description

	Setup new Windows 8 PC for work, play, development


## Getting Started

Here is a *short* list of where I'd start. The list is not exhaustive or authoritative. It reflects my personal preference and a small of amount of knowledge gained through experience.

Start by installing the 


### Basic Apps

- [ ] Browsers - Chrome, Firefox (optionally, set up sync)
- [ ] [7zip](http://www.7-zip.org/)



## Dev Env Setup

### Text Editor

My two favorites:

- [ ] [Notepad++](http://notepad-plus-plus.org/)
- [ ] [Sublime Text 3](http://www.sublimetext.com/3)


### IDE

This comes down to personal preference. Right now, I'm mostly using PhpStorm and Visual Studio 2013.

You may be able to get Visual Studio Professional for free because you're a student at dreamspark.com.


### Build Tools

- [ ] [Visual Studio Express](http://www.visualstudio.com/downloads/download-visual-studio-vs)

Optional

- [ ] [MinGW](http://www.mingw.org/) and add to path -> `C:\tools\MinGW\bin` or whatever
- [ ] [Python](http://www.python.org/getit/windows/)


### Node

- [ ] [Node](http://nodejs.org/)

_Install it!_



#### GIT


> Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

from

Install Apps [github](http://github.com) and [msysGit & Git](http://msysgit.github.com/)

Add Git to path, for example `C:\Progra~2\Git\bin`

Configure Git - see [github:help](https://help.github.com/articles/set-up-git#platform-linux) for details

	git config --global user.name "Your Name Here" // default name for commits
	git config --global user.email "your_email@example.com" // default email for commits

Password caching with https

install [git credential winstore helper](http://blob.andrewnurse.net/gitcredentialwinstore/git-credential-winstore.exe)

	git config --global credential.helper 'cache --timeout=3600'
	# credential helper cache, timeout 1 hour


Configure SSH

	cd ~/.ssh // backup ssh keys if applicable
	ssh-keygen -t rsa -C "your_email@example.com" // create ssh key
	// add id_rsa.pub to github if you want
	// test it out
	ssh -T git@github.com

You'll need ssh at some point, so go ahead and set it up.


### Powershell

Set up powershell to assist with git usage

	// set execution policy to allow scripts, run as admin
	Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Confirm
	// initialize powershell profile
	New-item –type file –force $profile

Install [[posh-git](https://github.com/dahlbyk/posh-git)
