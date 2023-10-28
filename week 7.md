## Contents
1.  [Code Review](#code_review)
2.  [Merge feature branch into development] (#merge-feature-branch-into-development)


## Code Review

Prior to merging the feature branch into the devleopment, a code review on GitHub project repo is required first.

In this scenario, I reviewed the code that sets up the initiation of the database. Given that the same code applies to the ToDoList and that the developer confirmed that it worked on their local machine, I was able to review and approve the code segment quickly.

Below, shows how I did this directly in the GitHub repo.

Firstly, selelec the Pull Request section in the header and click on the branch you wish to review (fig 1)

![](images/git-see-pull-request.png "")

**fig 2 (view pull requests)**

Next, find the commit you wish to perform a code reivew on (fig 2)

![](images/git-select-code-to-reivew.png "")

**fig 2 (select commit to review)**

The code marked in green in figure 3 is the requested changes made. This was the code that was reviewed

![](images/git-reivew-code.png "")

**fig 3 (view PR request code)**

The code base marked in green was reviewed.  Once reviewed, click on Review Changes button on the top right hand side of the scren. Here, you can leave a comment, approve the request or request changes. Please note that the personal who created the Pull Request cannot approval or request their own changes (fig 4)

![](images/git-leave-review.png "")

**fig 4 (comment and approve/reject pull request)**

## Merge feature branch into development 

![](images/github-merge-request.png "")

**step 1 - click on Merge pull request**

![](images/github-confirm-merge.png "")

**step 2 - click on confirm merge**

![](images/github-merge-confirmed.png "")

**step 3 - merge of branches confirmed**

