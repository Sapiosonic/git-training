# GIT BASICS

## WHAT'S IN IT FOR ME?

- GIT BASICS WITH EXAMPLES

- STEPS TO INSTALL GIT ON WINDOWS, MAC AND LINUX

- GIT CONFIGURATION LEVELS

- STEPS TO CONFIGURE GIT

## INTRODUCTION TO GIT

GIT PROVIDES:

- FLEXIBLE ENVIRONMENT

- VERSION CONTROL SYSTEM

1. TO MODIFY

2. TO RECORD

3. TO REVERT

4. TO CONTROL

5. TO MANAGE

6. TO MERGE

- CREATE AND MANAGE REPOSITORIES

- FACILITATES BRANCHING AND MERGING REPOSITORIES

- KEEPS THE FILE IN THE SERVER SECURE (LOCALLY)

## WHY CHOSE GIT OVER OTHER CONTROL SYSTEMS?

### LIMITATIONS OF EXISTING VERSION CONTROL SYSTEMS:

- EXISTING VERSION CONTROL SYSTEMMS HAVE A CENTRALIZED ARCHITECTURE

- CHANGES CANNOT BE DONE OFFLINE

- RETRIEVE FILES > MAKE CHANGES > COMMIT

- ALL CHANGES MADE IN CENTRAL SERVERS

## WHAT IS GIT?

- GIT IS A VERSION CONTROL SYSTEM

- IT WAS ORIGINALLY DEVELOPED BY LINUS TORVALDS IN 2005

## INSTALLING GIT ON WINDOWS:

- DOWNLOAD FROM THE [LINK](https://git-scm.com/)

- IN 'GNU GENERAL PUBLIC LICENSE' SCREEN CLICK NEXT

- SELECT THE FOLDER WHERE YOU WANT TO INSTALL AND CLICK NEXT

- KEEP THE DEFAULT ELEMENTS CHECKED AND CLICK NEXT

- ON THE 'SELECT START MENU FOLDER' SCREEN KEEP THE DEFAULT ELEMENT AND CLICK NEXT

- ON THE 'ADJUSTING YOUR PATH ENVIRONMENT' SCREEN SELECT THE OPTION 'USE GIT FROM WINDOWS COMMAND PROMPT' AND CLICK NEXT

- ON THE 'CONFIGURING THE LINE ENDING CONVERSIONS SELECT THE 'CHECKOUT WINDOWS-STYLE, COMMIT-UNIX STYLE LINE ENDINGS' OPTION AND CLICK NEXT

- ON THE 'CONFIGURING THE TERMINAL EMULATOR TO USE WITH GIT BASH' SELECT THE 'USE MINTTY (THE DEFAULT TERMINAL OF MSYS2) OPTION AND CLICK NEXT

- ON THE 'CONFIGURING EXTRA POINTS' SCREEN KEEP BOTH 'ENABLE FILE SYSTEM CACHING' AND 'ENABLE GIT CREDENTIAAL MANAGER' BOXES CHECKED AND CLICK INSTALL

- WAIT FOR THE INSTALLATION TO FINISH

- SELECT LAUNCH GIT BASH AND CLICK FINISH

- OPEN THE GIT CMD FROM THE PROGRAM MENU

- EXECUTE git --version TO VERIFY YOUR INSTALLATION

## GIT CONFIGURATION LEVELS

THERE ARE THREE LEVELS OF CONFIGURATION IN GIT:

### --SYSTEM LEVEL

- IT IS THE TOP MOST LEVEL, IT IS APPLICABLE TO EVERYONE WHO USES GIT ON THE SYSTEM WHERE GIT IS INSTALLED 

- THE SETTINGS ARE DEFINED USING THE COMMAND: 'git config --system' which is saved to: /etc/gitconfig

### --GLOBAL

- IT REFERS TO USERS SETTINGS IN ALL REPOSITORIES, THE SETTINGS ARE DEFINED USING 'git config --global' and are saved to ~/.gitconfig (on windows it would be Users/...)

### --LOCAL

- It refers to the user in the repository level. The settings are defined using 'git config --local' (or just 'git config') and are saved to .git/config


- All the files follow the same pattern independently of the level 

- Note Local overrides Global and Global overrrides System level

- the following settings needs to be configured for all commits:

1. user.name

2. user.email


## WHAT IS THE MINIMUN CONFIG TO CONFIG YOUR GIT?

Invoke the "git commit" method in the Git console

git commit -m "initial version"

Git indicates two missing configurations: "user.name" and "user.email" that need to be defined at a global level.

user.name and user.email are mainly configured to associate commit actions to a particular person

There are several otther configurations that should be made

Configure Git at a global level and choose a color of the UI to define the configuration of the editor:

git config --global color.ui "auto"

git config --global core.editor "'C:\Program Files\Sublime Text 3\sublime_text.exe'"

For informations related to the number of configurations execute $ git config --list

View the details of core editor, user.name, user.email, and color.ui, and access the effective configurations.

To check the configuration level, execute: $ git config --global user.name

These configurations are  stored in the .gitconfig file in the user directory and defines all global configurations

## LESSON 2 - GETTING STARTED WITH GIT

### STEPS TP CREATE A GIT REPOSITORY:

CREATE AN EMPTY DIRECTORY

- cpmmand: $$ mkdir <directory-name></directory-name>

CONVERT THE DIRECTORY INTO REPOSITORY

- commandd: $ git init

RUN GIT STATUS

- command: $ git status

- NOTE!!! $ git init command creates a hidden directory that stores all the metadata required for it to function.

## GIT WORKOFLOW

### GIT'S THREE STAGE WORKFLOW

- GIT MAINTAINS THREE SNAPSHOTS OF A FILE IN SEPARATE DIRECTORIES

1. WORKING DIRECTORY: THE FILES ADDED TO THIS DIRECTORY ARE UNTRACKED. IN ORDER TO TRACK THESE FILES YOU SHOULD MOVE THE FILES TO AN STAGING AREA BY USING THE  $ git add COMMAND.

2. THESE FILES ARE NOW STORED IN  .git/index file LATER THIS FILES ARE COMMITED TO THE LOCAL REPOSITORY USING THE $ git commit COMMAND

- WHILE COMMITTING, IT IS IMPORTANT TO ADD A MESSAGE STRING USING THE -m FLAG. IF MISSED, A DEFAULT EDITOR OPENS ASKING FOR COMMENTS.

## MANAGING AND VIEWING CHANGES

- TO MODIFY A FINLE IN GIT -> UPDATE -> ADD -> COMMIT

$ git log -> view the changes in a file  1. commit ID
                                         2. author
                                         3. date
                                         4. commit message


TO RESTRICT THE OUTPUT TO ONE-LINE, EXECUTE: $ git log --oneliner THIS WILL DISPLAY THE INFORMATION IN A SINGLE LINE

