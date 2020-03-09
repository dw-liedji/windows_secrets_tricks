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

127.0.0.1 www.sublimetext.com
127.0.0.1 license.sublimehq.com


2. copy and paste the following linc key.


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
