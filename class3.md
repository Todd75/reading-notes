# Course 102 Class 3 "Revisions and the Cloud" Reading Notes

## *Class Three*

**Version Control:**
Version Control is a system that allows you to revisit various versions of a file or set of files by recording changes. Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. By utilizing a Version Control System (VCS), mistakes with files can easily be rectified.

**Local Version Control:**
Many years ago, programmers created Local Version Control systems. A Local VCS entails one database on your hard disk that stores changes to files.

**Centralized Version Control:**
The need for collaboration within a developer team on a single file or set of files led to the advent of the Centralized Version Control System (CVCS). This system entails a single server storing all changes and file versions, which can be accessed by various clients. This streamlined the collaboration process (by eliminating the need to involve all local databases), allowed programmers to have more knowledge of team members’ activities with certain files, and gave administrators much more control over divvying up revision privileges.

**Distributed Version Control:**
A Distributed Version Control systems (DVCS) addresses the major vulnerability of the CVS: the server as a single point of failure. If a CVS goes down, collaborators cannot work with each other on a file or save changes and new versions. Also, in the event of corruption of a central database’s hard disk — with the absence of backups — all work will be lost, except for any portions on local machines.

To prevent this type of catastrophic loss, a DVCS allows clients to create mirrored repositories. These data backups can be easily be placed on the server to replace any lost information.

Because the DVCS allows for multiple mirrored repositories, programmers working in teams can collaborate with each other in various ways to complete a joint project, which enables the use of various simultaneous workflows.

**GIT:**

**Snapshots:**

Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.

**Local Operations:**

Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.

**Tracking Changes:**

Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.

**Loss of Data:**

Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

**States:**

Files in Git can reside in three main states: committed, modified and staged.

- **Committed:**
Data is securely stored in a local database

- **Modified:**
File has been changed but not committed to the database

- **Staged:**
Flagged a file’s changed version to be committed in the next snapshot

**Setting up a Git Repository:**

**Importing:**
To import an existing project or directory into Git, follow these steps using the Terminal or Command Line:

Switch to the target project’s directory
Example:

$ cd test cd = change directory
Use the git init command
$ git init

Note: At this stage, you have created a new subdirectory named .git that has the repository files. Tracking has not commenced.

To start tracking these repository files, perform an initial commit by typing the following:

- $ git add *.c
- $ git add LICENSE
- $ git commit -m “any message here”

Now, your files are tracked and there’s an initial commit. We will discuss the particular commands in detail soon.

**Cloning:**
You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:

$ git clone `https://github.com/test`

By cloning the file, you have copied all versions of all files for a project. This command leads to the creation of a directory called “test,” with an initialized .git directory inside it, which has copies of all versions of all files for the specified project. The command also automatically checks out — or retrieves for editing — a copy of the newest version of the project.

To clone a repository into a directory with another name of your choosing, use the following command format:

$ git clone `https://github.com/test` mydirectory

*The local Git repository has three components:*

- Working Directory: The actual files reside here.
- Index: The area used for staging
- Head: Points to the most recent commit
 ![Work Flow](https://blog.udemy.com/wp-content/uploads/2015/08/image036.png)

### Saving Changes

All files in a checked out (or working) copy of a project file are either in a tracked or untracked state.

  *Tracked:*

Tracked files can be modified, unmodified, or staged; they were part of the most recent file snapshot.

  *Untracked:*

Untracked files were not in the last snapshot and do not currently reside in the staging area.

*After cloning a repository, files have tracked status and are unmodified because they have been checked out but not edited.*

### The Life Cycle of File Status

- 1.)  After you edit a file, Git flags it as modified because of changes made after the previous commit.
- 2.)  You stage the modified file.
- 3.)  Then, you commit staged changes.
![Flow Chart](https://blog.udemy.com/wp-content/uploads/2015/08/image006.png)

**Check File Status:**
To determine the state of files, utilize the git status command:

$ git status

**Tracking and Staging a New File:**

*Single File:*
Track one file only by using the following format:

git add filename

*All Files:*
Track all files in a repository by using the following command:

$ git add *

After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:

$ git status

**Committing a File:**
After staging one or multiple files, you should commit the changes and record what you did within the commit message:

$ git commit -m “made change x,y,z”

*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.

**Committing All Changes:**

$ git commit -a

*This command commits a snapshot of all modifications to tracked files in the working directory.

**Pushing Changes:**
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.

*Example:*

$ git push origin master

*This command pushes changes from the local “master” branch to the remote repository named “origin”.

*For cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local repository. However, these names can be changed by the user.

**Stashing Changes:**

When you are not ready to commit changes but do not want to lose them either, git stash is a great option. This command temporarily removes changes and hides them, giving you a clean working directory. When you are ready to continue working on the changes, simply use the git stash apply command to retrieve the hidden changes.

**Remote Repositories:**

In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.

$ git remote

you can view the short names, such as “origin,” of all specified remote handles.

$ git remote -v

you can view all the remote URLs next to their corresponding short names.

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)
