

# Windows Termina Customization

---
## git-bash

### **Adding git-bash**


By installing git-bash, you dot only have the git commands available at shell
but you also will wet some useful linux commands,   
this expecially useful if you are used to linux commands (like ls, vi, mv, grep ... and so on)


## **including git-bash to Windows Terminal**  

after installing the big-bash  
just got to the settings menu and *add* a new *profile*  
the command line should be something like : `C:\Program Files\Git\bin\bash.exe`  

## **customizing git-bash**  

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

