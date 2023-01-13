# This guide offers useful tricks to use Git with R-Studio

## Prerequisites
* [Git](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/GithubConfig.md) must be installed and configured
* You should know the basic concepts of using [GitBash](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/WorkingGit.md) to understand underlying processes
* Have R-Studio installed

## Creating a new project from scratch
- If starting from scratch it is easier to create a github repository first, and then import the empty github repo as an R-Studio project

1. [Create a new Github Repository](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/Repositories.md#creating-an-empty-new-github-repository)"
2. Once github repository has been set up, follow the "**Creating R-Studio project from Github Repository**" section below to import the repo as an R Project
3. After you have cloned the github repository into your R-studio environment, you can begin creating files and scripts like normal!
   * Just remember to regularly commit your changes and then push those versions to the online repository so it can also stay updated!



## Creating R-Studio project from Github Repository
* Most applicable when you want to import a project from a Github repository to your local environment so you can make changes or create scripts/files

Copying Github repo URL
1. Navigate to the Repository on Github
2. Open the repository and click the green "Code" dropdown menu in the top right
3. Copy the HTTPS link (URL)

Creating new Git-backed R project
1. Navigate to the toolbar in R-Studio and select File > New Project

![Screenshot 2023-01-11 at 15 48 33](https://user-images.githubusercontent.com/85688580/211852432-ca2fdb6a-64a2-4146-bb36-d12e278fddf1.png)

2. Select "Version Control" At the bottom

![Screenshot 2023-01-11 at 15 48 40](https://user-images.githubusercontent.com/85688580/211852809-9b4c2527-ac56-420e-9638-71800ba26d8a.png)

3. Select "Git"

![Screenshot 2023-01-11 at 15 48 50](https://user-images.githubusercontent.com/85688580/211852913-4b0460e4-52f3-4107-a512-5a1fe1696dd7.png)

4. Paste the HTTPS link (URL) from previous section in the "Repository URL" field and name your project in the "Project Directory Name" field.
5. Create project!