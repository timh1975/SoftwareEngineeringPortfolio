
For this week's portfolio, I will focus on code review from pull requests, managing conflict errors and merging feature branches into the development branch.

## Checking on Pull Requests ##

I read through the existing pull requests, looking for those who have had code reviews and ready for merging.  I undertook a check that the comments for the code reivew I undertok last week had been actioned. (fig 1).  The request asked that comments were added and that commented out code was removed.

![](/images/week10-check-changes-made.png "")

**fig 1**

Once the reive of changes were confrime, I added comments in the reivew and approved (fig 2). The next step was to merge the feature branch into the development branch.

![](/images/week10-code-review-completed.png "")

**fig 2**

## Conflict Management ##

The branch had conflicts that had to be resolved (fig 3). This is because the feature branch had code that conflicts on the same lines as the development branch. I would have to review where the code conflicts occured and decided on wheather to accept the code changes in the feature branch I reviewed, or keep the orginal code.  

![](/images/week10-github-merge-issues.png "")

**fig 3**

Github had a list of git bash command line information which I followed (fig 4)

![](/images/week10-command-line-instructions.png "")

**fig 4**

The git status command showed the files that had the conflicts marked in red (fig 5).  These conflicts were complicated and therefore had to be managed via git bash command line and editing the affected files, rather than directly in GitHub.  

![](/images/week10-git-merge-conflict.png "")

**fig 5**

Using Visual Studio code as a code editor, I opened each file that had the merge conflicts.  The example below in figure 6 is straigt forward.  The using System line looks identical, with the only difference being all being a space which was enought for git to see this as a change.  All I needed to do was accept the incoming change (from the feature branch I was reviewing) as this one had the line removed.

![](/images/week10-correcting-merge-conflict.png  "")

**fig 6**

The example below is more complicated. Here, new and updated Nugent packages have been added to the repository.  I decided to accept incoming changes to allow for package updages and import packages that were required for the feature.  However, this is not always the best approach as updates could stop existing code from working properly.  This issue was experienced during the Software Engineering Methods project where GitHub actions failed due to a mismatch/incompatable package versions. See fig 7

![](/images/week10-correcting-merge-conflict-complex.png "")

**fig 7**

Once the conflicts had been resolved, the feature branch was merged into the devleopment branch (fig 8)

![](/images/week10-mrge-request.png "")

**fig 8**


