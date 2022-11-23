# This file explains how to properly set up Git on your device

## What is Git?
* Git is the version control software you use to push/pull/rollback and merge (and many more)
* GitHub is the cloud hosting that provides you free storage to upload and maintain your code
* If you have used software like GitHub desktop, or have pushed local file changes from an Integrated Developemt Environment to modify cloud-stored documents,
the underlying software to communicate these changes and updates is Git!
* Git is best enjoyed on terminal/command line

## Before you install Git
* It is recommended you check that you dont already have it installed
* In terminal (MacOS) or command prompt (Windows) enter the following command
```
$ git --version
```
* If this returns the following: You already have Git installed!
```
> git version 2.32.1 (Apple Git-133)
```

## Installing Git - Windows
* Installing Git on Windows is extremely simple!
* Head to the [official download page](https://git-scm.com/download/win)
* Download the latest stable version! Be sure to check your system for compatiability (x64 or x84)

## Installing Git - MacOS
* Navigate to [Git's official page](https://git-scm.com/)
* Download Git in the bottom right corner
* There are other ways such as Homebrew and Xcode to install via command line if necessary:
* Using terminal, install [HomeBrew](https://brew.sh/), wait for it to finish, and then use Homebrew to install Git
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
. . . wait for completion . . .
$ brew install git
```

## Setting up GitHub Credentials
* In order to push/pull to GitHub from your device using Git, you require credentials

1. enter the following into terminal or command prompt:
```
$ git config --global user.name "[username]"
$ git config --global user.email "[email]"
```
* \[username] = your GitHub username
* \[email] = your GitHub email

2. To check these details enter the following into terminal or command prompt:
```
$ git config -get [user.name]
$ git config -get [user.email]
```

3. The next time you attempt to pull/push from Github when credentials are required, it will launch a browser-authentication for your Github account!
