# windows_secrets_tricks
In this repository some windows cool tricks are documented



## use windows colortool  to change your command prompt color themes

### step 1

Download the colortool utils from [this](https://github.com/Microsoft/Terminal/tree/master/src/tools/ColorTool) repository.

### step 2

Unzip the colortool.zip file and copy it to your program file folder.

### step 3

Add this folder to your path.

### step 3
Run the following command to your console ( cmd, powershell, etc..):

colortool [scheme name in schemes/ e.g: campbell]

Example run the command in your console:
colortool -b solarized_dark.itermcolors

and finally :
Right click on the window title to access the ‘Properties’ dialogue box
Once the properties dialogue box opens press OK (which saves the color change)


## Solve sublime text 3 latextools error COULD NOT COMPILE! 
### This is the error

TraditionalBuilder: Invoking pdflatex... 

COULD NOT COMPILE!

Attempted command:pdflatex -b -p --tex-option="--synctex=1" filename.tex
Build engine: Traditional Builder

### This is the solution (simple)

Do not open sublime text 3 using the "subl" command line command.
use the "sublime_text" command instead or open sublime text 3 from menu icon and everything will compile now correctly.

That's.


  
##  Sublime Text 3.x (after Build 32XX)

1. Add this to your windows hosts.

- hosts location: C:\Windows\System32\drivers\etc

- paste the following strings

```
127.0.0.1 www.sublimetext.com
127.0.0.1 license.sublimehq.com

```

2. copy and paste the following linc key.

```

—– BEGIN LICENSE —–
Member J2TeaM
Single User License
EA7E-1011316
D7DA350E 1B8B0760 972F8B60 F3E64036
B9B4E234 F356F38F 0AD1E3B7 0E9C5FAD
FA0A2ABE 25F65BD8 D51458E5 3923CE80
87428428 79079A01 AA69F319 A1AF29A4
A684C2DC 0B1583D4 19CBD290 217618CD
5653E0A0 BACE3948 BB2EE45E 422D2C87
DD9AF44B 99C49590 D2DBDEE1 75860FD2
8C8BB2AD B2ECE5A4 EFC08AF2 25A9B864
—— END LICENSE ——​

```

### Setting conda (ananconda) in sublime text 3

1. install conda package from the control package of sublime text 3
2. open the conda user setting file an configure like this

```Javascript

// Default settings for sublime-text-conda:
{
    // executable is the path to anaconda's python
    // this python executable is used in order to find conda
    "executable": "C:\\ProgramData\\Anaconda3\\python",

    // Directory in which the conda envs are stored
    // Default location is the user's home directory
    "environment_directory": "C:\\ProgramData\\Anaconda3\\envs\\",

    // configuration is the path to conda's configuration file
    "configuration": "C:\\Users\\liedji\\.condarc",

    // when true, the scripts will be run through the shell
    // If your code has a GUI (e.g. a matplotlib plot),
    // this needs to be true, otherwise Windows suppresses it.
    "run_through_shell": false,

    // when true, the script execution will be handed over to
    // the pythonw executable, instead of python
    "use_pythonw": false,
}

```
3. Use conda as your build system 
4. Type (ctrl+shift+P) and chose your conda environnement (root(python3) or python2 or other)

That is !

### Setting sublime text for c/c++ program including user headers files
1. create a new folder inside your project folder and name it *lib*
2. add this following code to your build system and name *c-cpp-build*

```Javascript
{
    "cmd": "g++ -Wall ${file_path}/lib/*.cpp ${file} -o ${file_base_name} && ${file_base_name}",
    "selector": "source.c++",
    "working_dir": "${file_path}",
    "shell": true,


    "variants": [
        {
            "name": "Run",
            "cmd": "g++ -Wall ${file_path}/lib/*.cpp ${file} -o ${file_base_name} && ${file_base_name}",
            "working_dir": "${file_path}",
            "shell": true

        }
     ]

}

```
3. make sure that all your header files are inside the *lib* folder and finally use ctrl+B or ctrl+shift+b and select *c-cpp-build* as your build system.
