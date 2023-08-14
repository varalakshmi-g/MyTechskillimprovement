Hello all,

Let's learn git one of the most demanding skill in today's IT world.

What are we going too learn in this course :

- What is version control system ? why we need them and what are different types of VCS ?
- How to Install git ?
- Git Key concepts 
   - init
   - GIT Repository Structure
   - Git Object Model 
   - GIT Working Tree
   - GIT Clone
   - GIT BRANCH
   - GIT CHECKOUT
   - Staging Area
   - ADD
   - commit
   - push 
   - pull
   - stash 
   - tags
   - 
## Version Control System

version controlling system is a system which involves in the process of tracking modifications of a previous versions of present code.
- Version Control system is also known as source control system, is a system that helps you to manage changes to a file or a set of files over time.
- It allows you to keep track of all the changes made to a file
or set of files, as well as who made the changes, when the
changes were made, and why the changes were made.
Version control is commonly used in software development,
but it can also be used for other types of files, such as
documents, spreadsheets, and images.

#### Why use Version control system 
- **Keep Track of changes :** Version control allows you to keep track of changes made to a file or a set of files over time. You can see
who made what changes, when the changes were made, and why the changes were made. This can be particularly helpful when
trying to troubleshoot or debug an issue.
- **Collaboration :**: Version control enables multiple people to work on the same files at the same time without overwriting each other's
changes. This can be particularly helpful when working on a project with a team of people.
- **Versioning :** With version control, every change is saved, so you can go back to previous versions if needed. This can be particularly
helpful when you need to revert to an earlier version of a file, or when you need to see how a file has changed over time.
- **Branching and Merging :** Version control allows you to work on multiple versions of a file simultaneously and merge changes
together. This can be particularly helpful when you want to experiment with a new feature or fix a bug without affecting the main
codebase.
- **Backup :** : Version control systems provide a form of backup for your files, as they are stored in a central repository. This can be
particularly helpful in case of hardware failure or other catastrophic events.

version controlling systems are basically divided into 2 types. They are 1. centralised version conrol system 2. Distributed version control system.

|centralised version control system| Distributed version control system|
|------------------|------------------------------|
|It is a single repository| It is a multirepository |
|Internet connection always needed | No need of internet connection |
|Made conflicts between the developers | Don't made the conflicts between the developers. Since, each developer has their own repository |
|It is having a high risk of losing data | It has a less risk of losing data |

How to Install GIT ?
- Go to `https://git-scm.com` and choose installation method as per your OS.

EX: To install in Linux/Debian/Ubuntu based system use `sudo apt install git-all`

- Git is distributed version control system. Which means everybody has their own self contained repository.


**Difference between git and github**

|GIT | GITHUB |
|------|------|
|It was started in 2005 | It was started in 2008 |
|It is a software & CLI| It is a website, GUI & Service|
|It was developed by linux foundation | It was developed by Microsoft |
|It is user independent | It is user dependent |
|It is installed locally on the system | It is hosted in the web |
|It can manage source code history | It is a hosting service for git repo |
|It is focussed on the code sharing & version controlling | It is focussed on the centralised source code hosting |


**Init**

git init is a command in the Git version control system that is used to create a new Git repository. When you run git init in a
directory, it creates a new Git repository in that directory, which enables version control of your files.
Here's how you can use git init:
1. Open your terminal or command prompt.
2. Navigate to the directory where you want to create your new Git repository.
3. Run the command git init.
4. Git will create a new directory called .git in your current directory. This directory contains all the files and folders needed to
manage your repository.
5. You can now start adding files to your repository and using Git commands to manage them.

It's important to note that git init only needs to be run once in a directory to create a Git repository. If you run it again in the
same directory, it will overwrite the existing Git repository, which could result in data loss.

Running `git init` command creates `.git` folder

Git repository exists entirely in a single ".git" directory

### GIT Repository Structure

![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/af0fe859-7ec0-4f3f-9e58-63c98bdd2e31)

>> git log --oneline --decorate --graph --all  --> To visualize the logs in graph format.


 A Git repository is a version control system that stores all the files and information related to a project. It contains all the files that
