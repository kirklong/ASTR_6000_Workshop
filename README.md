# ASTR 6000 Git Workshop

We're going to use this repo as an interactive exercise to learn Git together!

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

This makes a new branch called "dev" that is based on your existing "main" branch, with the second line telling git that you would like to be able to push/pull from the remote version of your repository on GitHub, and the third line telling git that now you would like to work on this new development branch instead of your main one. There are many other command line options for this that allow more specificity you can read about [here](https://www.git-tower.com/learn/git/faq/create-branch/). [You can also complete these steps graphically from your repository's page on GitHub](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository).

## Step 3: Changing something and making a commit

When working in teams often small groups and individuals will work on specific features/problems. Pretend you're doing just that, and you've just developed an awesome new bit of code to add to the project. Create a dummy file (you can put actual code in it if you want, but this is not required), add it to your branch, and then commit your changes. Here's an example from the command line:

```bash
touch dummyFile.txt
git add dummyFile.txt
git commit -m "description of cool new feature!"
git push origin -u
```

The first line creates a dummy text file (with nothing in it), the second tells git to add it to the list of files it should keep track of, the third commits this staged change (officially adds the new file to this "version" of your branch), and the fourth sends an update to the version of your branch on GitHub. You should be able to check your repository on GitHub and see that your new file exists there! When you do this name your file something unique &mdash; later we will want to sync all our repositories together as if we were working on a real team, and we don't want to have naming conflicts!

## Step 4: 
