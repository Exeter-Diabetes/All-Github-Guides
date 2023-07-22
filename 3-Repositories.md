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
8. Under "Quick Setup" you should be able to see an HTTPS button greyed out, with a URL to the right side
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
4. Use the 2 commands below to: Initialize the Git environment within the folder, and then download the project files from online (GitHub) to your local folder
```
git init
git clone [Repository HTTPS link from previous part]
```

## Using your development environment (IDE) with Git
* This is can potentially be a very long section - as there are MANY IDE's each with their own way of integrating with Git and GitHub
* There are plenty of tutorials available for free online (Youtube, "Setting up a GitHub project with \[IDE\]"
* IF YOU ARE USING **R-STUDIO**, be sure to look at our "GitWorkshop_slides1and2.pptx" presentation which goes into much deeper detail of how to connect, integrate and use R-Studio with Git.

## Pushing a local project to a new github repository using Git Command-Line-Interface (CLI)
- This section is most applicable when you have already started or created a coding project on your local device
- If you have a local project and you want to MIGRATE this to the online Exeter-Diabetes Organisation Github

### 1. Create a new Github repository on Exeter-Diabetes
- Use the first section to learn how to create a new repository!
- Once it has been set up and you have the HTTPS link (URL), come back here

### 2. Terminal pointed to local environment (MacOS)
1. As **Mac** and Windows have different file explorers and shell environments, these two require two different set ups.
2. On Finder, find your project folder, which contains all of your project files
3. Right click on the project folder and open a "New terminal at Folder"

### 2. Shell pointed to local environment (Windows)
1. As Mac and **Windows** have different file explorers and environments, these two require two different set ups.
2. On File Explorer, find your project folder, which contains all of your project files
3. Right click on the project folder and "Copy as path" - this will copy the folder's path into your clipboard
4. Open Command Prompt (type "cmd" into the Windows menu), and type "cd " and paste your copied file path.
   - You can right click on the command prompt or use Control + V to paste the folder path.
```
cd [folder path]
```

### 3. Init, Track, Commit, and Remote Add
1. Once terminal is pointing to the correct project folder (previous steps):
2. Initialize the Git environment within the folder by entering the following command into Terminal:
```
git init
```
3. This folder now has Local Version Control enabled thanks to Git! Let's link it up to our online repository so we can start pushing and pulling our latest project versions.
4. We need to tell Git which files we want to push to Github. We can do this by using the $ _git add \[filename.txt\]_
  * It is **SUPER** important that you make sure to not upload any sensitive data, datasets, medical information, etc. online!
  * For more information regarding this, please see our "GitWorkshop_slides1and2.pptx" presentation which goes into greater detail
5. We then need to tell Git to _save_ our changes Locally, and provide a brief description using $ _git commit -m 'message!'_
  * Beware that using this command **DOES NOT SAVE FILE CHANGES**! Git commit tracks the last file version - so make sure to save your files before committing (usually by using Cmd/Control + S)
  * To use git commit, we need to provide an -m 'message', even if the message is blank! Eg. $ git commit -m ''
6. Finally, we need to tell Git _where_ we want to push (save) these selected files online, giving it the URL of our repository we copied earlier
```
git add filename.txt foldername/file-within-folder.py analysis.R
git commit -m ‘initial commit’
git remote add origin [Repository HTTPS URL]
```

### 4. Push
* Congratulations! You have just connected your local project folder to an online repository! No easy task.
* Although we have _connected_ the two, we still actually haven't **pushed** our local project to the online repository - online there is still an empty folder! We need to sync the two.
1. The first time we push via command line, we need to specify which _branch_ we are pushing to. In this case its the origin branch we created earlier.
   * After the initial push, we can simply just use ` git push ` instead.
```
git push origin main
```
* This instructs git to **push** all of the new local versions to the online repository.

If you navigate to your repository on GitHub, you should now see your project is online!

## Additional Support, Detailed walkthrough with images, and Security
* Well done if you were able to follow that the whole way through. If you got lost anywhere - do not fret! Look at our "GitWorkshop_slides1and2.pptx" presentation which goes into much greater detail, step by step, and with images!
* Regarding Security - thoughtfulness and consideration is extremely important when uploading potentially-sensitive information online.
* There are 2 next steps before proceeding onto the next file/section:
  1. Download and look through the security slides on our "GitWorkshop_slides1and2.pptx" presentation! This is of utmost importance so you are an educated Git-er
  2. When in doubt - Don't!! It is better to ask for help to use this complicated software, than dealing with the issues from a data leak.

