---
layout: base
title: Tips
permalink: /tips/
---

## Places To Change Repository Name
- In order to have a functioning repo that is deployed on github pages you need to change the name of your repo in 3 locations.
    - Makefile
    - _config.yml "gitub_repo"
    - _config.yml "baseurl"

## Aliases
> Aliases are user-defined strings that replace a command or series of commands that produce the same results as the original command. They can greatly improve a user's efficiency and command line experience

### Creating temporary Aliases
- When you want to create a temporary alias, all you have to do is type ```alias``` followed by an ```=``` sign and then the quote of the command you want to alias. **To string together two commands you can join the two commands with a ;**

Ex: ```alias shortname="command1;command2"```

- Check all defined aliases with: ```alias -p```

### Saving Aliases
- When saving aliases across sessions you can save them in one of the following files depending on your user's shell. 

    - Bash - ~/.bashrc
    - ZSH - ~/.zshrc
- For bash open the .bashrc file and find a place in the file to store custom aliases and enter your alias.
Ex: ```alias shortname"command1;command2```

- Now load your alias with ```source ~/.bashrc``` or start a new session and the file will be loaded automatically

### Removing Aliases
- To remove an alias use the unalias command.
```unalias alias name```
- To remove all aliases
```unalias -a```

