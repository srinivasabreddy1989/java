Git 
Git is a fast, scalable, distributed revision control system with an unusually rich command set that provides both high-level operations and full access to internals.
 to configure git
    git config --global user.name "Your Name Comes Here"
    git config --global user.email you@yourdomain.example.com
git init:- To initiate empty git repository
    You’ve now initialized the working directory—​you may notice a new directory created, named ".git".
git diff --cached
git status
git commit 
git commit -a :-which will automatically notice any modified (but not new) files, add them to the index, and commit, all in one step.
Git tracks content not files
git log
git log -p :-If you also want to see complete diffs at each step, use
git log --stat --summary:-Often the overview of the change is useful to get a feel of each step

Managing branches:
    git branch experimental:- To create new branch
    git branch: To check available branches
    git switch experimental: To switch branch
    git commit -a
    git switch master
    gitk : to see conflict in grapgical manner
    git pull
Using Git for collaboration
    git clone /home/alice/project myrepo
    git commit -a
    alice$ cd /home/alice/project
    alice$ git pull /home/bob/myrepo master
    alice$ git fetch /home/bob/myrepo master
    alice$ git log -p HEAD..FETCH_HEAD
    gitk HEAD..FETCH_HEAD
    gitk HEAD...FETCH_HEAD
    alice$ git remote add bob /home/bob/myrepo
    alice$ git fetch bob
    alice$ git log -p master..bob/master
    alice$ git merge bob/master
    alice$ git pull . remotes/bob/master

Exploring history
    git log
    git show c82a22c39cbc32576f64f5c6b3f24b99ea8149c7
    git show c82a22c39c	# the first few characters of the name are
			# usually enough
    $ git show HEAD		# the tip of the current branch
    $ git show experimental	# the tip of the "experimental" branch
    git show HEAD^  # to see the parent of HEAD
    $ git show HEAD^^ # to see the grandparent of HEAD
    $ git show HEAD~4 # to see the great-great grandparent of HEAD
    $ git show HEAD^1 # show the first parent of HEAD (same as HEAD^)
    $ git show HEAD^2 # show the second parent of HEAD
    git tag v2.5 1b2e1d63ff
    $ git diff v2.5 HEAD	 # compare the current HEAD to v2.5
    $ git branch stable v2.5 # start a new branch named "stable" based
			 # at v2.5
    $ git reset --hard HEAD^ # reset your current branch and working
			 # directory to its state at HEAD^
    $ git log v2.5..v2.6            # commits between v2.5 and v2.6
    $ git log v2.5..                # commits since v2.5
    $ git log --since="2 weeks ago" # commits from the last 2 weeks
    $ git log v2.5.. Makefile       # commits since v2.5 which modify
                    # Makefile
    git log stable..master
1. Local area
2. Staging area
3. Remote repository

git
----
options
    --version
    --help
        These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs
   show      Show various types of objects
   status    Show the working tree status

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects

    -C <path>
GIT COMMANDS
------------
    High-level commands (porcelain)
    git add
    git-am - Apply a series of patches from a mailbox
    git-archive - Create an archive of files from a named tree
    git-bisect - Use binary search to find the commit that introduced a bug
    git branch :- List, create, or delete branches
    git-bundle - Move objects and refs by archive
    git-checkout - Switch branches or restore working tree files
    git-cherry-pick - Apply the changes introduced by some existing commits
    git-citool - Graphical alternative to git-commit
    git-clean - Remove untracked files from the working tree
    git clone
    git commit
    git diff :-Show changes between commits, commit and working tree, etc
    git fetch :-
    git-gc - Cleanup unnecessary files and optimize the local repository
    git grep: Print lines matching a pattern
    git-gui - A portable graphical interface to Git
    git init
    git log
    git-merge - Join two or more development histories together
    git mv
    git pull
    git rebase
    git reset:-Reset current HEAD to the specified state
    git restore:- Restore working tree files
    git revert:-Revert some existing commits
    git rm
    git stash:- Stash the changes in a dirty working directory away
    git status:
    git switch:
    git tag:-
    git:- the git repository browser

    Ancillary Commands
    ------------------
    git config
    git fast exporter
    git fast importer
    git mergetool
    git prune
    git remote

git-config - Get and set repository or global options
------------------------------------------------------



FAST-FORWARD MERGE
TRUE MERGE
