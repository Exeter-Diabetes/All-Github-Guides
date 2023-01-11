# This guide explains how to set up and use a new repository
Collaborator-focused

## Prerequisites
* [Nomenclature](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/Nomenclature.md) naming convention 
* [Git](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/GithubConfig.md) installed and configured
* Must be a member of the Exeter-Diabetes Github Organisation before you can add files, repositories or make changes!
  - If you are not a member yet, ask the current organisation owner to send you an invitation which you will need to accept.





## Pushing a local project to a new github repository
### When would I use this?
- This section is most applicable when you have already started or created a coding project (folder) on your local device
- If you have a local project and you want to MIGRATE this to the online Exeter-Diabetes Organisation GitHub
- To upload your project, Github requires a container to hold your files: referred to as a "Repository"
- "Repository" is usually used synonymously with "project" as it holds all of your _project files_

### Create the new repository on Github
1. Head to the [organization](https://github.com/Exeter-Diabetes) on github
2. Navigate to the ["Repositories" tab](https://github.com/orgs/Exeter-Diabetes/repositories)
3. Create a "New Repository", and following the [naming convention](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/Nomenclature.md)
4. Choose whether the repository is best kept Private (within the organization, NOT individual) or Public (viewable by anyone on the internet)
   - Note: Public repositories although viewable by anyone, they can only be edited/modified by Exeter-Diabetes Organisation members.
5. Finalise details and click "Create Repository"
6. The Github Repository (Often shortened to "Repo") has been created!
7. Under "Quick Setup" you should be able to see an HTTPS button greyed out, with a URl to the right side
   - Something like:  | HTTPS | SSH |   | www.github.com/Exeter-Diabetes/repository.git |
8. Copy the HTTPS link (URL) that points to YOUR repository

### Initialize local environment (MacOS)
1. As **Mac** and Windows have different file explorers and terminals, these two require two different set ups.
2. On Finder, find your project folder, which contains all of your project files
3. Right click on the project folder and open a "New terminal at Folder"
4. Initialize the Git environment within the folder by entering the following command into Terminal:
```
git init
```
5. This folder now has Local Version Control enabled thanks to Git! Let's link it up to our online repository so we can start pushing and pulling our latest project versions.
6. Enter the following sequence of commands to connect your Local environment to the online Github repo
```
git add -A
git commit -m ‘initial commit’
git remote add origin [Repository HTTPS URL from step 4]
```
* "git add -A" tells Git to check ALL files within your folder for changes. If any changes are found from the previous commit, Git will _recognise_ and _save_ these files and their changes.
* "git commit" tells Git to **commit** these file changes to update the local Git repository. This essentially creates a new version of your project, where these saved changes are the difference. 
* " -m 'initial commit'" -m adds a command-line argument, which allows you to post a message along with your commit. This is extremely useful in versioning so you can keep track of _what_ changes you made, and how this version is different from the last. Feel free to change "initial commit" to whatever you like! But be sure to keep the single-quotation marks around it.
* "git remote add origin" tells Git that you are adding a new final destination to PUSH your versions (commits) to. "origin" refers to a specific branch - but don't worry about this too much, you wont ever need to change or manage branches.
* You can `Command + V` to paste your URL into the terminal, thereby giving the exact address to git so that it knows where to push your versions.

###  Initialize local environment (Windows)
1. As Mac and **Windows** have different file explorers and terminals, these two require two different set ups.
2. On File Explorer, find your project folder, which contains all of your project files
3. Right click on the project folder and "Copy as path" - this will copy the folder's path into your clipboard
4. Open Command Prompt (type "cmd" into the Windows menu), and type "cd " and paste your copied file path.
   - You can right click on the command prompt or use Control + V to paste the folder path.
```
cd [folder path]
```
5. Initialize the Git environment within the folder by entering the following command into Terminal:
```
git init
```
5. This folder now has Local Version Control enabled thanks to Git! Let's link it up to our online repository so we can start pushing and pulling our latest project versions.
6. Enter the following sequence of commands to connect your Local environment to the online Github repo
```
git add -A
git commit -m ‘initial commit’
git remote add origin [Repository HTTPS URL from step 4]
```
* "git add -A" tells Git to check ALL files within your folder for changes. If any changes are found from the previous commit, Git will _recognise_ and _save_ these files and their changes.
* "git commit" tells Git to **commit** these file changes to update the local Git repository. This essentially creates a new version of your project, where these saved changes are the difference. 
* " -m 'initial commit'" -m adds a command-line argument, which allows you to post a message along with your commit. This is extremely useful in versioning so you can keep track of _what_ changes you made, and how this version is different from the last. Feel free to change "initial commit" to whatever you like! But be sure to keep the single-quotation marks around it.
* "git remote add origin" tells Git that you are adding a new final destination to PUSH your versions (commits) to. "origin" is involved with branches - but don't worry about this, you wont ever need to change or manage branches.
* You can `Command + V` to paste your URL into the terminal, thereby giving the exact address to git so that it knows where to push your versions.

### Finishing up
* Congratulations! You have just connected your local project folder to an online repository! No easy task.
* Although we have _connected_ the two, we still actually haven't **pushed** our local project to the online repository
1. In your command prompt or terminal, enter the following command
```
git push origin main
```
* this instructs git to **push** all of the new local versions to the online repository.

If you navigate to your repository on GitHub, you should now see your project is online!

**_Now that setup is complete, please see the ["WorkingGitHub" guide!!](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/WorkingGit.md)_**





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
