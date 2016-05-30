# Accept Pull Request

Github

---

## Accept Pull Request
Press **Merge Pull Request** button can merge pull request to repository.

## Things to be done befor Accept 
1. code examination
2. see the differences between 2 pictures.

## The step of check Pull Request in local
Example:
    *Receive: ituring;   Delivery:PR*
    
1.  Refresh the receive repository
    ```git
    $ git clone git@github.com:ituring/first-pr.git
$ cd first-pr
    ```

1.  Achieve the delivery remote repository
Set PR's repository as the remote repository of the locol repository.
    ```git
    $ git remote add PR git@github.com/PR/first-pr.git
$ git fetch PR
    ```

1. create a branch to check
We just achieve the data of remote repository, but it's still not in branch. So we create a branch to imitate the status if we accept Pull Request.
    ```git
    $ git checkout -b pr1
    ```

1. Merge
This step is to merge the fetched PR edit content with pr1 branch.
    ```git
    $ git merge PR/work
    ```
After this, pr1 is merged into the edit content from PR/work.
So we can test if the code can work well.

1. Delect Branch
After check, pr1 is useless. So we delete pr1.
    ```git
    $ git branch -D pr1
    ```

## Accept Pull Request
If you ensure the Pull Request is well, open your browser and press **Merge Pull Request**. And the content of Pull Request will be merged into repository.

There is another way. Because we built a same environment in local, so we merge and push into Github, the Pull Request will reveal the status that Pull Request is accepted. The step is as follows.
1 Merge into Master
```git
$ git checkout gh-pages
$ git merge PR/work
```
2  Push the amend content
To ensure, we should check the different between local and remote first.
```git
$ git diff origin/gh-pages
```
If there is no fault, then push it.
```git
$ git push
```
Then, the Pull Request will turns out to be closed.


