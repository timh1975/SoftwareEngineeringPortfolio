
For this week's portfolio, I will focus on code review, managing conflict errors and merging feature branches into the development branch.

## Code Review ##

Last week, I undertook a code review and commented that it lacked comments and and had commented out code.  This week I reviewed the same code and noticed tht these issues have been corrected.  The feature branch was ready for merging into the development branch.

Firstly, I added comments in the reivew and approved (fig 1)

![](/images/week10-code-review-completed.png "")

**fig 1**

## Conflict Management ##

The branch had conflicts that had to be resolved (fig 2). This is because the feature branch had code that conflicts on the same lines as the development branch. I would have to review where the code conflicts occured and decided on wheather to accept the code changes in the feature branch I reviewed, or keep the orginal code.  

![](/images/week10-github-merge.issues.png "")

**fig 2**

Github had a list of git bash command line information which I followed (fig 3)

![](/images/week10-command-line-instructions.png "")

**fig 3**

The git status command showed the files that had the conflicts marked in red (fig 4)

![](/images/week10-git-merge-conflict.png "")

**fig 4**

Using Visual Studio code as a code editor, I opened each file that had the merge conflicts.  The example below in figure 5 is stragith forward.  The using System line looks identical, with the only difference being all being a space which was enought for git to see this as a change.  All I needed to do was accept the incoming change (from the feature branch I was reviewing) as this one had the line removed.

![](/images/week10-corecting-merge-conflict.png "")
**fig 5**




