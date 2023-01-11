# This guide offers useful tricks to use Git with R-Studio

## Prerequisites
* [Git](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/GithubConfig.md) must be installed and configured
* You should know the basic concepts of using [GitBash](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/WorkingGit.md) to understand underlying processes
* Have R-Studio installed

## Creating a new project from scratch
- If starting from scratch it is easier to create a github repo, and then import the empty github repo as an R-Studio project

***Please see: "[Creating an empty, new Github Repository](https://github.com/Exeter-Diabetes/All-Github-Guides/blob/main/Repositories.md#creating-an-empty-new-github-repository)"***


## Creating R-Studio project from Github Repository
* Most applicable when you want to import a project from a Github repository to your local environment so you can make changes or code

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
