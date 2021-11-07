# Help me git.
This repo contains nothing but a text file with helpfull little **git commands** that just might make your life easier. Nothing too advance. Just enough to get you going in your day to day git life.

---

### Create a new branch
> Use ```git checkout -b [branch-name]``` if you wish to checkout to a new branch. You will also need to use ```git push --set-upstream origin [branch-name]``` to create the remote branch.

### View local branches only
> Do you want to see all of your branches stored on your local machine? Use the ```git branch``` command.

### View remote/local branches
> If you want a overview of all the branches that your current repo contains, you can use 
```git branch -a```  to see every single one. All the remote branch will be seen as
**remotes/origin/[branch-name]**.

### Update remote branches on local machine
> Incase your remote branches changed and want to bring those changes to your local machine you may use the ```git remote update origin --prune``` command.

### Delete local branches based on remote status
> Sadly a local branch will still remain intact even after deleting your remote branch. This may or may not be what you want. If you wish to delete all the local branches based on the remote branch status, you can use 
```git fetch -p && for branch in $(git branch -vv | grep ': gone]' | awk '{print $1}'); do git branch -D $branch; done```. This will delete your local branch if the remote does not exist anymore.

### Add tracked file/folder to gitignore
> to gitignore a file/folder that already has been tracked, you must remove this file/folder from the tracked data with ```git rm --cached [file/folder]```. After this use the ```git add .``` followed with the ```git commit``` command to complete this process.

