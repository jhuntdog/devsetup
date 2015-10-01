devsetup
========

Notes about setting up a new pc


## <a id="top"></a>Description

Setup new Windows PC for work, play, development


## Getting Started

Here is a *short* list of where I'd start. The list is not exhaustive or authoritative. It reflects my personal preference and a small of amount of knowledge gained through experience.


### Basic Apps

- [ ] Browsers - Chrome, Firefox (optionally, set up sync)
- [ ] [7zip](http://www.7-zip.org/)
- [ ] [Notepad++](http://notepad-plus-plus.org/)



## Dev Env Setup

### Base

- [ ] [Visual Studio](http://www.visualstudio.com)
- [ ] [Git for Windows](https://git-scm.com/download/win)
- [ ] [Github for Windows](https://desktop.github.com/)

### IDEs

Text Editors
- [ ] [Atom](https://atom.io/)
- [ ] [Sublime Text 3](http://www.sublimetext.com/3)

JetBrains
- [ ] PhpStorm


### Python
- [ ] [Python](http://www.python.org/getit/windows/)



### Optional Build Tools

- [ ] [MinGW](http://www.mingw.org/) and add to path -> `C:\tools\MinGW\bin` or whatever



### Node

- [ ] [Node](http://nodejs.org/)

Node Packages

	```
	npm install -g bower grunt gulp typescript
	```




### GIT

Make sure git has been added to path

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

Install [posh-git](https://github.com/dahlbyk/posh-git)
