# This guide explains how to set up and use a new repository
Collaborator-focused

## Prerequisits
* [Nomenclature](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/Nomenclature.md) naming convention 
* [Git](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/GithubConfig.md) installed and configured

## Pushing a local project to a new github repository
### Create the new repository
1. Head to the organization on github and view repositories
2. Create a new repository, and following naming convention
3. Choose whether the repository or best kept Private (within the organization, NOT individual) or Public
4. Create repository, and copy the HTTPS link to the repository

### Initialize local environment
1. Create a new folder on your desktop where you want the project to be located
2. MacOS - Right click on the project folder and open a "New terminal at Folder"
3. Windows - Open command prompt and navigate via "cd" to the target folder
4. Initialize the Git environment within the folder using
```
$ git init
```
5. Move local files that you want to PUSH to the empty local git-intialized folder
6. Enter the following sequence of commands to push your local files to target GitHub repository
```
$ git add -A
$ git commit -m ‘initial commit’
$ git remote add origin [Repository HTTPS link from step 4]

```

## Cloning a GitHub repository into a local environment
### Obtain the GitHub repository link
![Screenshot 2022-11-23 at 13 30 46](https://user-images.githubusercontent.com/85688580/203559099-3f0f8aff-52c6-44d7-bccf-0ca099b2e183.png)
1. Find your target Github repository
2. Click on the "Code" dropdown to reveal and copy the HTTPS link

### Clone Repo to local environment
1. Create a new folder on local device where you would like to store github repository
2. MacOS - Right click on the project folder and open a "New terminal at Folder"
3. Windows - Open command prompt and navigate via "cd" to the target folder
4. Initialize the Git environment within the folder, and then clone the repository into the folder
```
$ git init
$ git clone [Repository HTTPS link from previous part]
```
