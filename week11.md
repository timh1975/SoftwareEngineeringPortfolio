### Tim Honsett 40595819 ###

## Contents

1.  [Workflow process](#workflow-process)
2.  [Managing Pull Request](#managing-pull-request)
3.  [Merge Conflict Management](#merge-conflict-management)
4.  [Code Review](#code-review)
5.  [Reflection](#reflection)

## Workflow process ##

The main areas in this portfolio focus on the the process of managing pull requests, conflict merge fixes and conducting code reviews.  This in concordance of the agreed team workflow as briefly outlined below.
The processes are broken down into their own sections

1.  Identify a feature branch that has a new pull request.  A pull request is made that identicates that it is ready for a code review.
2.  Identify a feature branch that has any merge conflicts. These were fixed so that approved code can be merged successfully into the development branch without causing merge conflict errors on merge.
3.  Code review using code smell and SOLID principles. Either approve or ask for changes
4.  If the code review has been approved, merged with the development branch.  I would fetch these changes into my development branch to check that the development branch works correctly.

## Managing Pull Request

Before looking feature branches that required a code review at pull request stage, I looked at all the branches at New pull request status.

Example provided in figure 1.

![](/images/week11-check-pull-requests.png "")

**figure 1 (Example of branch with new pull request)**

In the example below, the Pull Request workflow was not followed. Instead, it was indicated as read for code review in GitHub Project.  Before I undertook the code, I needed to create a pull request, as per figure 2.  Once of the lessons learnt earlier as that the master branch is automatically selected as the base branch. In GitHub, I need to change the base branch to the development branch. This is to comply with the workflow that only tested code that passed code review would be merged into the development branch. Only once the project is completed, which included testing the development branch, would the development branch be finally merged into the master branch.  Here, the code would be ready for deployment

![](/images/week11-create-pull-request.png "")

**figure 2 (Create a pull request)**

Here, it was noted there was a merge conflict. This needed to be fixed prior to code review, and based on the outcome, merged into the development branch.  Here, the conflicts could be resolved directly in GitHub (figure 3)

## Merge Conflict Management

![](/images/week11-merge-conflict.png "")

**figure 3 (Merge conflict)**

Figure 4 shows the conflict.  This was very straight forward to fix as there was no issue with the code. Instead, it was a case of removing git Header information, inlcuding HEAD, <<<< and  >>>> symbols as well as the name of the branches.  Changes can be seen in figure 5

![](/images/week11-pre-merge-conflict-fix.png "")

**figure 4 (merge conflicts prior to fixing)**

Whilst the above conflict merge could be fixed directly in GitHub, the example below needs to be fixed using git bash command line and directly editing the files where the conflicts occur. Figure 5 shows which files have the merge conflicts.

![](/images/week11-post-merge-conflict-fix.png "")

**figure 5 (merge conflicts fixed)**

![](/images/week11-conflict-command-line.png " ")

**figure 6 (Command line conflict merge)**

To undertake this fix, the following instructions were used with git bash shell (figure 7)

![](/images/week11-command-line-gitbash.png " ")

**figure 7 (Command line input for git bash)**

![](/images/week11-file-conflict-fix.png " ")

In figure 8, the TeamAlertsPage had a conflict merge.  Here, I accepted in incoming change as the ContentPage needs access to the Data folder.  Given that there is a team effort to move to the View, Model, ModelView architecture, adding a using statment to the Data folder would be in breach of that architecture. That is the Data Model must not be directly in communication to the Data Model. Instead, the ViewModel would facilitate communication between model and database.  As most of the views had not yet implemented the ViewModel module, it was decided to allow the incomming changes so that the feature branch would be functional in the development branch.

If this project was to merge to the ViewModel architecutre, the pull request would have been declined with the request that the user updates their feature branch to comply with the architecture.

**figure 8 (Fixing a conflict file )**

Once the merge conflicts were fixed, a code reivew was undertaken

## Code Review

In practice, I would be able to view the Ready to Review tab in GitHub Project.  Unfortunately, this column has not been kept updated.  Instead, I checked for new pull requests in GitHub. This was because the agreed workflow is that a pull request is made once the code is ready for review.  Prior to review, any conflict merge conflicts would be fixed.  Once a review has been undertaken, it would be accepted or rejected with required changes. Only approved feature branches would be merged into the development branch.  

In the first two code reviews, 2 issues were identified.  In figure 9a, the UserInput control names were not clearly defined as it was difficult to identify what data they are storing.  In figure 9b, there was no comemnts added to the methods. However, it was recognised that the superceeded fixes to the branch had the comments added.  Figure 10 shows the comments 

![](/images/week11-review1a.png " ")

**figure 9a (Incorrect instance usage)**

![](/images/week11-review1b.png " ")

**figure 9b (Unclear control item names)**

![](/images/week11-code-review1-comments.png " ")

**figure 10(Code review 1 and comments)**

In the third code review, 1 issue was identified.  There were commented out code sections. This is difficult to identify their purpose. Could be for the purpose of debugging which makes it unclear if the code is to be uncommented once it works. Another purpose in this scenario could be that the code would be uncommented until the table related to the foreign keys have been setup.  Either way, commented out code does not provide clarity for the purpose of that action (fig 11)

![](/images/week11-review2.png " ")

**Figure 11 (Code review 3)**

![](/images/week11-review2-comments.png " ")

**figure 12  (Code review 3 comments)**

## Reflection

The following are from this week's reflectins

1.  The GitHub project view needs to be updated the the entire team when a workflow procedure has been completed. Not doing so makes the process of managing pull requests, code reviews and merges less efficient. I need to go into GHitHub and look at each branch to see what actions I need to undertake on them.
2.  There needs to be better team instructions to minimise merge conflicts which is something I need to fix on the majority of pull requests. For example, ensuring that people are fetching the most recent remote repo and merging into their own local repo.
3.  As a follow up from the last few weeks of the project, I have gained a greater knowledge on git and GHitHub. I am learning how to manage merge conflicts and have been able to correct the development remote branch where these issues have occured so that team members are able to push from the remote to fix issues on their local machine. I have had exposure on how to deal with merge conflicts both directly in GitHub and remotely using the git bash shell and editing files that are afftect. I have identied whether to accept incoming changes, or not.  If the incoming change includes extra libaries required for that feature branch, removing unncessary lines or code or new code that does not effect the rest of the code base then the changes would be accepted. However, if the incoming changes overwrites someone else's code, introduces code that would fail, or introducing libary versions that cause a compatability issue then the incoming branch would be rejected.
4. For the last portfolio, I need to move my code to the View, ViewModel, Model example. This is for personal development as well as adopting the new architecture. I recognise that in the real world, updating achitecture during the development would not be appropriate as it makes the process less efficient given the required changes needed and the potential of introducing more complexity and errors. 
