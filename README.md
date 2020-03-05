# windows_secrets_tricks
In this repository some windows cool tricks are documented



## use windows colortool  to change your command prompt color themes

### step 1

Download the colortool utils from this repository.

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

TraditionalBuilder: Invoking pdflatex... 

COULD NOT COMPILE!

Attempted command:pdflatex -b -p --tex-option="--synctex=1" filename.tex
Build engine: Traditional Builder

### solution

Do not open sublime text 3 using the "subl" command line command.
use the "sublime_text" command instead or open sublime text 3 from menu icon and everything will compile now correctly.

That's.


  
  
