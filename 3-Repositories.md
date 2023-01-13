# This guide explains how to set up and use a new repository
Collaborator-focused

## Prerequisites
* [Nomenclature](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/1-Nomenclature.md) naming convention 
* [Git](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/2-GitConfig.md) installed and configured
* Must be a member of the Exeter-Diabetes Github Organisation before you can add files, repositories or make changes!
  - If you are not a member yet, ask the current organisation owner to send you an invitation which you will need to accept.
  - Currently: Ethan de Villiers or Katie Young

## Creating a new Exeter-Diabetes Github Repository
- Github repositories are just online folders that hold your project files
  * "Repository" is usually used synonymously with "project" as each repository should be dedicated to one project and its _project files_
  * Repositories are often referred to as a repo or repos,
- It is good practice to separate your projects into different repositories
  * Refer to _Nomenclature_
- Creating a new Github repository **instead of** creating a new project-folder on your computer is the recommended practice
  * Best practice to _keep_ your code on Github = more organised, easier to track
  * It is much simpler to start a new project on Github and then connect it to your local environment, than creating it locally and connecting it to Github later
- **Please note:** This section is not for creating personal repositories. These steps will create a new repository within the Exeter-Diabetes organisation

1. Navigate to [Github.com](https://github.com/)
2. Once signed in, at the top of the left navigation panel, click on your username to open the Dashboard Context dropdown
   * If you have been added to the Exeter-Diabetes organisation, you should see it there
   * Click on the "Exeter-Diabetes" option to navigate to the organisation's dashboard
3. On the left side, click on "View Organisation" to be taken to the [Exeter-Diabetes page](https://github.com/Exeter-Diabetes)
4. Open the "Repositories" tab at the top, and click the green "New Repository" button in the top right
   * Follow correct _Nomenclature_ naming format, and add an appropriate description for your new project.
5. Choose whether the repository is best kept Private or Public
   * Private repositories are visible ONLY by the organisation. Anyone within the organisation can view the repository but not the public.
   * Public repositories are viewable and clonable by anyone on the internet, but they can only be modified by Exeter-Diabetes organisation members.
6. Finalise details and click "Create Repository"
7. The Github Repository has been created!
8. Under "Quick Setup" you should be able to see an HTTPS button greyed out, with a URl to the right side
   - Something like:  | HTTPS | SSH |   | www.github.com/Exeter-Diabetes/repository.git |
9. Copy the HTTPS link (URL) that points to YOUR repository
10. This URL will be used to access and connect to your new repository!
    * Extremely important for connecting local development environments to this online Github repository!

## Cloning a Github repository into a local environment
* Cloning is the fastest way to create new github projects!
* Also used when you are working collaboratively on a project someone else has already begun
* Useful for downloading others' code and running it in a local environment
* Used when you want to make changes to a project

### 1. Obtain the GitHub repository link
![Screenshot 2022-11-23 at 13 30 46](https://user-images.githubusercontent.com/85688580/203559099-3f0f8aff-52c6-44d7-bccf-0ca099b2e183.png)
1. Find your target Github repository
2. Click on the "Code" dropdown to reveal and copy the HTTPS link

### 2. Clone Repo to local environment
1. Create a new folder on local device where you would like to store github repository
2. MacOS - Right click on the project folder and open a "New terminal at Folder"
3. Windows - Open command prompt and navigate via "cd" to the target folder
4. Initialize the Git environment within the folder, and then clone the repository into the folder
```
$ git init
$ git clone [Repository HTTPS link from previous part]
```

## Pushing a local project to a new github repository
- This section is most applicable when you have already started or created a coding project on your local device
- If you have a local project and you want to MIGRATE this to the online Exeter-Diabetes Organisation Github

### 1. Create a new Github repository on Exeter-Diabetes
- Use the first section to learn how to create a new repository!
- Once it has been set up and you have the HTTPS link (URL), come back here

### 2. Initialize local environment (MacOS)
1. As **Mac** and Windows have different file explorers and shell environments, these two require two different set ups.
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
* "git add -A" tells Git to "track" ALL files within your folder for changes. If any changes are found from the previous commit, Git will _recognise_ and _save_ these files and their changes.
  * Notice how this is our first commit, so there is no "previous commit"! Git will recognise this and thereby track ALL files as being newly added - creating your first version.
* "git commit" tells Git to **commit** these file changes to update the local Git repository. This essentially creates a new version of your project on your local device, where these saved changes are the difference from the old version. 
* " -m 'initial commit'" -m adds a command-line argument, which allows you to post a comment along with your commit. This is extremely useful in versioning so you can keep track of _what_ changes you made, and how this version is different from the last. Feel free to change "initial commit" to whatever you like! But be sure to keep the single-quotation marks around it.
* "git remote add origin" tells Git that you are adding a new final destination to PUSH your versions (commits) to. "origin" regards branching - but don't worry about this too much, we'll explore branches in the [next guide](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/4-GitBash.md)
* You can `Command + V` to paste your URL into the terminal, thereby giving the exact address to git so that it knows where to push your versions.

### 2. Initialize local environment (Windows)
1. As Mac and **Windows** have different file explorers and environments, these two require two different set ups.
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
* "git add -A" tells Git to "track" ALL files within your folder for changes. If any changes are found from the previous commit, Git will _recognise_ and _save_ these files and their changes.
  * Notice how this is our first commit, so there is no "previous commit"! Git will recognise this and thereby track ALL files as being newly added - creating your first version.
* "git commit" tells Git to **commit** these file changes to update the local Git repository. This essentially creates a new version of your project on your local device, where these saved changes are the difference from the old version. 
* " -m 'initial commit'" -m adds a command-line argument, which allows you to post a comment along with your commit. This is extremely useful in versioning so you can keep track of _what_ changes you made, and how this version is different from the last. Feel free to change "initial commit" to whatever you like! But be sure to keep the single-quotation marks around it.
* "git remote add origin" tells Git that you are adding a new final destination to PUSH your versions (commits) to. "origin" regards branching - but don't worry about this too much, we'll explore branches in the [next guide](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/4-GitBash.md)
* You can `Command + V` to paste your URL into the terminal, thereby giving the exact address to git so that it knows where to push your versions.

### 3. Finishing up
* Congratulations! You have just connected your local project folder to an online repository! No easy task.
* Although we have _connected_ the two, we still actually haven't **pushed** our local project to the online repository - online there is still an empty folder! We need to sync the two.
1. In the command prompt or terminal from the previous section, enter the following command
```
git push origin main
```
* This instructs git to **push** all of the new local versions to the online repository.

If you navigate to your repository on GitHub, you should now see your project is online!









