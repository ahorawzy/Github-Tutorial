# Send Pull Request

Github

---

## What is Pull Request?

Pull Request is tha act when you edit the code and wish to be merged and admitted in other's repository.

When you delivery a Pull Request, the manager's repository will receive a Issue with code.

The Pull Request will be admitted or not is determined by manager of repository. If it's not admitted, usually you will receive a comment.
If your Pull Request is admitted, you will be a Contributor of the repository.

## What is the step?

### Step 01: Fork
Fork the repository you would like to edit.

### Step 02: Clone
Clone the repository to your disk.use code like this

```git
$ git clone git@github.com:user_name/repository_name.git
```
### Step 03: Branch

The good habit that edit code in topic branch should be cultivated.

1. confirm branch
    ```git
    $ git branch -a
    ```
    
1.  create topic branch
    ```git
    $ git checkout -b work gh-pages
    ```
work is the topic branch, gh-pages is the raw branch

    ```git
    $ git branch -a
    ```
confirm again

    ```git
    ls
    ```
check the file list

1. edit
    edit code

1. commit
    use git diff to confirm
    ```git
    git diff
    ```

    add and commit
    ```git
    $ git add file
$ git commit -m "message"
    ```
    
1. create remote topic branch
    ```git
    $ git push origin work
$ git branch -a
    ```
## Send Pull Request

Log in Github.

If you confirm this is the exact Pull Request, press the Create Pull Request button and fill a table to comment.

## More Effective way

### Send Pull Request through the progress.
You can send Pull Request when the progress is pushing forward, instead of when the progrogress is over.

In order to prevent the unfinished Pull Request is merged, you can title it [WIP] in the begining.

### Don't Need Fork
If you have the right, you don't need to fork. You can send Pull Request in the branch directly.

## Maintenance of repository

If you fork or clone a repository, it will go far away from the newest origin repository.
So you must maintain the repository to keep the newest status.

### Step01: Fork and Clone
fork on Github
```git
$ git clone git@github.com:user_name/repository_name.git
cd repository_name
```

### Step02: Rename the origin repository
```git
$ git remote add XXX git://github.com/user_name/repository_name.git
```
XXX is the identity of origin repository.

### Step03: Achieve the newest data

```git
git fetch XXX
git merge XXX/master
```



