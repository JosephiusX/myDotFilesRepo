Notes from this dot files tutorial:   https://www.youtube.com/watch?v=3dUxUcmVROE&t=230s

First step , 4:00 into tutorial. Create a remote github repo for all my dot files. 

        mkdir myDotFilesRepo
Make the repo in git, initilize, and push. 

Now lets say I just want to work on the "waybar" file inside the .config in the home directory. 

        cd .config
        cp -r waybar ~/myDotFilesRepo/
        cd myDotFilesRepo

Add, commit, and push changes.

Next we create a symbolic link after removing original waybar folder(Not repo backup)

        cd .config
        rm -rf waybar/
        ln -s ~/myDotFilesRepo/waybar/ ~/.config/
we should beable to verify with following(detailed list):

        ls -al

Now changes I make in my remote repo will be translated to the config file upon file reload. The repo simply allows me version control. 


We can clone other configure files from the web. we just need to setup the symbolic link. That can be done with a script.

15:55