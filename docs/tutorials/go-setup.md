# Go Tutorial
In this tutorial, you'll learn how to set up a development environment for Go using Docker, Visual Studio Code, and Git. By the end of this tutorial, you'll have a fully functional Go project, running in a VS Code dev container, and you'll know how to write, build, and run a simple Go program.

---
## Prerequisites 
1. Docker Desktop App
2. Visual Studio Code
3. Git
---
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
!!! note
    - "name" is simply what you are calling your dev container
    - "image" defines the Docker image to use, in this case the latest version of a Go environment
    - "customizations" is useful when you want to add any important extenisions to make sure your project works for anyone using your dev container


## Creating the Go Project
1. Before you begin, you must reopen your project in a VS Code Dev Container. To do this, press Ctrl+Shift+P (or Cmd+Shift+P on Mac), search for "Dev Contianers: Reopen in Container" and select this option.
2. Once it opens, try running ```go version``` in your terminal to check if you are on the latest version of Go.
![Screenshot of Go version](/assets/images/goversionss.jpg "SS of version")
3. Now create a new directory named "hello" to add your Go program by using the following commands in the terminal:
``` bash
mkdir hello
cd hello
```
4. Enable dependency tracking for your code by using the command ```go mod init example/hello```. It will create a go.mod file in your hello directory.
5. Now create a new hello.go file in your hello directory to write your program.
6. Paste the following code into your hello.go file:
``` go
package main

import "fmt"

func main() {
  fmt.Println("Hello COMP423")
}
```
7. Now when you run ```go run .``` in your terminal, "Hello COMP423" should print out.

!!! note
    Instead of using the ```run``` subcommand, which builds your code into a executable binary and then runs it, you could use the ```build``` subcommand to only build your code into an executable binary file and you can choose to run it manually or distribute it to your liking. To use the ```build``` subcommand, type ```go build hello.go``` in your terminal, and then you can run it by running ```./hello``` in your terminal, which prints out "Hello COMP423".

## References
1. [Starting a Static Website Project with MkDocs](https://comp423-25s.github.io/resources/MkDocs/tutorial/#step-2-add-requirementstxt-python-dependency-configuration)

## Contributors
* Primary author: [Miguel Alvarado Dorado](https://github.com/miguelaa123)
* Reviewer: [Boluwatife Adeshina](https://github.com/boluwatifeda)