## Review of what we've covered in Day 1, part 1: 
#### Getting Ready for Class
- Make sure you have [Git insalled](https://git-scm.com/) on your computer and a [GitHub account](https://github.com/).

#### Getting Started
**Quick review of what we've covered so far:**
- Repository for Class: https://github.com/githubteacher/fluffy-octo-guacamole
- Gitter Q&A for class: https://gitter.im/githubteacher/fluffy-octo-guacamole
- Tour of Repository: 
  - Code View:  Files belonging to the project
  - README.md: Description of the Repository 
  - Issues: A place to have conversations and collaborate
  - Pull requests: A place to collaborate while introducing changes to your project
- Comment on [this issue](https://github.com/githubteacher/fluffy-octo-guacamole/issues/3) to become a collaborator on the project
- Practice making an issue [in the issues tab of the class repository](https://github.com/githubteacher/fluffy-octo-guacamole/issues).
  - For today's activity, be sure to include your username in the title, like "YourUserName Hometown"
  - In the body of the issue, we added the steps we'll take for the workflow. 
  - Our goal later will be to add a document with information about your hometown, like good restaurants or things to do. 
  - You can include [markdown](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf) syntax here.

**Getting access to the collaborator script:**
The collaborator script is open-source! You can access it [here](https://github.com/github/training-utils). Our [training kit](https://github.com/github/training-kit) is also open-source. We invite you to use these and welcome contributions to both these repos!

#### Local Git Configs 
**Review of configurations:**
- We determined our git version by running `git --version`... version 1.9+ is recommended
- If you need to, you can install it [here](https://git-scm.com/)
- If you don't already have GitHub Desktop, you can install it [here](https://desktop.github.com/)
- Clone the repository by running `git clone https://github.com/githubteacher/github-for-developers-2016-04.git` (Make sure you are in the directory where you want the repository to be when you run this command)
- If you have trouble with your proxy server or firewall, you may need to use SSH. Instructions [here](https://help.github.com/articles/generating-an-ssh-key/).
- Set up your Git configurations by running these commands:
  - `git config --global user.name "your name"`
  - `git config --global user.email <youremail@email.com>`
  - `git config --global core.editor <editor>` (For more help associating your text editor with Git, read [this GitHub Help article](https://help.github.com/articles/associating-text-editors-with-git/).
  - If your version is less than 2.0: `git config --global push.default simple`
  - Windows ONLY: `git config --global core.autocrlf true`
  - Mac and Linux ONLY: `git config --global core.autocrlf input`
  - `git config --global fetch.prune true`
- Check your configurations by running `git config --list`

#### GitHub Flow 
**You can find that visual of the GitHub flow at this link:** https://guides.github.com/introduction/flow/

#### Branching with Git 
**Create a branch locally**
- When you create a branch, you are essentially creating an identical copy of the project at that point in time that is completely separate from the master branch.
- In your terminal and in the directory for the repository, create a branch with a unique name: `git branch <username-add-bio>`
- Checkout to that branch to work on it: `git checkout <username-add-bio>`
- See what branch you're on: `git branch`


####_6. Working Locally_
**Review of working locally**
- Working on our new branch, create a new file: `touch <newfilename.md>`
- See your working/staged area  `git status`. This command is :heart:! 


## Notes from Day 1, section 2: 

#### Using Git Locally

1. Change your file from 'working' to 'staging' by running `git add <file-name>`
2. Change your file from 'staging' to 'history' by running `git commit`. (To avoid using the text editor, use `git commit -m "Enter commit message here"`)
3. Text editor opens: Write a 'commit message' tells a story of the changes you just made in 50 characters or less.

- List the files in your current directory by running `ls -la`
- We learned about 'working', 'staging', and 'history' and how commits fit into those areas using [this resource](https://training.github.com/kit/modules/CONT-CLI-04_Two_Stage_Commit.html).
- Create a new file and repeat steps 1 - 3 for the two stage commit. This way, we'll have two commits to work with.
- Here are some shortcuts to know about in the future:
  - To automatically stage all files that have been changed, run `git add -A`. Note: This will only work for files that are already being tracked, not brand new files.
  - Avoid the text editor in the commit by running `git commit -m "commit message"`

#### Collaborating on Code 
**Review of moving from Git to GitHub**
- We talked about _remote_, and how we can see details about it by running `git remote`, `git remote -v`, and `git remote show origin`
- 'Push' our changes on the current branch to GitHub.com by running `git push -u origin <branch-name>`
- If you forget the `-u` tag, set a 'upstream branch' relationship between our local branch and the GitHub.com remote branch by running `git branch --set-upstream-to=origin/<remote-branch-name>`
  - This means we only have to run `git push` and `git pull` in the future
    - git pull is the combination of git fetch and git merge
- `git branch` and `git branch -a` will help you see what is going on with your local and remote branches
- On GitHub.com, open a pull request in our [class repository](https://github.com/githubteacher/github-for-developers-2016-04) by clicking the green "New pull request" button.
  - Make sure your pull request says `base: master` and `compare: <your-new-branch>`
  - Give it a good title and message about the changes you introduced. Bonus points for using [markdown](https://guides.github.com/features/mastering-markdown/) and emojis!
  - You can add labels and assignees to pull requests like we did with Issues.
- Using @mention is important - you can mention people or teams to give them a notification to see your pull request to start collaboration.


**Notifications**
- Notifications are an important part of GitHub. You can customize these several ways.
  - For GitHub in general, [Settings/notificatons](https://github.com/settings/notifications)
  - For repositories, at the top of a repository page on GitHub.com by clicking "Watch"
  - For individual issues and pull requests by clicking "unsubscribe" on the right hand side of the webpage
- On the pull request page, we talked about the different tabs for 'conversation', 'commits', and 'files changed'.
  - 'Conversation' is where you and your colleagues can collaborate on your changes. This view includes comments as well as notes of when changes happen.
  - 'Commits' shows a history of what commits were added - this is why your commit messages matter - they tell a story.
  - 'Files changed' will let you see the actual code in several different formats. You also can make line level comments from this view.


### Notes from Day 1,  section 3: 
#### Collaborate on GitHub
- Once you've opened a pull request, go into someone elses. Please don't merge someone else's PR. 
- Look at their code, and make a comment about something you see. 


#### Merging Pull Requests
**Pull requests**
- During class, please do not close or merge any pull requests other than your own.
- On your own pull request, if all is green and there are no conflicts, go ahead and merge your branch.
- After merging a branch, it's part of the `master` branch and good practice is to delete it.
  - This is a major difference between Git and some older version control systems. In Git, branch often, merge often, and delete branches often.
- Back at the command line, we need to pull down the changes from GitHub.com in the remote repository.
   - `git checkout master`
   - `git pull`
   - `git branch --merged`
   - `git branch -d <branch-name>`
   - `git fetch --prune`
- Configure your settings to do this by default by typing `git config --global fetch.prune true`

#### View Local Changes
**Local Diffs**
- View local diff diagram [here](https://training.github.com/kit/modules/CONT-CLI-11_Viewing-local-diffs.html)

#### 11. Local History
- Use `git log` to view the history of the repository
- `git log` will show commits from your own local repository, but also changes made by other collaborators 
- Experiment with different option switches to view history:
  - `git log`
  - `git log --oneline`
  - `git log --oneline --graph`
  - `git log --oneline --graph --decorate`
  - `git log --oneline --graph --decorate --all`
  - `git log --stat`
  - `git log --patch`
- Use the up and down arrows or press enter to view additional log entries. Type q to quit viewing the log and return to the command prompt.

#### Streamline Workflow With Aliases
- Set up an alias in configurations: `git config --global alias.<desired-alias> "the long version of the command that you want the alias to run, without git at the beginning, and with the desired flags"`

## Notes from Day 2, section 1:
### Review of workflow
- We are using the same repository as yesterday
- Clone the repository locally on your command line: `git clone https://github.com/githubteacher/fluffy-octo-guacamole.git new-fluffy-repository`
  - _Note: the extra argument at the end creates an alternate name for the repository_
- CD into the new repository: `CD new-fluffy-repository`
- See all of the bios: `ls bios/`
- Create a new branch and checkout to it: `git checkout -b new-unique-branch-name`
- Make changes locally to your own file in your favorite text editor. Save your changes and exit your text editor.
- Commit your changes:
  - `git add <filename>`
  - `git commit -m "enter short descriptive commit message"`


### View Local Changes
**Local Diffs**
- View local diff diagram [here](https://services.github.com/kit/modules/CONT-CLI-11_Viewing-local-diffs.html)
- `git diff`: See local changes between working, staging, and history
- If we have added more changes to a file that we've already created, we can see differences between them with `git diff`
- See differences with `git diff`
 - `git diff`
 - `git diff --staged`
 - `git diff HEAD`
 - To see differences between branches: `git diff <branchname>`
 - `git diff --stat master`

### Local History
- Use `git log` to view the history of the repository
- `git log` will show commits from your own local repository, but also changes made by other collaborators
- Experiment with different option switches to view history:
 - `git log`
 - `git log --oneline`
 - `git log --oneline --graph`
 - `git log --oneline --graph --decorate`
 - `git log --oneline --graph --decorate --all`
 - `git log --stat`
 - `git log --patch`
- Use the up and down arrows or press enter to view additional log entries. Type q to quit viewing the log and return to the command prompt.

### Make more changes
- Make more changes with the steps used before.
- Add and commit those changes.
- Continue to use `git diff` and `git log -5` to see changes throughout the commit process
- See commit differences between branches: `git log <current-branch> ^master`

### Update your local environment 
- In your command line, go back to the master branch: `git checkout master`
- Update your local repository: `git pull`
- Git will delete remote tracking branches that no longer exist: `git fetch --prune`
- See what branches have been merged into the current branch: `git branch --merged`
- Delete the branches locally: `git branch -d <branch-name>`


## Day 2, Section 2 notes: 
### Make local changes
- Create a new branch and checkout to the branch at the same time by typing `git checkout -b username-readme-update`
- Edit the `readme.md` file with your text editor so the link on line 5 reflects your username instead of `githubschool`
- Save those changes, and exit the text editor
- Type `git status` to see your current branch and current stages of each file

### Share changes to GitHub
- Type `git add readme.md` to move your files from working to staging
- Type `git commit -m "update link in readme"` to move files to history
- To push the changes to the remote repository in the correct branch to reflect your local branch, type `git push -u readme-update`.
- See your changes on GitHub.com

### Merge Conflicts
- Open a new pull request
- You will see there is a merge conflict!
- We are going to resolve the conflict on our branch and make sure it works out with a reverse merge. This is when you merge master into your feature branch.
- Locally, checkout to your own branch.
- `git merge --no-ff master`
- `git status`
- Open the README.md again. You'll look for the conflict markers. Delete the copy of the content you don't want to keep as well as the merge conflict markers. Save and close.
- `git add README.md`
- `git status`
- `git commit -m "enter commit message here"`
- `git status`
- `git push`
- Feel free to practice more with merge conflicts later on this repository.


### Reverting Commits
- `git revert` creates a new commit that is the exact opposite of the selected commit. This is important to note when thinking about impact on history!
- Revert a commit by typing `git revert <first-4-of-commit#>`.

### Fixing the broken game
- See the commit history: `git lol`.
- Find the commit where index.html was renamed to inde.html and copy the first 4 characters of that commit ID
- Revert that commit: `git revert <first-4-characters>`.
- Complete the commit message in your text editor, save, and close.
- Push your local changes to the remote repository: `git push mygame`.
- See your working game by going to the new link in the README on your remote repository.

### Patrick showed the differences between fast forward merges, recursive merges, and three way merges
- Overview for conceptual understanding
- To follow along: 
  - `git checkout master`
  - `git log --oneline --decorate -5`
  - `git status`
  - `git merge origin/master`
  - `git log --oneline --decorate -5`
- Pull requests default to fast forward merge if possible, which does not create a commit
- To force a recursive merge and a commit message, use `git merge --no-ff <branchname>`
- Remember, when you delete a branch, you're only really deleting a pointer to a commit.   

## Day 2, Section 3 Notes:

### Helpful Git Commands
- We made a new file, and renamed it with `git mv`
  - Make sure your local repository is up to date: `git pull`
  - Create a new branch and checkout to it: `git checkout -b demo-undoing-things`
  - See the files: `ls`
  - Move a file: git mv hello.txt bios/hello.txt
  - `git status`
  - git commit -m "enter commit message"
- Remove files with `git rm`
  - Delete a file and stage the deletion `git rm jt_bio.md`
  - `git status`
  - `git commit -m "demo deleting files"`
- See the commits that have worked with a given file: `git log -- bios/hello.txt`
- See all of those, including renames: `git log --follow -- bios/hello.txt`

### Undo one commit with Revert
- See all recent history: ` git log --oneline --decorate -5`
- Revert a single commit by using the first four characters of the commit ID: `git revert <first-four-chars>`
- This creates a new commit with a new ID and it does the opposite of everything done in the referenced commit. It is the safest way to undo changes.

### Commit amend
- Make another change to a local file, like your bio.
- Add the changes, and make a commit. 
- Make another change and add it, but do not commit it.
- To change the previous commit to include your most recent changes, type: `git commit -a --amend`
- It is unsafe to use this command after a commit has been pushed to a remote repository, as you are rewriting history.

### Rewriting History With Git Reset
- `git reset` moves the branch pointer along the current branch
- To practice, create a new branch: `git checkout -b <demo-branch-name>`
- Add text to the README with: `echo 'lorem ipsum' >> README.md`
- Commit these changes with `git commit -am"add first dummy line`
- Add more files
  - `echo 'a second line' >> README.md`
  - `git commit -am"a second line"`
  - `echo 'a third line' >> README.md`
  - `git commit -am"a third line"`
- See your recent log history: `git lga-5`
- Reset soft back to one of the earlier commits: `git reset --soft <first 4 of commit ID>`
- See that log: `git lga -5`
- Check our status to see what is staged: `git status`
- `git diff --staged`
- `git commit -m"add additional two lines"`
- `git reset soft` moves head and moves the files back to staging
- The default for `git reset` is `git reset --mixed`.
- Try it with `git reset <first four of commit ID>`
  - Don't forget to use `git lga -5` and `git status` to see how it works
- Now, let's use `git reset --hard <first 4 of commit ID>`
  - Warning: If you `git reset --hard` and there are uncommitted changes, they will be gone forever. :( 
- See how these changes work with `git log --oneline`, `git status`, and `cat README.md`

### Tracking HEAD with Git Reflog
- In case you were worried that `git reset` had done some damage to your commits, you should know about `git reflog`
- `git reflog` shows every place your HEAD has been, including commits and resets. 
- This means you can `git reset` **back** to the commits you just got rid of!
- Warning: The commits in the reflog do not live forever!
  - Reflog information exists only 30-90 days based on your settings.
  - Reflog information is only local - not on the remote repository or any other collaborator's repositories

### Git cherry-pick
- This command, `git cherry-pick` is not part of the every-day workflow
- `git cherry-pick` will bring back specific commits that may have been undone with `git reset`
- It's also used to grab a single commit off of a feature branch and replay it on master.
- Practice by typing `git cherry-pick <commit-ID>` of a commit that has been undone
- It's important to only use `git cherry-pick` with commits that have not been pushed to a remote repository as it changes the commit ID of the same information

### Merge Strategies: Rebase
**About Rebase**
- The `rebase` command enables you to modify your commit history in a variety of ways.
- Because changing your commit history can make things difficult for everyone else using the repository, it’s considered bad practice to rebase commits you’ve already pushed to a repository.


## [Video from Day 1](https://vimeo.com/166273795/bf43c46e11)
## [Video from Day 2](https://vimeo.com/166424261/f7b7d06ecc)
