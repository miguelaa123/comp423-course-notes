# Go Tutorial
## Prerequisites 
1. Docker Desktop App
2. Visual Studio Code
3. Git
4. GitHub Account
## Setting Up a Dev Container for Go
### Step 1: Creating a Local Directory and Initializing with Git
1. Navigate to your terminal/command prompt
2. Create a new directory named "first-go-project" in a directory of your choice
``` bash
mkdir first-go-project
cd first-go-project
```
3. To initialize your new directory with git use: 
``` bash
git init
```
4. Create your first commit with a README file: {insert code block}
### Step 2: Setup a remote repo on GitHub
1. Navigate to your github profile homepage and create a New repo by pressing the green “New” button
2. Once on the create new repo page, fill in the entries with the following:
    1. Repository Name: first-go-project
    2. Description: "This is my first Go project!"
    3. Visibility: Public
    4. Make sure **NOT** to initialize the repo with a README, .gitignore, or license
3. Click Create Repository
Your screen should look something like this: {insert ss}
Press the button to copy your GitHub repo's HTTPS link for the next step.
### Step 3: Link your initalized directory to GitHub
1. Add the GitHub repo as a remote by using the HTTPS link you previously copied in the git command: {insert codeblock}
## Dev Container Configuration
1. Before you begin, install the Dev Containers extension for VS Code
2. Now open your first-go-project directory in VS Code
3. Create a .devcontainer directory in your project directory with a file named devcontainer.json with the following content, changing "latest" to the lastest version of Go when you are completing this tutorial:
``` json
{
  "name": "First Go Project",
  "image": "mcr.microsoft.com/vscode/devcontainers/go:latest",
  "customizations": {
    "vscode": {
      "settings": {},
      "extensions": ["ms-vscode.go"]
    }
  }
}
```
4. 
## Creating a new Project in Go
## References
1. [Starting a Static Website Project with MkDocs](https://comp423-25s.github.io/resources/MkDocs/tutorial/#step-2-add-requirementstxt-python-dependency-configuration)
## Contributors
* Primary author: [Miguel Alvarado Dorado](https://github.com/miguelaa123)
* Reviewer: [Boluwatife Adeshina](https://github.com/boluwatifeda)