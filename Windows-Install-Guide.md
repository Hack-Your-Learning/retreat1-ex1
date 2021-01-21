<div>
<img src="http://drive.google.com/uc?export=view&id=1MADw5CwZYysojTdKwgfJEJpAHdO1Jxoq">
<h1 style="font-family: -apple-system, BlinkMacSystemFont, 'Space Mono', sans-serif;">Git Install Guide - Windows
</h1>
</div>

## 1. Download the installer from https://git-scm.com/downloads 
Click the download button and your download should start immediately. If it doesn't you can manually click Windows 64 bit as shown below. Keep track of where you saved the installer.

![git download website](assets/downloadscreen.PNG)

## 2. Run the installer
You can accept the default for most of the install. However, it is recommended to pause at the following critical steps to double check the information.

### Text editor choice

![Text editor choice](assets/texteditorchoice.PNG).

This step is where you choose your text editor for git bash. It's ok to stick with the default, but if you have a preferred text editor you should specify that here.
### Default branch

![Default branch](assets/defaultbranch.PNG).

It is recommended to choose the default branch name to be "main" since this is what Github uses.
## 3. Start your git bash
- Create a folder to house your project. Change into this folder
- Start a git bash by right clicking and selecting "Git Bash Here". This will open a terminal like that shown below. All your commands in this workshop will be executed in the git bash terminal.

![Open git bash](assets/opengitbash.png)
![Git bash](assets/gitbash.PNG)

## 4. Generate ssh keys
To make our GitHub experience smoother we will generate ssh keys. This allows us to securely communicate with GitHub. If you're interested in how this works you can research public/private key encryption. To generate an ssh key pair type `ssh-keygen`. Accept the defaults.

![ssh-keygen](assets/sshkeygen.PNG)

## 5. Add our ssh keys to GitHub
We now need to add the public key to our GitHub account. 
- Type `cd ~/.ssh`. This will change directory to the folder we just made the keys in. If we type `ls` it will list the contents of this folder. 
- Type `cat id_rsa.pub` to show the contents of your public key. 
- Copy your public key

Next navigate to github.com and create an account if needed. To edit your ssh keys: 
- Click your profile picture in the top right
- Go to settings
- Choose SSH and GPG keys from the sidebar
- Click "New SSH Key".
- Paste the contents of your public key in the key field. The title field doesn't really matter. 
- Click "Add SSH key".

Your ssh keys are now set up.

![Copy key](assets/copysshkey.PNG)  
![Settings](assets/githubsettings.PNG)
![New key](assets/newsshkey.PNG)

## 6. Fork the HYL Repository - only one team member needs to do this!
To work on the HYL project one member of your team will need to fork the repository. To do so, navigate to https://github.com/Hack-Your-Learning/retreat1-ex1. Click "Fork" in the top right corner. This will create a copy of this repository for your team to work on. GitHub should redirect you to your copy when you create it. If it did not you can find your copy by clicking on your profile picture and then "your repositories".

![Fork](assets/fork.PNG)
![Your Repositories](assets/yourrepositories.png)

## 7. Clone the repository
Now that we have our fork on GitHub we need a local copy. We get this copy with the "clone" command. First copy the ssh link by clicking the green "Code" button, choose ssh and then copy the link. Go back to your git bash and `cd` to your project directory. We can clone the project with `git clone <your link>`. If it asks you about adding to known hosts say yes.

![SSH Link](assets/clonessh.PNG)
![Clone Repo](assets/clonerepo.PNG)

## 8. Open in your preferred text editor
You will now be able to open the files in your favourite text editor. Below you can see how to open it in VSCode.

![Open Folder](assets/openfolder.png)
![File System](assets/vscodefilesystem.PNG)

## 9. Add collaborators
If you're working with a team you will want to add collaborators. From your repository's page on GitHub, click
- Settings
- Manage Access
- Invite Collaborator

You can add your collaborators by email or GitHub username. To contribute they should clone the repository as described above. Note that there is no need for your teammates to fork either the HYL repository or your repository! They should *clone* the repository that you have just *forked*.

![Add Collaborator](assets/addcollaborators.png)
