# Learn Git

 Github; Git

---

### Basic Operation
1. create a dir:X and initialization

    ```git
    $mkdir X
$cd X
    $git init
    ```

2. see the status of repository
    ```git
    $git status
    ```
3. write code in repository

1. add file in temporary storage

    ```git
    $ git add filename
$ git status
    ```

1. commit the file
    ```git
    $ git commit -m "message"
    ```
    
    or
    ```git
    $ git commit
    ```
then the VIM editor will be opened, and you insert detail message of this change

1. check log

    ```git    
    $ git log
    ```
    
    check log in short 
    ```git
    $ git log --pretty=short
    ```
    
    check log of certain dir/file
    ```git
    $ git log dirname/filename
    ```
    
    check the change
    ```git
    $ git log -p filename
    ```

1. check the differences 
    check the differences between work-tree and temporary-storage
    ```git    
    $git diff
    ```

    check the differences between work-tree and the lastest commit
    ```git
    $git diff HEAD
    ```
    **(it's a good custom that check diff before commit and comfirm)**

### Branch Operation
(the effective way for collaborate-coding)

1. check the branch
    ```git
    $ git branch
    ```

1. create a branch and transfer
    ```git
    $ git checkout -b branchname
    ```    
    
    or
    
    ```git
    $ git branch
$ git checkout branchname
    ```
    
1. topic branch and master branch
    ```git
    $ git checkout master
$ git merge --no-ff branchname
    ```  
     Then VIM launched, and you enter some message and close it.
1. check log as graph
    ```git    
    $ git log --graph
    
    ```

### Change Commit

1. Recall previous version
    ```git
    $ git reset --hard hard-number
    ```
    **(hard-number represents a certain time version)**
    
    
1. Push forward to a future version
    **attention**:
    ```git        
    $ git log
    ```        
    This can only check the log before this version.
    
    Here we can use git reflog, to check all the opertaion and find the certain hard-number.
    ```git
    $ git reflog
$ git checkout master
    $ git reset --hard hard-number
    ```
    
1. solve confliction
    ```git    
    $ git merge --no-ff branchname
    ```
    
    CONFLICT
    Now,open the conflicted file and edit.
    ```git
    $ git add
$ git commit
    ```
    
1. change the commit message
    ```git    
    $ git commit -amend
    ```
    
1. press the history
    ```git    
    $ git rebase -i HEAD~2
    ```

    it turns out:
    ```git
    pick hard1 message
    pick hard2 message
    ```
    
    Amend the second line pick->fixup,save the file and close.
    It turns out rebase success.


