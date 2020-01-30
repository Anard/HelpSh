# HelpSh
Help configuration for shell scripts

File to place in /usr/local/lib for other scripts help
Use on top of your scripts :

- configPath="/usr/local/lib"
- source ${configPath}/help.cnf

In the script, use echo with:

- ${bold}Bold text${normal}
- ${underline}Underlined text${nounderline}

For more specific commands, use echo with option -e and
- ${italic}Italic text${normal}
- ${COLORNAME}Colorized text${nocolor}

All tags can be used together
${normal} tag resets all changes made in Terminal
Read file help.cnf for other tags and colors names