make up a project, as well as the metadata that tracks changes to those files over time.
The structure of a Git repository is divided into two main areas: the working directory and the Git directory

**1. Working directory:** The working directory is the place where you create, edit, and modify your files. It is the directory that you are
currently working in, and it contains all the files that you are currently working on. You can think of the working directory as your
local copy of the repository.
**2. Git directory:** The Git directory is the place where Git stores all the metadata and version control information for the project. It is
located inside the working directory and is hidden from view by default. The Git directory contains all the information necessary
to manage the repository, including the commit history, branches, and tags.

The Git directory contains several important files and directories, including :

**HEAD:** This file points to the current branch that you are working on.
**Objects:** This directory contains all the objects that Git uses to store the content of your files, including blobs (file contents) and
trees (directory structures).
**refs:** This directory contains all the references to branches, tags, and other Git objects.
config: This file contains configuration information for the repository.
<br>which are points to a single object(usually a commit or a tag object

**References/refs:**
- A reference is a file stored in somewhere else ./git/ref containing hash of commit object.

`$ ls -l .git/refs/heads` 

`$ cat .git/refs/heads/master`

`$ git show --oneline master`

`$ git rev-parse master`

**hooks:** This directory contains scripts that Git can run before or after certain actions, such as committing or pushing changes

Overall, the Git repository structure is designed to allow for efficient version control and collaboration on projects, while keeping
track of all the changes made to files over time.

### GIT Object Model :
Git is a distributed version control system that stores the content of a project as a set of snapshots or commits. The Git object model is the way Git internally represents and stores the content and history of a project.
- GIT object Model consists of four types of objects .
- 
1. **BLOB :**
- BLOB stands for binary large object.
- It is a binary representation of a file. This is the object type which is used to store the contents of each file in a directory.These are most basic datatypes in git.

2. **Tree objects :**
- These are bit like directories. Tree objects can contain pointers to blobs and any other tree objects.
- It represents the hierarchy of files and directories in a project.
- - root tree object is essentially a snapshot of your repository at a given time. When git refers to the tree it means it is root tree object.

3. **Commit objects :**
- A commit is an object that represents a particular version of a project.
- These points to a single tree object. And contain some meta data including the commit author and any parent commits.
- - Even if we give partial hash, it gives us complete hash value because it's unique.

4. **Tag objects :**
- A tag is a lightweight object that points to a particular commit. Tags are often used to mark releases or other important points in a project's history
- which points to a single commit object and contain some meta data.

Git uses a content-addressable storage system, which means that each object is identified by a unique SHA-1 hash of its contents.
This allows Git to easily verify the integrity of objects and detect any changes.
The Git object model is key to understanding how Git tracks changes in a project and allows users to navigate the history of a
project


**Git Working Tree**

The Working Tree in Git refers to the current version of a repository that a user is working on. It is the place where developers make
changes to the files in the project and test their code before committing their changes to the repository.
- When you clone or checkout a Git repository, the entire project is downloaded onto your local machine, creating a local copy of the
repository in your file system. The files and directories in the repository are stored in the .git directory, and when you make changes
to any of the files in your working directory, Git will track those changes and allow you to commit them to the repository.


The working process of git as follows : 
working area ---> staging area --> local repository ---> remote repository.


- we can initiate a empty git repository anywhere by using `$ git init` command

- The important directories are ./objects where we store all objects and ./refs where we store all references

**Clone**
- git clone is a command used in Git, to create a copy of a repository. When you clone a repository, you create a copy of the
entire project, including all its files and the full revision history on your local machine. This allows you to work on the project
locally, make changes, and then push those changes back to the original repository

Example: git clone <repository URL>
- By default, git clone will create a local copy of the entire repository. However, you can also specify a particular branch or tag
to clone using the -b or --branch option, or clone only a specific directory or subdirectory of the repository using the --depth
option.

**Branches :**
 - git branch is a Git command used to list, create, or delete branches in a Git repository.
In Git, branches are pointers to a specific commit in the repository's history. Each branch represents a line of development,
allowing developers to work on multiple features or bug fixes simultaneously and independently.
- By default, when you create a Git repository, it has one branch called "master"/ "Main" which points to the latest commit in
the repository's history. However, you can create multiple branches using the git branch command to work on different
features or experiment with new ideas without affecting the main codebase.
- git branches is a strong feature. It is lightweight. It is entire clone of the repository.
`$ cat .git/HEAD`
 
`$ git branch </branch-name>`

`$ cat .git/refs/heads/</branch-name>`

`$ cat .git/HEAD`

`$ git checkout </branch-name>`

`$ cat .git/HEAD`

- When run with no arguments, git branch will display a list of all the local
branches in the repository, indicating which branch is currently checked
out with an asterisk (*).

Some common usage examples of git branch are:

git branch: List all local branches

git branch new-branch: Create a new branch called "new-branch"

git branch -d branch-to-delete: Delete the local branch called "branchto-delete"

git branch -m old-branch new-branch: Rename the branch "old-branch"
to "new-branch"

git branch -a: List all local and remote branches

git branch -v: List all local branches along with the commit message and
hash of their most recent commit.

**Commonly used Git branches are:**
Master Branch: The primary branch of the repository which represents the main codebase.

Feature Branch: A branch created to implement a new feature or work on a specific task. It is
typically created off the master branch, and once the feature is complete, it is merged back into the
master branch.

Release Branch: A branch created when a new release is ready. It is typically created from the
master branch and contains only stable and tested code.

Hotfix Branch: A branch created to fix critical issues in the codebase. It is created off the release
branch and once the fix is complete, it is merged back into both the master and release branches.

Development Branch: A branch used for ongoing development work, separate from the master
branch. Changes made on this branch are merged into the master branch once they are stable and
tested.

### Git Checkout

git checkout is a command in the Git version control system that is used to switch between different
branches, create a new branch, or checkout a specific commit or file.

Here are some common uses of git checkout :

1. **Switching branches :** : To switch to an existing branch, use git checkout <branch-name>. This will move
your working directory to the latest commit on that branch.

2. **creating a new branch :** To create a new branch and switch to it, use git checkout -b <new-branchname>. This will create a new branch off the current branch and switch to the new branch.
3. **checking out a specific commit**: : To check out a specific commit, use git checkout <commit-hash>. This
will move your working directory to the state of the repository at the specified commit.
4. **Checking out a specific file**: To check out a specific file from a branch or commit, use git checkout
<branch-name/commit-hash> <file-path>. This will replace the contents of the file in your working
directory with the contents of the file in the specified branch or commit.

It's important to note that git checkout can modify the state of your working directory and potentially
overwrite changes that you have made. Therefore, it's important to use it with caution and make sure you
understand what you are doing.

 **staging area **
 - In Git, the staging area (also known as the "index" or "cache") is a concept that refers to the intermediate step between
modifying files and committing those changes to the Git repository.

 - When you make changes to files in your Git repository, those changes are initially only tracked in your local working directory.
In order to commit those changes to the Git repository, you first need to add them to the staging area.
 - The staging area is essentially a snapshot of your working directory at a particular point in time. You can use the "git add"
command to add modified files to the staging area. Once a file is in the staging area, you can review the changes and make
any necessary modifications before actually committing the changes to the repository using the "git commit" command.
 
 - Using the staging area can be helpful in a number of ways. For example, it allows you to review and selectively add changes
before committing them, which can help prevent mistakes and ensure that you only commit changes that are ready to be
shared with others.
- Additionally, using the staging area can help you organize and structure your commits more effectively, which can make it
easier to track changes over time and collaborate with others.
 
 add :
 
 - In Git, the "git add" command is used to add changes to the staging area, which is an intermediate step in the process of
committing changes to the Git repository.
- When you make changes to files in your working directory, Git initially tracks those changes but does not automatically add them
to the staging area. To add changes to the staging area, you can use the "git add" command followed by the name of the file(s)
you want to add. 
 For example:
`git add myfile.txt`
 
- This command adds the changes made to "myfile.txt" to the staging area, where they can be reviewed and modified before being
committed to the Git repository using the "git commit" command.
- You can also use the "git add" command with wildcards or patterns to add multiple files at once. 
 
 For example:
`git add *.txt`
 
- The "git add" command can also be used to stage file deletions or moves. For example:
`git add --all`
- This command adds all changes, including file deletions and moves, to the staging area. Alternatively, you can use the "git rm"
command to remove files from both the working directory and the Git repository
 
commit :
 
 - A git commit is a command used in the Git version control system to save changes to a local repository. When you make changes
to files within a Git repository, you can stage those changes using the git add command, which adds the changes to the staging
area. Once you have staged all the changes you want to include in the commit, you can use the - - git commit command to create a
new commit.
The git commit command allows you to provide a commit message, which should briefly describe the changes you are committing.
- It's important to write clear and descriptive commit messages, as they help others understand what changes you have made and
why.
- A typical git commit command looks like this:
git commit -m "Add new feature to web app"
- This command creates a new commit with the commit message "Add new feature to website". The -m option is used to specify
the commit message inline with the command.
 
 push
- git push is a command used in the Git version control system to upload local repository changes to a remote repository. This
command is used after making changes to the files in your local repository and committing those changes using the git commit
command.
- The basic syntax for the git push command is as follows:
`git push <remote> <branch>`

 Here, <remote> refers to the name of the remote repository you want to push your changes to, and <branch> refers to the name of
the branch you want to push to the remote repository.
For example, to push changes from the local master branch to the origin remote repository, you would use the following command:
`git push origin master`
- This command would upload all the changes you have made in your local master branch to the master branch in the origin remote
repository.
- It is important to note that you may encounter errors when pushing changes if there are conflicts between the changes made in
your local repository and the changes made in the remote repository. In such cases, you may need to resolve the conflicts before
pushing your changes.
 
 Pull :
 - git pull is a Git command used to fetch and merge changes from a remote repository into your local repository.
When you run git pull, Git performs two operations:
 <br>1.**git fetch**: : This command downloads the latest changes from the remote repository and stores them in a local branch named
"origin/branch-name" (where "branch-name" is the name of the remote branch you're tracking).
  <br> 2. **git merge**: This command merges the changes downloaded from the remote repository into your current branch. If there are
any conflicts between your local changes and the changes from the remote repository, Git will prompt you to resolve those
conflicts before completing the merge.

 Here's an example of how to use git pull to update your local repository with the latest changes from the remote repository:<br>
1. Navigate to the local repository directory using the command line
2. Run the following command to fetch the latest changes from the remote repository
`git fetch`
3.Run the following command to merge the changes into your current branch:
`git merge origin/branch-name`
Replace "branch-name" with the name of the remote branch you want to merge.
- Alternatively, you can use the git pull command with the --rebase option to fetch and rebase the changes from the remote
repository instead of merging them. This option can be useful for keeping a linear commit history. For example:
`git pull --rebase`
This will fetch the latest changes from the remote repository and rebase your changes on top of them. If there are any conflicts, Git
will prompt you to resolve them before continuing with the rebase.
 
 Stash :
 
 - git stash is a command in Git that allows you to temporarily save changes you've made to a working directory and revert it back to
the last commit. This is useful when you need to switch to a different branch or work on a different task, but don't want to commit
the changes you've made so far.
When you run git stash, Git takes all of the changes in your working directory that are not yet committed and stores them in a
"stash." You can then switch to a different branch or task and continue working. When you're ready to go back to the changes you
stashed, you can run git stash apply to apply the stash back to your working directory.
Here are some common git stash commands:
 
 - **git stash** : this command stashes all the changes you've made to the working directory.
 - **git stash save "stash message"**: This command allows you to provide a message describing the changes you've stashed.
 - **git stash list**: This command shows a list of all the stashes you've created.
 - **git stash apply**: This command applies the most recent stash to your working directory.
 - **git stash apply stash@{2}: This command applies a specific stash to your working directory.
 - **git stash drop**: This command deletes the most recent stash.
 - **git stash pop**: This command applies the most recent stash and then deletes it
 
 It's important to note that git stash does not create a commit. so, it's not a replacement t for committing changes. Instead, it's a tool
for temporarily saving changes when you need to switch contexts or work on a different task
 
**Tags:**
 - Git tags are markers that are used to create a named reference to a specific commit in a Git repository. They can be used to label
specific points in a repository's history, such as release versions or important milestones.
There are two types of Git tags: lightweight tags and annotated tags.

 A lightweight tag is simply a pointer to a specific commit. It is created by running the following command:
`git tag <tag-name> <commit>`
 
An annotated tag, on the other hand, is a full object in Git, which includes a tagger name, email, and date, along with a
message. It is created by running the following command:
`git tag -a <tag-name> <commit> -m "tag message"`

 Annotated tags are often used to mark release versions, while lightweight tags can be used for other purposes.

 Once a tag is created, it can be pushed to a remote repository using the following command:
`git push origin <tag-name>`

 To list all of the tags in a repository, you can use the following command:
`git tag`

 You can also view information about a specific tag by running the following command:
`git show <tag-name>`

 Overall, Git tags are a useful feature for organizing and marking important points in a repository's history.
 
- There are 2 types of tags in git they are 1. annotated tags and 2. lightweight tag
`$ git checkout master`
`$ git tag 1.0-lightweight`
`$ cat .git/refs/tags/1.0-lightweight`
`$ git cat-file -p 1.0-lightweight`

- lightweight tag and commit are the same object. light weight tag is only reference to the commit object
- let's create annotated tag
`$ git tag -a -m "taged 1.0" 1.0`
we have passed -a(annotated) to git tag to create annotated tag, It is also created a reference tag just like lightweight tag but reference is not pointing to same object as the lightweight tag.
`$ git cat-file` to inspect the object

Tag objects can also be signed with GPG keys to prevent commit or email spoofing.
`$ cat .git/refs/tags/1.0`
`$ git cat-file -p 1.0`

Reasons why we prefer annotated tag rather than lightweight tag :
> GpG keys
> Owner authorization
> These are timestamped, Apart from telling when the last commit was made. It also tells us about the last version release date.

**Merging :**
- Merging in git is the process of joining two histories(branches)together.
- let's say you have created new feature branch from master, and done some work on it.
`$ git checkout -b </branch-name>`
`$ git commit -am "finished the new feature"`
`$ git checkout master`
At the same time, you need to fix an urgent bug . so you created a hotfix branch from master and do some work in there.
Now you want to bring the bug fix into master. so that you can tag it and release it.

`$ git checkout -b hotfix`
`$ git commit -am "fixed some wording"`

- Notice how git mentions **fast-forwarding** during the merge. what this means is that all of the commits in hotfix were directly upstream from master. This allows git to simply move the master pointer up the tree to hotfix.

let's try and merge feature-branch into master.
`$ git branch hotfix`
`$ git merge hotfix`
`$ git merge feature-branch`
`$ git log --oneline`
`$ git show --format=raw </commit-id>`

- This time, Git wasn't able to perform a fast-forwarding. This is because feature-branch isn't directly upstream from master. This is clear on the above above, where master is at commit **D** which is in  a different history tree to feature-branch at commit **C**
so, how did git handle this merge ? Taking a look at the log, we see that git has actually created a new "merge" commit, as well as bringing the commit from feature-branch.

upon closer inspection, we can see that this is a special kind of commit object- It has **two parent commits** this is refered to as **merge commit**

**cherry-picking :**

![image](https://user-images.githubusercontent.com/89054489/218244876-691578c1-e3c1-438d-becd-38bfe4192cd3.png)

- if you are on commit **D** and you run git cherry-pick **F**, Git will take that changes that are introduced in commit **F** and replay them as new commit(shown as 'F`') on top of commit **D**
 ![image](https://user-images.githubusercontent.com/89054489/218245440-2e306048-0a61-4caf-81e1-56467b952111.png)

- The reason why we end up with a copy of commit **F** rather than commit **F** itself is due to the way commits are constructed. Recall the parent commit is part of a commit's hash.so, despite containing the same changes, author information and timestamp. **F`** will have a different parent to **F**, giving it a different hash.

- A common workflow in git is to develop feature on small branches and merge the features one at a time into the masters branch.
![image](https://user-images.githubusercontent.com/89054489/218246806-08a20b41-183a-4dbc-b734-e83a8f80e77f.png)

- As you can see, master has been updated since, "foo" was created. To avoid potential conflicts when "foo" is merged with "master", we want to bring master's changes into "foo". Because master is the base branch, we want to play foo's commits on top of master. Essentially, we want to change commit **C's** parent from **B**to**F**
it's not going to be easy. But, we can achieve this with git cherry-pick.First, we need to create a temporary branch at commit F

`$ git checkout master`
`$ git checkout -b foo-tmp`
Now that we have a base on commit **F**, we can cherry-pick all of foo's commits on top of it.
`$ git cherry-pick C D`

- Now all that's left to do is point "foo" at commit **D`**  and delete temporary branch "foo-temp". We do this with the reset command, which points HEAD(and therefore the current branch) at a specified commit. The --hard flag ensures our working tree is updated as well.

   why do we need reset ?
   - Remove error commits before push
   - combine commits before push
   - Refine history graph before push
   
   3 types of reset
      - Soft reset (1)
      - Mixed reset (1+2)(default0
      - Hard reset (1+2+3)
   
`$ git checkout foo`
`$ git reset --hard foo-temp`
`$ git branch -D foo-temp`

- This gives the desired result of foo's commits being upstream of master. Note that the original **C**and**D** commits are no longer reachable because no branch points to them.

![image](https://user-images.githubusercontent.com/89054489/218247808-426a42ec-8015-41da-a191-d39ddba359d3.png)


![image](https://user-images.githubusercontent.com/89054489/218248215-e83029c0-635e-4fa9-b447-ac4c09af505f.png)

**Rebasing :**
`$ git rebase <base> <target>`
- with the format git rebase <base> </target> , the rebase command will take all of the commits from <target> and play them on top of <base> one by one. It does this without actually modifying <base> , so the end result is a linear history in which <base> can be fast-forwarded to <target>
- In a sense, performing a rebase is like telling git **"Hey, i want to pretend that <target> was actually branched from <base> Take all of the commits from <target>, and pretend that they happened after <base>"**.

- All we have to do to enable fast-forward merge of feature-branch into master is run git rebase master feature branch before performing the merge. This has brought feature-branch directly upstream of master.

![image](https://user-images.githubusercontent.com/89054489/218262135-7530d9e1-ec21-47b5-aee0-5bc4b3d5f0f0.png)

- **Rebase flatterns the history, removing unwanted entries**. Git merge on the other hand, only changes the target branch and creates a commit, preserving the history of the source branch.
-**cherry picking in git means to choose a particular commit from one branch and apply it onto another branch**. In contrast merge or rebase apply normally many commits onto another branch.

**Remotes :**

- It is therefore possible to have a repository which can store your project's history without actually having a working tree. this is called **bare repository**.Bare repositories are most commonly used as a "central" repository where collaborators can share changes. the mechanism for sharing these changes will be explained in detail in the **pushing**and**pulling**sections. For now, let's look at creating a bare repository.

`$ git init --bare`
- Notice here instead of creating a .git folder, the above command simply treats the current directory as .git directory.

- Notice how rather than creating a .git directory for the repository. git init --bare simply treats the current directory as the .git repository.
There's really not much to this repository. The only interesting things it contains are HEAD reference. which points to the master branch(which doesn't exist yet) and a config file which has the bare flag set to true. The other files aren't of much interest of us.

`$ cat HEAD`
`$ cat config`
`$ find. -type f`

**Cloning :**
- the git clone is really just a shortcut which does a few things for you. with its default configuration, it will:<br>
1. create remote-tracking branches for each branch in the remote.<br>
2. checkout the branch which currently active(HEAD) on the remote.<br>
3. perform a git pull to bring the current branch and working tree up-to-date with the remote.

the clone command takes a url and supports a number of transport protocols including HTTP, SSH, and Git's own protocol. It also supports plain old file paths, which is what we'll use.

`$ cd ..`
`$ git clone bare-repo/clone-of-bare-repo`
let's inspect this cloned repository to see how git has set it up.

`$ cd clone-of-bare-repository`
`$ find. -type f`
`$ cat .git/HEAD`
`$ ls -l .git/refs/heads`
`$ cat .git/config`

- This is quite literally a clone of bare-repo the only difference is that this repository contains a few extra lines in .git/config
<br>First, it contains a remote listing for "origin"  which is the default name given to a repository's main remote. This tells git the URL of the repository and which reference it should retrieve when performing a **git-fetch**.

**pushing :**
- we just now cloned a completely empty repository, and we want to start working on it.
`$ echo 'project v1.0'>README`
`$ git add README`
`$ git commit -m "Add readme"`
- Now that we've completed some work, we need to share this with our collaborators who have also cloned this repository. Git makes this really easy.

`$ git push origin master`
- As expected, the remote repository now contains a master branch which points to the commit that we just created.
- Essentially, what happened when we ran git push, is GIT updated the remote's references, and sent it any objects required to build those references. In this case, git push updated the remote's master to a point at <commit-id> and sent it to <commit-id> commit object as well as any tree and blob objects related to that commit.

`$ remote-tracking branches`
- As we saw in cloning, a remote-tracking branch is essentially just a few lines in .git/config.
**[branch "master"]<br>
        remote = "origin"<br>
        merge = refs/heads/master

The line [branch "master"] denotes that the following configuration applies to the local **master** branch.
The rest of the configuration specifies that when this remote-tracking branch is fetched. Git should fetch the **master** branch from the **origin** remote.
Besides storing this configuration, git also stores a local copy of the remote branch.This is simply stored as a reference in .git/refs/remotes/<remote>/<branch>

**fetching :**
- **git fech** command is fairly simple. It takes the name of a remote (unless used with -all flag, which fetches all remotes) and retrieves any new references and all objects necessary to complete them.
- This fetch parameters here specifies a mapping of <remote-refs>:<local-refs>
<br>
The example above simply states that the references found in origin's refs/heads/* should be stored locally in /refs/remote/origin/*

`$ git fetch origin`
This has done a couple of things. First, it has created a reference for the remote branch in .git/refs/remote/origin
`$ cat .git/refs/remotes/origin/feature-branch`
it has updated a specific file .git/FETCH_HEAD with some important information.

- But, what if we do want a local branch which tracks the remote feature-branch ? Git makes this easy. if we run git checkout feature-branch rather than failing because no local feature branch exists, git will see that there is a remote feature-branch available and create a local branch for us.
`$ git checkout feature-branch`
branch feature-branch set up to track remote branch feature-branch from origin.

git has done couple of things for us here. first, it has created a local feature-branch reference which points to the same commit as the remote feature-branch.

`$ cat .git/refs/remotes/origin/feature-branch`
It has also created a remote-tracking branch entry in .git/config
`$ cat .git/config`

**pulling :**
- the git pull command is, like git clone, a nice shortcut which essentially just runs a few lower-level commands. In short, with the format `$ git pull<remote> <branch>, the git pull command does the following :<br>
1. Runs git fetch <remote>
2. Reads .git/FETCH_HEAD to figureout if <branch> has a remote-tracking branch which should be merged.
3. Runs git merge if required, otherwise quits with an appropriate message.

At this point, it helps to understand git's FETCH_HEAD. Everytime you run git fetch, git stores information about the fetched branches in .git/FETCH_HEAD. This is refered as short-lived reference, because by default git will override the contents of FETCH_HEAD everytime you run git fetch.

**Toolkit :**
 **git-reflog**:
- git records information about the changes in so called "reflog"
- git log is no help, since the commits are no longer reachable from HEAD.
In these cases, we use reflog
`$ git reflog`
- the reflog shows a list of all changes to HEAD in reverse chronological order.
- the hash in the first column is the value of HEAD after the action on the right was performed.

- if we want to recover commits we follow different methods depends upon situation. In this particular example, we can simply do `$ git reset --hard <commit-id>` to restore HEAD to its original position.However, if we have introduced new commits since, the destructive change, we may need to do something like **cherry-pick** all the commits that are lost.

**note:** git's reflog is only a record of chages for your repository. if your local repository becomes corrupt or deleted. the reflog won't be of any use(if the repository is deleted the reflog won't exist at all)
- depends upon the situation, you may find **git fsck** more suitable for recovering lost commits.
- git's object storage works like a primitive file system--objects are like files on harddrive and hashes are object's physical address on the disk. the git index is exactly like the index of a file system in that it contains references which point at an object's physical location.
- In `$ git fsck` fsck(file system check) this tool is able to check git's database and verify the validity and reachability of every object that it finds.
- when a reference(like branch) is deleted from git's index. the object(s) they refer to usually aren't deleted. even if they are no longer reachable by any other references. if we delete **feature-branch(ex)** the commit will no longer be reachable.<br>
At this point, commit<commitid> still exist in our repository. but there are no references pointing to it. By searching through the database, git fsck is able to find it.
`$ git fsck --lost found`
- An example of this is when you delete a remote branch through interfaces like github. Assuming the object haven't been garbage-collected, you can clone the remote repository and use git fsck to recover the deleted branch.
**git stash:**
- it takes all changes to your working tree and index and "stashes" them away, giving you a clean working tree. you can then retrieve those changes from your stash and reapply them to the working tree at anytime with `$ git stash apply`
- A common usecase of git stash command is to save some half finished changes inorder to checkout another branch.
- stashes in git are put onto a stack. with the most recently stashed on top. you can list all current stashes with `$ git stash list`
-**stash commit is a merge commit**
- to find path of git merge commit , we use `$ git show-ref`
#### why does git creates a merge commit for stash ?
- Recording the stat of working tree, and record the state of index(also known as "staging area")
- since, its possible for the index and the working tree to contain changes to a same file. Git needs to store the states repeatedly.
This gives us a history that looks a little like this :

![image](https://user-images.githubusercontent.com/89054489/218262227-765b9b2c-6700-4c9a-9e6c-005c9c729082.png)

- In this history graph, the tree of commit C contains the changes to the working tree. commit C's first parent is the commit that HEAD pointed to when the stash was created (commit A). The second parent (commit B) contains the changes to the index. It is with these two commits that Git is able to re-apply your stashed changes.

**git describe:**
- git describe show the most recent tag that is reachable from a commit.
- git describe will take any reference or commit hash, and return the name of the most recent tag.if the tag points at the commit you gave it.
- git describe will return only the tag name. otherwise, it will suffix the tag name with some information including the number of commits since the tag and an abbreviation of the commit hash.
`$ git describe <commit-id>`
- if you want to ensure that only the tag name is returned. you can force git to remove the suffix by parsing --abbrev=0
`$ git describe --abbrev=0 </commitid>`
**git rev-parse**
- it is an ancillary plumbing command which takes a wide range of inputs and returns one or more commit hashes. The most common use case is figuring out which commit a tag or branch point to.
`$ git rev-parse --short v1.2.15`
**git bisect :**
- git bisect is an indispensible tool when you need to figure out which commit introduced a breaking change. the **bisect** command does a binary serach through your commit history to help you find the breaking change as quickly as possible.
To get simply started, simply run `$ git bisect start `
To tell git that commit your'e currently on is broken `$ git bisect bad`
then give git a commit that you know is working with `$ git bisect good <commit>`
once bisect is finished( or when you want to abort it) be sure to run git bisect reset HEAD to where it was before the bisect.

find which commit a reference points at `$ git rev-parse HEAD` `$ git rev-parse --short HEAD`
find which branches a commit is in `$ git branch --contains HEAD`
find commits that are in one branch but not another `$ git log --oneline --right-only master..hotfixed-1`
exclude commits that are cherry-picked `$ git log --oneline--cherry-pick --right-only master..hotfixed-1`
To view details of an object `$ git cat-file -p HEAD`
To shown an object's type `$ git cat-file -t HEAD`
to show an object's size `$ git cat-file -s HEAD`
print the tree of a given reference `$ git ls-tree-t-r HEAD`
find  the first tag that contains the reference `$ git describe HEAD`




`git config --global user.name "Nagacharan g"`   To provide global user name
`$ git config --global user.email "nagacharan4286@gmail.com"` To provide global user email id
`$ git config --global user.name` To check the name of the user
`$ git config --global user.email` To check the name of the email id
`$ git config --list`      To check all the list of configurations
`$ git config --global --list` To check only the global configurations.
`$ git config --global --edit` To edit the global configuration settings.

`$ git init`    To create a new empty local repository.

`$ git status`  To check the status of untracked files



