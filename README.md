# HelpSh
## Help configuration for shell scripts, formatting text in echo commands

File to place in /usr/local/lib for other scripts help
Use on top of your scripts :

```
configPath="/usr/local/lib"
source ${configPath}/help.cnf
```

In the script, use :

```
echo "${bold}Bold text${normal}"
echo "${underline}Underlined text${nounderline}"
```

For more specific commands, use echo with option -e :
```
echo -e "${italic}Italic text${normal}"
echo -e "${blink}Bliniking text${normal}"
echo -e "${invert}Inverted text${normal}"
echo -e "${COLORNAME}Colorized text${nocolor}"
```

All tags can be used together
${normal} tag resets all changes made in Terminal
Read file help.cnf for other tags and colors names

IMPORTANT : Always finish your command by a ${normal}. Else your changes will still apply to every Terminal output.

To write on the same line (echo without new line)
Use echo with option -ne and finish your lines by ${noNewLine}
```
for percent in $(seq 1 100); do
	echo -ne "$percent %${noNewLine}";
	sleep 1;
done
echo
```
