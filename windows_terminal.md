



# Windows Termina Customization

## Table of contents

* [git-bash](#git-bash)
    * [Adding git-bash](#adding-git-bash)
    * [including git-bash to Windows Terminal](#including-git-bash-to-windows-terminal)
    * [customizing git-bash](#customizing-git-bash)
        * [Coloring the shell](#coloring-the-shell)
        * [ANSI Color Escape Codes](#ansi—color-escape-codes)
        * [ANSI Font styles](#ansi-font-styles)



## git-bash

### Adding git-bash


By installing git-bash, you dot only have the git commands available at shell
but you also will wet some useful linux commands,   
this expecially useful if you are used to linux commands (like ls, vi, mv, grep ... and so on)


### Including git-bash to Windows Terminal  

after installing the big-bash  
just got to the settings menu and *add* a new *profile*  
the command line should be something like : `C:\Program Files\Git\bin\bash.exe`  

### Customizing git-bash

the process is very similar to the linux bash way:  

* go to the $HOME folder
* edit the .bashrc file

```
lfriends->~ $  cd $HOME
lfriends->~ $  cat .bashrc
\alias ll='ls -lsah'
PS1="\[\e[97;44m\]\u->\[\e[30;43m\]\w\[\e[97;45m\] $ \[\e[0m\] "
cd $HOME
cd /d
lfriends->~ $ 
```

where the **PS1** variables are:

- `\[\e[97;44m\]` --> set the blue color
- `\u->` --> print the current user name
- `[\e[30;43m\]` --> set the orange color
- `\w` --> print the current path
- `\[\e[97;45m\] $ ` --> set color to purple and print the $ symbol
- `\[\e[0m\] ` --> restore normal colors

<br><br>

##### Coloring the shell

Option| 	Description
----|-----
\e[ | Begin the color modifications
COLORm | Color Code + 'm' at the end
\e[0m| 	End the color modifications


##### ANSI Color Escape Codes

Color |	Foreground |	Background |	
----|----|----|----
Black |	30 |	40 	| ![black](https://placehold.co/15x15/000000/000000.png)  `#000000`
  Red |	31 |	41 	| ![Red](https://placehold.co/15x15/ff0000/ff0000.png) `#ff0000`
Green |	32 |	42 	| ![Green](https://placehold.co/15x15/008000/008000.png) `#008000`
Brown |	33 |	43 	| ![Brown](https://placehold.co/15x15/A52A2A/A52A2A.png) `#A52A2A`
Blue |	34 |	44 	| ![Blue](https://placehold.co/15x15/0000ff/0000ff.png) `#0000ff`
Purple |	35 |	45 |	![Purple](https://placehold.co/15x15/800080/800080.png) `#800080`
Cyan |	36 |	46 	| ![Cyan](https://placehold.co/15x15/00ffff/00ffff.png) `#00ffff`
Light Gray |	37 |	47 | ![Light Gray](https://placehold.co/15x15/D3D3D3/D3D3D3.png)  	`#D3D3D3`

Dark Gray |	1;30| 	1;40 	| ![Dark Gray](https://placehold.co/15x15/A9A9A9/A9A9A9.png) 	`#A9A9A9`
Light Red |	1;31| 	1;41 	| ![Light Red](https://placehold.co/15x15/FF3333/FF3333.png) 	`#FF3333`
Light Green |	1;32 |	1;42 	 | ![Light Green](https://placehold.co/15x15/90EE90/90EE90.png) 	`#90EE90`
Yellow |	1;33 	|1;43 	 | ![Yellow](https://placehold.co/15x15/FFFF00/FFFF00.png) 	`#FFFF00`
Light Blue |	1;34 |	1;44 	| ![Light Blue](https://placehold.co/15x15/728FCE/728FCE.png) 	`#728FCE`
Light Purple |	1;35| 	1;45 	| ![Light Purple](https://placehold.co/15x15/D46FF9/D46FF9.png) 	`#D46FF9`
Light Cyan |1;36| 	1;46 	| ![Light Cyan](https://placehold.co/15x15/e0ffff/e0ffff.png) 	`#e0ffff`
White |	1;37 |	1;47| ![White](https://placehold.co/15x15/ffffff/ffffff.png) 	`#ffffff`

Code: `$ echo -e "\e[31mRed Text\e[0m"`

##### ANSI Font styles 

ANSI Code |	Description | Code
---|---|---
0 |	Normal Characters | ``
1 |	Bold Characters | ``
4 |	Underlined Characters | ``
5 |	Blinking Characters | ``
7 |	Reverse video Characters | 

Code: `$ echo -e "\e[1mBold Text\e[0m"`

Code: `echo -e "\e[1;37;5;41mWhite Blinking Text over Red Background\e[0m"


