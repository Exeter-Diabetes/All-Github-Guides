# This guide explains how to best use Git on a daily basis

## Prerequisites
* [Git](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/GithubConfig.md) installed and configured
* [Have set up a Github repo](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/Repositories.md)

## Pulling
* Once a local environment has been connected to an online repository, there can be _version conflicts_:
  - Imagine you and a co-worker are working on the same file, and they begin work before you do and *push* a new change to the online repository.
  - By the time you *push* your code from your local environment to the online repository, there can be issues! Perhaps they deleted some of the code you required.
* **Pulling** is the idea of requesting the most recent version from a Github repository. You will then be required to *merge* incoming changes. This process is not done automatically as Git does not want to damage or break your code!
* When working collaboratively on files: *It is best practice to **pull** the latest version before you **push**, to avoid version conflicts*
  - When working on your own projects, if you are the **only one** committing changes, you won't need to pull frequently as your changes are the only.
* To Pull, open terminal or command prompt to your local project
  - Terminal: Right click folder and "New Terminal at Folder"
  - Command Prompt: open command prompt and "cd C://folder/path"
* Enter the following command:
```git pull```

## Pushing
* Everytime you commit changes to your local environment, it is good practice to *Push* these changes as well.
* Beware! Saving files is **NOT** the same as committing, which is also ***NOT*** the same as pushing.
  - Saving files refers to saving the changes to your device, modifying the actual *file*
  - Commiting files refers to updating your *local version*, it **does not change your files**
  - Pushing files refers to **uploading** your local version to the online repository. ***It does not change your local files, nor version.***
* Commit messages should ideally be succinct, summarising all of your latest and most important changes
  - Commit messages are designed for _other people_ to be able to keep track of your changes as well, not always are they just for you.
* To Push, open terminal or command prompt to your local project
  - Terminal: Right click folder and "New Terminal at Folder"
  - Command Prompt: open command prompt and "cd C://folder/path"
* Enter the following command:
```git push origin main```
