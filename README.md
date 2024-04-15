# C++ Solution For Visual Studio Code
 An example solution for Visual Studio Code to start programming in C++.

## How to use
### Compiler
 First of all, you will need to change the path of the compiler you are going to use inside [.vscode/tasks.json](https://github.com/oscardelgado02/Example-CPP-Solution-For-VSC/blob/main/.vscode/tasks.json) file:
 ```json
{
    "tasks": [
        {
            ...
            "command": "E:\\MinGW\\bin\\g++.exe",
            ...
        }
    ]
}
 ```
In my case, I installed and used [MinGW G++ compiler](https://sourceforge.net/projects/mingw/).

### Add a class to the project
 To add a class, you need to create two files and add them on [src](https://github.com/oscardelgado02/Example-CPP-Solution-For-VSC/tree/main/src) folder:
 - className.cpp
 - className.h

 Also, you will need to add the class cpp path inside [.vscode/tasks.json](https://github.com/oscardelgado02/Example-CPP-Solution-For-VSC/blob/main/.vscode/tasks.json) file:
 ```json
{
    "tasks": [
        {
            ...
            "args": [
                "-fdiagnostics-color=always",
                "-g",
                "${workspaceFolder}\\src\\main.cpp",
                "${workspaceFolder}\\src\\className.cpp", //your class path here

                // you can add more classes here

                "-o",
                "${workspaceFolder}\\program.exe"
            ],
            ...
        }
    ]
}
 ```
