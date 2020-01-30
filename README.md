# HelpSh
Help configuration for shell scripts

File to place in /usr/local/lib for other scripts help
Use on top of your scripts :

- configPath="/usr/local/lib"
- source ${configPath}/help.cnf

In the script, use echo with:

- ${bold}Bold text${normal}
- ${italic}Italic text${normal}
- ${underline}Italic text${nounderline}
- ${COLORNAME}Colorized text${nocolor}

${normmal} tag resets all changes
See file help.cnf for other tags
