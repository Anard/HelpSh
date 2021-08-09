# shell-text
## decorate texts for shell scripts, formatting text in echo commands

File to place in /usr/lib or /usr/local/lib for other scripts
Use on top of your scripts :

```
configPath="/usr/lib"
source ${configPath}/shell-text.cnf
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

Finally, simply use for multiline decorated texts
```
text=$( cat << EOT
Your multiline
and ${bold}decorated${normal}
text here
EOT
)

echo -e $text
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
