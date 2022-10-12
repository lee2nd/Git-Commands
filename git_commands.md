Frequenly Used Command During Development:
* Clone a repository
```
$ git clone <.git url> <customized_folder_name>
```

* Pull from remote
```
$ git checkout master
$ git pull origin master
```

* Create a new branch
```
git checkout -b <branch name>
```

* Rebase master if there is an update on remote  
You want to keep up your local master while your branch is developing.
```
$ git checkout master
$ git pull origin master
$ git checkout <branch name>
$ git rebase master
```

* Check log
```
$ git log --oneline
$ git reflog # reference log
```


* Check current status
```
$ git status
```


* Stage file and commit file
```
$ git add <file_name>
$ git commit -m "<Action_do what_by who>" 
```


* Undo commit: undo (1)  
`--hard` : Resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded
```
$ git reset --hard <SOME-COMMIT>
$ git reset HEAD~<#Number, discard number of commit from HEAD> --hard
$ git clean -f  # remove untracked files
```


* Undo commit: get back (2)  
If you want to cancel the undo commit and get back the old commit.
```
$ git reflog show     # the top record is the last movement of HEAD
$ git reset <the commit of the last movement of HEAD> --hard
```


* Unstage file
Reset the buffer zone, staging area
```
$ git reset HEAD <filename>
```


* Push  
`origin`: remote name
```
$ git push origin master     # push local master to remote master
$ git push origin <branch>   # push local branch to remote branch
$ git push origin <branch/HEAD>:master   # push local branch to remote master
```


* Delete Branch
```
$ git branch -a     # push local master to remote master
$ git branch -d <branch>   # delete local branch
$ git push origin --delete <branch>   # delete remote branch

```  

<a href=#mcf><p align='center'>Top</p> </a>
