# This guide explains how to best use Git with R-Studio

## Prerequisites
* [Git](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/2-GithubConfig.md) must be installed and configured
* You should know the basic concepts of using [GitBash](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/4-GitBash.md) to understand underlying Git processes
* R-Studio installed

## Creating a new project from scratch
If starting from scratch it is easier to create a github repository first, and then import the empty github repo as an R-Studio project

1. [Create a new Github Repository](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/3-Repositories.md#creating-a-new-exeter-diabetes-github-repository)
2. Once github repository has been set up, follow the "**Creating R-Studio project from Github Repository**" section below to import the repo as an R Project
3. After you have cloned the github repository into your R-studio environment, you can begin creating files and scripts like normal!
   * Just remember to regularly commit your changes and then push those versions to the online repository so it can also stay updated!



## Creating R-Studio project from Github Repository (Cloning)
Most applicable when you want to import a project from a Github repository to your local environment so you can make changes or create scripts/files

### Method 1: R-Studio console
* This method uses the built in R-Studio terminal/console and a native function
* Very quick and easy

1. [Copy Github repo URL](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/3-Repositories.md#cloning-a-github-repository-into-a-local-environment)
2. Enter the following commands into the R-Studio console
   * Requires an active R-Studio session (with a console of course)
   * First argument is the HTTPS link to remote Github repository
   * Second argument is the target project folder that R-Studio will create to store the files locally
 ```
 usethis::create_from_github(
  "https://github.com/YOU/YOUR_REPO.git",
  destdir = "~/path/to/where/you/want/the/local/repo/"
)
 ```


### Method 2: Clickity 
* This method relies on clicking through the various options R-Studio offers to set up a new project
* Slightly slower than using console, but more understandable 

1. [Copy Github repo URL](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/3-Repositories.md#cloning-a-github-repository-into-a-local-environment)
2. Navigate to the toolbar in R-Studio and select File > New Project
3. Select "Version Control" At the bottom

![Screenshot 2023-01-11 at 15 48 33](https://user-images.githubusercontent.com/85688580/211852432-ca2fdb6a-64a2-4146-bb36-d12e278fddf1.png)

4. Select "Git"

![Screenshot 2023-01-11 at 15 48 40](https://user-images.githubusercontent.com/85688580/211852809-9b4c2527-ac56-420e-9638-71800ba26d8a.png)

5. Paste the HTTPS link (URL) from previous section in the "Repository URL" field and name your project in the "Project Directory Name" field.
6. Create project!

![Screenshot 2023-01-11 at 15 48 50](https://user-images.githubusercontent.com/85688580/211852913-4b0460e4-52f3-4107-a512-5a1fe1696dd7.png)



## Exporting local project to a new Github repository
* Exporting local projects should **only be done** to migrate OLD projects to Github
* New projects should not be created this way! To learn how to correctly create new projects please view the "**_Creating a new project from scratch_** section above
* Unfortunately, R-Studio does not offer a simple way to create and connect Github repositories for your local projects, so you must use the command line to manually do this

Follow the ["Pushing a local project to a new Github repository" guide](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/3-Repositories.md#pushing-a-local-project-to-a-new-github-repository)
1. Create a new Exeter-Diabetes repository for the project
2. Open shell environment (Terminal or Command Prompt) and point it to project folder
3. Intialise Git ` git init `
4. Track, Commit, Add remote origin and then push!

## Pushing updates
* After connecting local environment and Github repository, you can begin coding!
* Pushing local changes to your Github repository will easily make up majority of your Git use

Commits and Pushing
* Once a project is Git initialised, you can begin committing changes.
* At the top of R-Studio, you can find a "Git" button written vertically, navigate to "Commit..."
![Screenshot 2023-01-13 at 12 29 37](https://user-images.githubusercontent.com/85688580/212321860-05cc701d-3aea-4eca-ad73-cd9432528155.png)

* Clicking on "Commit..." will open a new window that should look similar to this
* In the top left corner are all of the modified files within this project. You must manually select (tick) the files that you want to track (add) for the commit.
  * Rule of thumb: Dont track hidden files that begin with ".", such as ".RData"
  * These files are generally just important for local environments, and can sometimes be quite large
* Once you have selected a file to track for this commit, the bottom section of the window will display all of the code that has been modified since the last version.
  * This is a useful position to review all of the changes you have made, and double-check any new or removed code before submission
  * Green highlighted lines are new
  * Red highlighted lines are deleted
  * It is best practice to use this summary page to write your commit messages
 * In the top right corner there is a text box for you to write your commit message
   * The first line of the text box should be the **title** of your commit, keep it concise (<50 characters)
   * By hitting enter, you can provide more detailed and additional info if you choose to. I personally like to summarise my changes in bullet points
 * Once you have tracked changes, reviewed code, and written a commit message - **You can now click the "Commit" button in the top right**
   * Keep in mind this **does not** push your code to your Github repository, it only creates a new local version.

![Screenshot 2023-01-13 at 12 34 58](https://user-images.githubusercontent.com/85688580/212321802-8c0f3277-1642-491d-87cd-81fe17982cc5.png)

 * **_PUSHING_**: once a commit has been made, the online repository is one version behind your local version, so it is recommended you push straight away so others who might be viewing/working on your code can be updated
 * To push, simply click the "Push" button in the top right!
   * Remember, when working collaboratively, it is best to _pull_ before you _push_
 
 
