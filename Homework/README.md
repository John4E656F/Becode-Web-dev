# git/github Add, Commit, Push, Pull Request

<p>This is doc is about how to use basic git command</p>

<h2>Branch</h2>

1. git branch (branchname)
    - this will create a new branch
2. git switch (branchname)
    -this will switch the branch

<h2> git add vs git commit vs git push </h2>

1. git add adds your modified files to the queue to be committed later. Files are not committed

2. git commit commits the files that have been added and creates a new revision with a log... If you do not add any files, git will not commit anything. You can combine both actions with git commit -a

3. git push pushes your changes to the remote repository.

This figure from this git cheat sheet gives a good idea of the work flow
![example](https://i.stack.imgur.com/seHhY.png "workflow")

<p>git add isn't on the figure because the suggested way to commit is the combined git commit -a, but you can mentally add a git add to the change block to understand the flow.

Lastly, the reason why push is a separate command is because of git's philosophy. git is a distributed versioning system, and your local working directory is your repository! All changes you commit are instantly reflected and recorded. push is only used to update the remote repo (which you might share with others) when you're done with whatever it is that you're working on. This is a neat way to work and save changes locally (without network overhead) and update it only when you want to, instead of at every commit. This indirectly results in easier commits/branching etc (why not, right? what does it cost you?) which leads to more save points, without messing with the repository.</p>

<h2>Pull Request (PR) in Github</h2>

- git push origin (branchname)
- create a Pull Request from (branchname) to (main)
- merge pull (in github)
- in local terminal
    - git checkout main (switch back to main)
    - git pull origin main (update your local file)