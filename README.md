# 1678 Super Scout 2018

This is a guideline for handling and contributing to the 2018 season’s projects.


## Application Information
									
Collects more subjective data on comparative robot performance on the field, such as robot speed, agility, and defense. Generally used by a team member who is able to effectively rank the three robots playing on their assigned alliance from best to worst in each category. 1 Super Scout collects data on each alliance in each qualifying match. 												
## Use Notes

See the [Super Scout](https://docs.google.com/document/d/159PaCnExGtZYFpsA3HxMCevKZBWVccw01g_FTKpb3ww/edit) section in the Basic App Requirements doc for more details on the Scout.

## Style Guide

Use standard Android/Java code conventions. See [here](https://source.android.com/setup/code-style) for more information.
	
## Commit Guide

You should also make sure that you are writing good commit messages! Here are a couple articles on this: [1](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) [2](http://chris.beams.io/posts/git-commit/).

Particularly, you should make sure to write your commits in the imperative mood ("Add somefeature", not "Added somefeature") and capitalize the first word. If the change is complicated, use multiple lines to describe it.

Additionally, you should try to make your commits as small as possible (often referred to as making "atomic" commits). This helps other people understand what you are doing.


## Contributing

Here's how to get your code into the main project repository:


### If you've just joined the team:

1. Make an account on GitHub.
2. Ask the App Programming lead to add your account to the frc1678 repositories.


### If it's the first time you contributed to a repo:

1. Fork the repo
  	+ Login to github and navigate to the repo.
  	+ Click the "Fork" button in the upper right corner of the screen.
2. Clone your forked repo.
 	 + `git clone https://github.com/<your_name>/<repo_name>.git`, where `<your_name>` is your github username and `<repo_name>` is the project repository name (eg. scout-2017, server-2017).
3. Add a remote for the upstream main repository you forked.
	* `git remote add upstream https://github.com/frc1678/<repo_name>`


### Keeping your fork up to date:

You should **always** update your forked remote before you start working.

1. First, make sure you are on your local **master** branch. 
	* `git checkout master`
   If you are currently working on changes in another branch, * `add`, * `commit`, and * `push` those changes to your **forked repo** before checking out to the master branch.

2. Next, fetch the branches of your upstream remote
	* `git fetch upstream` to fetch all the branches
	* `git branch -a` to see all the branches, both local and remote

3. Now, merge your local master branch with the master branch of the upstream remote
	* `git pull upstream master` to update your local branch master with the upstream/main repository master branch

4. Finally, push to your forked repo to update your forked repository on Github
	* `git push <your-forked-remote’s name>  master`
See [here](https://gist.github.com/Chaser324/ce0505fbed06b947d962) for more information.


### Anytime you want to make a change:

1. Update your fork's master branch.
2. Create and checkout a **new branch**.
 	 * `git checkout -b <your-branch-name>`, where `<your-branch-name>` is a descriptive name for your branch. Use dashes in the branch name, not underscores.
3. Make whatever code changes you want/need/ to make. Be sure to test your changes!
4. Commit your work locally.
  	+ Try to make your commits as atomic (small) as possible. For example, moving functions around should be different from adding features, and changes to one subsystem should be in a different commit than changes to another subsystem.
 	 + Follow [these](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) conventions for commit messages.
 	 + If your change is anything more than a few lines or small fixes, don't skip the extended description. If you are always using git commit with the -m option, stop doing that.
See this [stackoverflow question](https://stackoverflow.com/questions/9562304/github-commit-with-extended-message) for instructions on how to write an extended commit description.
 	 + `git push origin <your_branch_name>`.
	+ Make sure to update version_number in strings.xml **before** submitting a pull request.
	 + Use the format yy.mm.dd:[# that your pull request will be]. For example, if I mke a pull request on 3/10/2018, and the most recently closed pull request is #42, the version number will be "18.03.10:43".
6. Submit a pull request.
 	 1. Log into github.
 	 2. Go to the page for your forked repo.
 	 3. Select the branch that you just pushed from the "Branch" dropdown menu.
 	 4. Click "New Pull Request".
 	 5. Review the changes that you made.
 	 6. If you are happy with your changes, click "Create Pull Request".
 7. Wait
 	 + People must review (and approve of) your changes before they are merged.
  	 + Specifically, ***2 experienced students*** contributing to that project have to approve it
 	 + If there are any concerns about your pull request, fix them. Depending on how severe the concerns are, the pull request may be merged without it, but everyone will be happier if you fix your code. To update your PR, just push to the branch on your forked repo.
  	+ Don't dismiss someone's review when you make changes - instead, ask them to re-review it.
8. Merge your changes into master
	  + If there are no conflicts, push the "Squash and merge" button, write a good commit message, and merge the changes.
 	 + If there are conflicts, fix them locally on your branch, push them, and then squash and merge.


## Helpful Tips

### Other remotes

You can add "remotes" to github that refer to other people's robot code repos. This allows you to, for example, take a look at someone else's code to look over it. You would be able to `git checkout <name_of_person>/juicy-commit` to see it. To add a remote, just do `git remote add <name_of_person> https://github.com/<username>/<repo_name>.git`. Once you've done this, you can use `git fetch <name_of_person>` to get updated code from other people's repos!