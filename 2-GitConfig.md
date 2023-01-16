# This file explains how to properly set up Git on your device

## What is Git?
* Git is the version control software used to push/pull/rollback and merge (++) code
* Git != Github
   * Github is the cloud hosting service that provides you free storage to upload, version and maintain your code
   * To upload your files to Github, you could manually click "Upload" on their web page and upload files, **or** you can use _**Git**_ to do it with ease
* Git is natively designed for Command Line (Shell) environments
* Most Integrated Development Environments (IDEs; PyCharm, R-Studio, VSCode) offer Git integration! Use Git without ever leaving your code.

## Before you install Git
It is recommended you check that you dont already have it installed:
1. In terminal (MacOS) or command prompt (Windows) enter the following command
```
$ git --version
```
2. If this command returns any "version" of git (usually formatted like 2.23.1), you already have it installed
   * If "Command was not found" this means you don't have it installed
```
> git version x.xx.x ...
```

## Installing Git - Windows
* Installing Git on Windows is extremely simple!
* Head to the [official download page](https://git-scm.com/download/win)
* Download the latest stable version! Be sure to check your system for compatiability (x64 or x84)

## Installing Git - MacOS
* Navigate to [Git's official page](https://git-scm.com/)
* Download Git in the bottom right corner

There are other ways such as Homebrew and Xcode to install via command line if necessary:
* **If you used the above steps to download and install it, you _DO NOT_ need to worry about the next step**
1. Using terminal, install [HomeBrew](https://brew.sh/), wait for it to finish, and then use Homebrew to install Git
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
. . . wait for completion . . .
$ brew install git
```

## Setting up GitHub Credentials
In order to push/pull to Github from your device using Git, you need to _Sign in_ to Github, using credentials.
Before proceeding, make sure you have a Github account! You will need your username and email.

1. Enter the following into terminal or command prompt, Where:
   * \[username] = your Github username
   * \[email] = your Github email
```
$ git config --global user.name "[username]"
$ git config --global user.email "[email]"
```

2. To check these details enter the following into terminal or command prompt:
```
$ git config -get user.name
$ git config -get user.email
```

3. The next time you attempt to pull from a private Github repository or push to any Github repository, your default browser will launch, requriing you to sign into Github to verify your credentials! (Browser-authentication)

## You now have Git working on your computer!
