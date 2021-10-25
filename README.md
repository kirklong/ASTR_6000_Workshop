# ASTR 6000 Git/GitHub Workshop

We're going to use this repo as an interactive exercise to learn how to collaborate with Git/GitHub together!

## Step 0: Setting up your Github

If you don't have a GitHub account yet, make one [here](https://github.com/join). If you already have a GitHub account make sure [you've set up SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) &mdash; you won't be able to push to your repositories without a "more secure" way than simply entering your username and password, and this is the preferred way. Aimee and I are happy to help you figure this out really quick if you haven't done it before! You can check if you already have this setup by entering the following in a terminal:

```bash
ssh - T git@github.com
```

Which should spit out a message telling you if you've successfully authenticated or not.

## Step 1: Forking this repository

Forking is a common way open-source projects work with their communities. You may find an interesting bit of code for your job or research that's open source that you would like to modify, but you may not know the creator / work with them directly, and this is where forking comes in! Forking allows you to make a copy of any repository as it is right now that then allows you to make your own changes. If you make changes that benefit the community as a whole you can later request that those changes be merged into the parent repository through what's called a "pull request" &mdash; we will practice this later. Follow [these instructions](https://docs.github.com/en/get-started/quickstart/fork-a-repo) to fork this repository.

## Step 2: Making a new branch

When you're testing new ideas in your code it's often best to create a "branch" instead of committing to main directly. This allows you to experiment and test changes without breaking your existing code &mdash; once you're satisfied that whatever you've done won't break your existing code you can then merge your branch with your main project to incrementally and safely update it. We'll practice this now. Create a new branch by typing:

```bash
git branch dev main
git push -u origin dev
git checkout dev
```

This makes a new branch called "dev" (you can name yours whatever you want) that is based on your existing "main" branch, with the second line telling git that you would like to be able to push/pull from the remote version of your repository on GitHub, and the third line telling git that now you would like to work on this new development branch instead of your main one. There are many other command line options for this that allow more specificity you can read about [here](https://www.git-tower.com/learn/git/faq/create-branch/). [You can also complete these steps graphically from your repository's page on GitHub](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository).

## Step 3: Changing something and making a commit

When working in teams often small groups and individuals will work on specific features/problems. Pretend you're doing just that, and you've just developed an awesome new bit of code to add to the project. Create a dummy file (you can put actual code in it if you want, but this is not required), add it to your branch, and then commit your changes. Here's an example from the command line:

```bash
touch dummyFile.txt
git add dummyFile.txt
git commit -m "description of cool new feature!"
git push origin -u
```

The first line creates a dummy text file (with nothing in it), the second tells git to add it to the list of files it should keep track of, the third commits this staged change (officially adds the new file to this "version" of your branch), and the fourth sends an update to the version of your branch on GitHub. You should be able to check your repository on GitHub and see that your new file exists there! When you do this name your file something unique &mdash; later we will want to sync all our repositories together as if we were working on a real team, and we don't want to have naming conflicts!

## Step 4: Merging your changes with main

Now that you've successfully tested and implemented your new code it's time to merge our changes with our main branch. This is important because you'll naturally want to keep building on your work, and it's best to make new branches each time you want to make a new feature instead of keeping everything all in one place. We accomplish this with a [pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request). Follow the link above and see if you can successfully merge your changes from your "dev" branch to main! After doing this you can now switch back to the "main" branch by typing `git checkout main` and updating it to reflect your merge by typing `git pull`. You can also safely delete your old branch if you like, but it's not required.

## Step 5: Submitting a pull request to a larger project

Suppose now you're really proud of all the work you've done on this fork of my repo, and you think everyone who uses this project would benefit from your changes. You can submit a pull request of your fork to me (the project owner) and I can then merge your changes into the official repository so that everyone who uses this project can benefit. This is how a lot of large open-source projects operate, including packages you probably use everyday like matplotlib, numpy, scipy, etc. Follow [these steps](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) to initiate a pull request to me, and I'll show you how it looks from my end as well!

## Step 6: Profit!

This concludes our "fun" tutorial on Git/GitHub/code collaboration basics. There's a lot more to learn, but hopefully this is a good starting place and you now feel more comfortable with this sort of thing! A final point on something we didn't practice &mdash; what if you want to undo your changes? Sometimes (okay, most of the time) things unexpectedly break and you may want to go back to an earlier version of your code. That's the power of git! You can always revert to a previous commit and undo breaking changes, and here's a [nice resource](https://medium.com/coder-nomad/how-to-reset-your-git-branch-to-a-previous-commit-both-local-and-remote-55e0351dca2b) on what to do when things break. Finally, here's a [nice resource](https://github.com/grandcircusco/cheatsheets/blob/master/git-commands-cheat-sheet.md#:~:text=Git%20Commands%20Cheat%20Sheet%201%20Upload%20a%20new,commands.%20Only%20do%20this%20once%20per%20project.%20) of command git commands and what they do that I often refer back to.
