# Github Flow

Github

---

## The attention when team use Github to software development
1. Simple is most.
Every function should be used in progress. The fact is that many functions can't be use. We don't need so much function.
Github is distinct with project manage tool. It use Issues to control most scene in progress.
1. Don't need to fork
Fork can prevent stranger involved in the project. But if the team members must fork every time, it's annoying. So we can empower members don't need to fork.

## Github Flow
It is a sample work flow of development project. It can hold a 15-20 members team to work together.

## Github Flow Path
The flow is as follows.
1. Keep the master ready to arrange every time.
2. A new work should be branched from master. And new branch should have description.
3. Commit in the repository from step2 branch.
4. Create a same-name branch, and push it regularly.
5. When assistance and feedback is needed, Pull Request should be created and members discuss in Pull Request.
6. Check by other member. if no fault, merge to master.
7. Arrange at once when merged.

Attention
1. Keep the master ready to arrange every time is most importent in this flow. After several hours, it should be arranged. There is no concept of Publishing. So it won't happen that HEAD to a long ago version.
The code haven't been test never should be merged into master. So Sustained Integration should be used.
2. Every new branch should be from master. The new branch should be named descriptively.
3. When edit a branch, work not related to the branch should never be done. The scale of Pull Request should be rather small.
4. Push regularly on time to minimize the fault. And every member should read other's code and progress.
5. Pull Request should be put up as soon as possible. Don't Pull Request only when you merge to master.
6. Check should be done by others. If several members admit, merge can be put up.
7. After merge, arrange should be done immediately.

## Prerequisite of using Github Flow
1. auto arrange tool
for example:
Capistrano
(Web) Webistrano/Strano
Fabric(use in Python development)

1. Auto test code


