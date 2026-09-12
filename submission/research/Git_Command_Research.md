# Git squash:
this command is used to merge more than one small commits in a big one 
so that if we are working on a feature on a branch for example working on the payment feature , the main branch should see one commit of the payment feature done , so if we have in the payment branch a commit for the choosing payment method , another commit for validation of the used credit card , another commit for inserting new card , git squash would merge all these small commits into one commit

# Git help:
this command is used to get the documentation of any git command and how to use it in case you don't know how to use it or forget its way of using , it has two ways to apply , the first one is git help <command> or git <command> --help which gives you the full explanaition of that command , the second one is git <command> -h which gives you a quick short help with that command

# Git clean:
this command helps you to delete the untracked files which haven't been put in the staging area , a scenario that can be useful for using that command is to when yo are working locally on some feature and you generated some temporary files that you need to use , soft-test that feature but that files are not necessary to get commited or tracked , so when you finish the development of the feature you are no longer need these files so this command clean your local project folder from these untracked unecessary files so if we used it the untracked files can't be rescued again to be tracked later 

# Git blame:
this command tells you who last changed each line in a file, and in which commit so it is like a detailed history of the file you specify in the command to get who changed in it , in which lines and in which commit , if we are working on a feature and the work is split between us so that each one file , two students are finishing it , then after that file is finished they would push it to the branch but to know which student made which lines in the file we use this command 

# Git shortlog:
this command gives you a brief of the commits done and the author who did them , this command can be used if you just need the number or the author of the commits done without knowing the commit id so you can't come back to a certain commit by git checkout command

# Git prune:
this command removes Git objects that are no longer reachable from any branch like tags so if there is an unreachable commit and there is no branch or tag or pointer pointing towards that comit , this command removes entirely that commit object 

# Git bisect:
this command makes us inspect which commit has the problem without checking all the done commits , if we started with commit c1 and it was working properly and ended with c5 and it has a bug but we don't know which commit between c1 and c5 started the bugs so this command let us jump into the middle commit which is the c3 and then we inspect the c3 commit if this commit is good then wwe know that the problem shrinked between c4 and c5 

# Git greb:
this command makes you find a certain word , function or anything inside the project repo , for example if i want to find the leetcode links in this submission i may type git grep "leetcode"

# Git filter-repo:
Imagine you accidentally commit and push a .env file containing an API key. Later, you remove the file and add it to .gitignore, but the secret still exists inside older commits. In that case, you use git filter-repo to rewrite the repository history and remove the secret from all past commits. Because this changes commit hashes, teammates may need to re-clone the repository

# Git merge vs Git rebase:
Imagine you are working on a feature branch while main also receives new commits. If you use git merge, Git combines both histories and usually creates a merge commit, preserving the real branching history — this is safer for shared branches. If you use git rebase, Git takes your feature commits and replays them on top of the latest main, creating a cleaner straight-line history but changing the commit hashes. So the rule is: use merge for shared history, and rebase mainly for your own private feature branch before it is shared

# Git cherry-pick:
Imagine a teammate has a branch containing three different unfinished changes, but one commit contains an urgent bug fix you need on main. Instead of merging the whole branch and bringing in all the unfinished work, you use git cherry-pick <commit-hash> to copy only that one specific commit onto your current branch. Git creates a new commit with the same change but a new hash

# Git worktree:
Imagine you are halfway through a large feature and your current branch has unfinished changes, but suddenly you need to check or fix something on main. Instead of stashing your work and constantly switching branches, you use git worktree to create another folder connected to the same repository, with main checked out there. This lets you work on both branches at the same time in separate folders without disturbing your current work