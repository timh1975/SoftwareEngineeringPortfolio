# Tim Honisett - Portfolio for Week 10 #

## Contents
1.  [Checking on Pull Requests](#checking-on-pull-requests)
2.  [Conflict Management](#conflict-management)
3.  [Correcting peer code review](#correcting-peer-code-review)
4.  [Reflection](#reflection)

In this week's portfolio, I will focus on code review from pull requests, managing conflict errors and merging feature branches into the development branch.

## Checking on Pull Requests ##

I read through the existing pull requests, looking for those who have had code reviews and ready for merging. I checked that comments for a code review I underook last week were actioned. (fig 1).  The request asked that comments were added and that commented out code was removed.

![](/images/week10-check-changes-made.png "")

**fig 1**

Once the review of changes were confirmed, I added comments in the reivew and approved the request (fig 2). The next step was to merge the feature branch into the development branch.

![](/images/week10-code-review-completed.png "")

**fig 2**

## Conflict Management ##

Once the code was reviewed, I was ready to merge it into the developement branch. However, as seen in figure 3, there were merge conflicts I had to address first. [GitHub](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line) defines a merge conflict where completing changes are made in the same line of a file, or an indivual edits a file that is deleted by someone else.

I would have to review where the code conflicts occured and decided on wheather to accept the code changes in the feature branch I reviewed, or keep the orginal code. I had to use git bash command shell and a code editor to correct these merge conflicts.

![](/images/week10-github-merge-issues.png "")

**fig 3**

GitHub provided a list of commands and instructions required to fix this issue, as shown in figure 4.

![](/images/week10-command-line-instructions.png "")

**fig 4**

The git status command showed the files that had the conflicts marked in red (fig 5).  These conflicts were complicated and therefore had to be managed via git bash command line and editing the affected files, rather than directly in GitHub.  

![](/images/week10-git-merge-conflict.png "")

**fig 5**

Using Visual Studio code as a file editor, I opened each file that had the merge conflicts.  The example below in figure 6 is straight forward. The Using System was added on the same file line by two different people .  All I needed to do was to accept the incoming change (from the feature branch I was reviewing).

![](/images/week10-correcting-merge-conflict.png  "")

**fig 6**

The example below is more complicated. Here, new and updated Nugent packages have been added to the repository.  I decided to accept incoming changes to allow for package updages and import packages that were required for the feature branch.  However, this is not always the best approach as updates could stop existing code from working correctly.  This issue was experienced during the Software Engineering Methods project where GitHub actions failed due to a mismatch/incompatable package versions. See fig 7

![](/images/week10-correcting-merge-conflict-complex.png "")

**fig 7**

Once the conflicts had been resolved, the feature branch was merged into the devleopment branch (fig 8)

![](/images/week10-mrge-request.png "")

**fig 8**

There were other Pull Requests that had more straight forward merge conflicts that can be directly fixed in GitHub.  This can be identified by not have a greyed out Rosolved Conflicts button is shown in figure 3.

Figure 9 shows what a file with a merge conflict looks like.  The code between <HEAD in line 38 and==== on line 43 is the original code, known as Current Change. Code below 43 is the code that is going to replace the original code, known as Incoming Change. 

In GitHub, the file was opened for editing and <Head along with === and >> removed. A closed bracket has added to line 43. The changes were then commited directly to the feature branch file.  Figure 10 shows the changes made to that file 

![](/images/week10-fixing-conflict-github.png "")

**fig 9**

![](/images/week10-fixing-conflict-github-fixed.png "")

**fig 10**

There were two risk indentified when editing merge conflict errors directly in GitHub, when compared to using an IDE. Firstly,  is that HEAD markers such as <, = and > need to be removed as they are interpreted as syntax code erors. Secondly, valid code syntax would be removed. The second example happened after I fixed an issue directly in GitHub. This was undertaken by correcting the issue directly in GitHub and in my local repository.

Once the Pull Requests have been approved and merged, the issue in GitHub Projects was moved from Ready To Merge to Completed (fig 11).

![](/images/wek10-github-project-board.png "")

**fig 11**

## Correcting peer code review ##

I received feedback from my code review from last weeek with the following comments

1.  Variable names should be readable. E.g.: instead of ea --> equipmentAllocation or equipmentAlloc (EquipmentDB.cs > AddEquipmentAllocation() method)
2.  Doxygen comments were added for the View classes, on the other hand, a summary comment on the top of the Page class could have been added to explain the Page's general functionality/purpose
3.  No doxygen comments added for the Model classes

    My colleauge and I agreed to push my feature branch to the devleopment branch given that the feedback was on the comments, rather than the codebase itself. Furthremore, I thought that this was most appropriate so that my code can be incorporated into the remote codebase for the benefit of others. For example, they can access the data models and database class if their issues require access to my database objects.

Despite this, I decided to incorporate the requested comments.  I created a new feature branch based on the remote development and added the comments. Once completed, pushed it back and requested a pull request.

Figure 12 shows a snippet of code before amendments were made. Here an instance of the Equipment model was named as eq. In figure 13, this was changed to equipment.

![](/images/week10-own-code-review-pre-fix.png "")

**fig 11**

![](/images/week10-own-code-review-post-fix.png "")

**fig 12**

## Reflection ##

This week, I had the following reflections
1.  Need to commit changes to git more often to prevent merge conflicts on my local repository.
2.  Need to observe GitHub more frequently to action approved pull requests so that everyone can take advantaged of updated development branch.
3.  Need to be more careful when applying merge conflict edits directly in GitHub so I dont accidently remove valid syntax.
4.  Need to ensure that variable naming is consistent and clear, particularly with database class instances.
5.  One of my colleagues have started applying the View/ViewModel/Model architecture. Need to start exploring this for my next issue.

   On reflection, this week provided an opportunity to learn how to approve pull request and merge these branches.  It provided execellent exposure to dealing with merge conflicts in the git bash shell and learnt what needs to be removed from affected files, making sure header details are moved and how to select either an incoming or current change. 

The aims of the next few weeks is to apply the View/ViewModel/Model architecture to my next issues.
