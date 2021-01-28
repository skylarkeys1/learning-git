# learning-git
This is a simple repo designed for learning git.

In general there's no reason to clone this unless you wish to learn how to work with git and manage a git repository.

## Creating a branch from current point
To create a branch from the current state of the repo, run the command below replacing values in `<>` with desired values.

```bash
git checkout -b <new_branch>
```

## Add your first commit
Open up this file and add you name below to the user list:

-  SaikWolf
-  Skylar Keys

The above should now include previous commiters along with you.

To commit those changes run one of the following.

```bash
git add README.md
git commit -m "Adding name to the README - following the guide."
```

Those commands add the changed file to be committed/tracked.
Then commits the added files with the flag `-m` for commiting with and inline comment, rather than opening up the editor afterward and writing the comment there.



## Push a branch to the remote manager
Now lets make sure those changes are backed up to the location we've pulled them from.
```bash
git push -u origin <new_branch>
```
Finally, the last command pushes the branch you've created with the change you've made back to `origin` or the original location of the repo that you cloned from.

NOTE: This command might not work depending on the remote manager, you might not have authority to push to the origin. On GitHub, what you can do is in your account you can `fork` the repository to your own space. Then you can add a remote location like in the next step.

## Working on GitHub
### Fork the repository
Going back to the source repository below: (learning-git](https://github.com/SaikWolf/learning-git)

In the top right corner, you'll see a `fork` button. Pressing that forks the current repository and make a unique copy within your own GitHub space.

Then we just need to let the local repository know there's a new location to backup work.


### Adding a new remote
Go to your new repository space, copy the URL and then run the following

```bash
git remote add <alias for your remote> <paste URL>
```

### Pushing (the first time)
Now we want to push the current repo to the new backup/remote location

So run:

```bash
git push -u <alias for your remote> <new_branch>
```

All other times you need to push the following can be run

```bash
git push <alias for your remote>
```

### Deleting a remote and working from the new remote only
Or if you want to purely work from your fork'd repo and don't want to keep track of the original repo anymore

```bash
git remote remove origin
git remote add origin <paste URL>
git push -U origin <new_branch>
...
git push
```

# Final task
Create a `helloworld` program where the source code has been put into a `src` folder along with the makefile that will build and execute it.

Then commit the code and push it back to GitHub.

Finally, submit a merge request back to the original GitHub Repo. https://github.com/SaikWolf/learning-git

# Cheers








