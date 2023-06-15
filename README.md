# **Branches and Pull Requests**

## **Creating a Branch**

There are multiple ways to create a branch in your IDE (Integrated development environment), but this is one of the easiest:

* Go to the GitHub repository for this project.

* You should be able to locate "Branch" (it'll normally say "1 branch" if there's just one, or "2 branches" etc.,). Click it.

![branches](./assets/documentation/readme_images/2%20branches.png)

* Then click "New branch". You can name it whatever but I would recommend calling it your name (in my case, I've named it "keiron").

Done.

Another way:

* Go into your actual IDE, and go to the Source Control panel. This can be found underneath the search tab on the left side of the screen in GitPod (should be the same for Code Anywhere and VSCode).

![source-control](./assets/documentation/readme_images/source_control.png)

* Then click on the three dot dropdown component up top (see attached photo)

![three-dots](./assets/documentation/readme_images/three_dots.png)

* Go to Branch > Create branch > Enter desired branch name

Done. _You will need to "Publish branch" in Source Control_, and then it can be seen in the GitHub Repo.

Once you've done this, in your IDE, go right down to the branch label (I will attach a photo).

![branch-ide](./assets/documentation/readme_images/branch-ide.png)

Click this and it will bring up a list of existing branches. Click the one you have made.

You should notice then that the branch label has changed to your named branch.

**Useful commands**

A list of useful commands when you're working from branches are:

`git status` (tells you which branch you're on and if you're behind/ahead of main branch)

`git pull origin main` (this is very important, please git pull everytime you merge a pull request as it avoids merge conflicts)

`git add`

`git commit -m your commit message`

`git push origin your branch name (I recommend just going into source control and clicking Sync changes)`

`git switch (branch name)` (allows you to switch branch instantaneously)

`git stash` (when you're in the middle of making changes and someone merges a PR, you can git stash your changes away temporarily, git pull from main, and then...)

`git stash pop` (... you can git stash pop your changes back into your IDE. alelujah!)

## **Creating a Pull Request (known as a "PR")**

When you've pushed changes to your branch, you can then head over to the GitHub repository for the Pride Hackathon and normally there appears an unmissable message saying that you can merge changes and begin a pull request.

![unmissable-message](./assets/documentation/readme_images/unmissable-message.png)

In case you've pushed changes and this message doesn't appear, don't worry, just go back into "branches", find your name, and alongside your branch name, there'll be a button for "New Pull Request". I've attached the following photo for reference.

![pr-button](./assets/documentation/readme_images/new%20pr%20button.png)

Once you've begun a PR, it will appear in the "Pull Requests" (next to "Issues") part of the GitHub repository, and you can manage it from there before merging your changes with main.

Please always tag reviewers (you can tag anybody or everybody) to take a look at the changes before merging.

**IMPORTANT**

When you make a branch, _there always exists two versions of it_, one in your IDE and the remote branch in GitHub. This sounds strange at first but it should begin to make sense as you repetitiously use the Git commands.

So when I made 'keiron', I now have the 'keiron' branch open in my IDE (Integrated development environment, which is a fancy way of saying "coding environment", i.e., VSCode, Gitpod, CodeAnywhere etc.), where I am modifying the code. And then I push these changes to the 'keiron' branch in GitHub (_the remote branch_), where I can then merge that branch with the main remote branch.

This is noteworthy because after every successfully merged Pull Request, you must always `git pull origin main` and then go to Source Control and click `Sync Changes`, to make sure the remote version of your branch is also up to date with your coding environment (IDE). If these branches aren't up to date, we could experience what's called a merge conflict, which I will explain below in the potential problems section.

![sync-changes](./assets/documentation/readme_images/sync_changes.png)

**Potential problems**

When a lot of PRs go up, a "merge conflict" can happen. This is okay and it's bound to happen, it's part of the experience of a hackathon as well (and also working in a team). It can occur for a variety of complex reasons.

An example of how it can occur is when changes are being made by various branches on the same content (say that "samuel" and "keiron" are working on the exact same part of the README.md file, and then we do a PR, or if one of us has forgotten to git pull to make sure our IDE and remote branches are up to date before we began our changes).

Of course the best way to avoid it is to try and always make sure your branch is up to date and to work on completely different sections. Make sure we make clear our tasks, roles and what it is we are working on within the file we are working in.

If it happens we will just deal with it but let's try avoid it xD

Do check your branches from time to time either at the bottom of your IDE, or in the GitHub repository to see if you are up to date. If you are, it'll appear as "0|0". If you make sure of this, it'll keep everything clean and we can reduce the risk of merge conflicts. One "0" represents your IDE branch and the other your "remote" branch. Keep these two in sync and at "0|0" as often as humanly possible.

![good-branch](./assets/documentation/readme_images/good%20branch.png)

An example of a badly managed branch is this: 

![bad-branch](./assets/documentation/readme_images/bad%20branch.png)

**Note**

I've tried my best to be as comprehensive as possible in this so that any new-hackathoners and those who are new to branching and PRs can be informed, but overall we will deal with any potential issues as a team. :D