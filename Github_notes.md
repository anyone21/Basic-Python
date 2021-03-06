
### Basic terminology

* Working tree: The set of nested directories and files that contain the project that's being worked on.

* Repository (repo): The directory, located at the top level of a working tree, where Git keeps all the history and metadata for a project. Repositories are almost always referred to as repos. A bare repository is one that isn't part of a working tree; it's used for sharing or backup. A bare repo is usually a directory with a name that ends in .git—for example, project.git.

* Hash: A number produced by a hash function that represents the contents of a file or another object as a fixed number of digits. Git uses hashes that are 160 bits long. One advantage to using hashes is that Git can tell whether a file has changed by hashing its contents and comparing the result to the previous hash. If the file time-and-date stamp is changed, but the file hash isn’t changed, Git knows the file contents aren’t changed.

* Object: A Git repo contains four types of objects, each uniquely identified by an SHA-1 hash. A blob object contains an ordinary file. A tree object represents a directory; it contains names, hashes, and permissions. A commit object represents a specific version of the working tree. A tag is a name attached to a commit.

* Commit: When used as a verb, commit means to make a commit object. This action takes its name from commits to a database. It means you are committing the changes you have made so that others can eventually see them, too.

* Branch: A branch is a named series of linked commits. The most recent commit on a branch is called the head. The default branch, which is created when you initialize a repository, is commonly named master. The head of the current branch is named HEAD. Branches are an incredibly useful feature of Git because they allow developers to work independently (or together) in branches and later merge their changes into the default branch.

* Remote: A remote is a named reference to another Git repository. When you create a repo, Git creates a remote named origin that is the default remote for push and pull operations.

* Commands, subcommands, and options: Git operations are performed by using commands like git push and git pull. git is the command, and push or pull is the subcommand. The subcommand specifies the operation you want Git to perform. Commands frequently are accompanied by options, which use hyphens (-) or double hyphens (--). For example, git reset --hard.

* Forking : A fork is a copy of a repository. Forking a repository allows to freely experiment with changes without affecting the original project. You can refer more about it on [Link](https://www.toolsqa.com/git/git-fork/) 

Now we are familiar with basic terms and we continue with setting up GIT.

## STEP-1 [CONFIGURE GIT]

| COMMANDS |
|----------|
| git --version |
| git config --global  user.name "<USER_NAME>" |
| git config --global user.email "<USER_EMAIL>" |
| git config --list |

* git --version : This command is used to check the installed version of git.

* Two global variables: ***user.name*** and ***user.email*** are required to make commits.

* git config --list : With this command we can see all variables provided by git.

## STEP-2 [SETUP A NEW GIT REPOSITORY]

| COMMANDS |
|----------|
| git init --inital-branch="branch-name" |
| git init -b "branch-name" |
| git --help |

* git init --inital-branch=main : This initialize our new repository ans set the name of the default branch to main.

* git --help : To get help with what we can do with git.

## STEP-3 [BASIC GIT COMMANDS]

| COMMAND | Description |
|---------|-------------|
| git status | displays the state of the working tree (and of the staging area—we'll talk more about the staging area soon). It lets you see which changes are currently being tracked by Git, so you can decide whether you want to ask Git to take another snapshot.|
| git add | It is the command you use to tell Git to start keeping track of changes in certain files. The technical term is staging these changes. We'll use git add to stage changes to prepare for a commit. All changes in files that have been added but not yet committed are stored in the staging area. |
| git commit | After changes added to staging area they are redy to commit |
| git log | This command allows us to see information about previous commits. |

To look at the previous changes made we use ***git log***. Output of ***git log*** looks like

![image](https://user-images.githubusercontent.com/32765126/125146627-5c730680-e144-11eb-855d-59018dc21c16.png)

git log have plenty of options to choose from like
1. git log --oneline  : output of same log as above but with more concise listing.

![image](https://user-images.githubusercontent.com/32765126/125146666-99d79400-e144-11eb-9cbb-e59f375724a5.png)

2. git log -nX : where X can be 1,2,3 ... which is a commit number: 1 for the latest commit, 2 for the one before that, ad so on.

![image](https://user-images.githubusercontent.com/32765126/125146724-05b9fc80-e145-11eb-9ddb-56e6ba1188db.png)





