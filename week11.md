## Managing Pull Request

Before looking feature branches that required a code review at pull request stage, I looked at all the branches at New pull request status. Example provided in figure 1.

![](/images/week11-check-pull-requests.png "")

**figure 1 (Example of branch with new pull request**

In the example below, the Pull Request was not followed. Instead, it was indicated as read for code review in GitHub Project.  Before I undertook the code, I needed to create a pull request, as per figure 2.  Once of the lessons learnt earlier as that the master branch is automatically selected as the base branch. In GitHub, I need to change the base branch to the development branch. This is to comply with the workflow that only tested code that passed code review would be merged into the development branch. Only once the project is completed, which included testing the development branch, would the development branch be finally merged into the master branch.  Here, the code would be ready for deployment

![](/images/week11-create-pull-request.png "")

**figure 2 (Create a pull request)**

Here, it was noted there was a merge conflict. This neede to be fixed prior to code review, and based on the outcome, merged into the development branch.  Here, the conflicts could be resolved directly in GitHub (figure 3)

## Merge Conflict Management

![](/images/week11-merge-conflict.png "")

**figure 3 (Merge conflict)**

Figure 4 shows the conflict.  This was very straight forward to fix as there was no issue with the code. Instead, it was a case of removing git Header information, inlcuding HEAD, <<<< and  >>>> symbols as well as the name of the branches.  Changes can be seen in figure 4

![](/images/week11-pre-merge-conflict-fix.png "")

**figure 4 (merge conflicts prior to fixing)**

![](/images/week11-post-merge-conflict-fix.png "")

**figure 5 (merge conflicts fixed)**

Whilst the above conflict merge could be fixed directly in GitHub, the example below needs to be fixed using git bash command line and directly editing the files where the conflicts occur. This is shown in figure 6

![](/images/week11-conflict-command-line.png " ")

**figure 6 (Command line conflict merge)**

To undertake this fix, the following instructions were used with git bash shell (figure 7)

![](/images/week11-command-line-gitbash.png " ")

**figure 7 (Command line input for git bash)**

GitHub shows which files have that have the conflicts as shown in figure 8



Once the merge conflicts were fixex, a code reivew was undertaken


## Code Review

In the first two code reviews, 2 issues were identified.  In figure Xa, the UserInput control names were not clearly defined as it was difficult to identify what data they are storing.  In figure Xb, there was no comemnts added to the methods. However, it was recognised that the superceeded fixes to the branch had the comments added.  Figure X shows the comments 

![](/images/week11-review1a.png " ")

**figure Xa (Incorrect instance usage)**

![](/images/week11-review1b.png " ")

**figure Xb (Unclear control item names)**

![](/images/week11-code-review1-comments.png " ")

**figure X(Code review 1 and comments)**

In the third code review, 1 issue was identified.  There were commented out code sections. This is difficult to identify their purpose. Could be for the purpose of debugging which makes it unclear if the code is to be uncommented once it works. Another purpose in this scenario could be that the code would be uncommented until the table related to the foreign keys have been setup.  Either way, commented out code does not provide clarity for the purpose of that action (fig X)

![](/images/week11-review2.png " ")

**Figure X (Code review 3)**

![](/images/week11-review2-comments.png " ")

**figure  (Code review 3 comments)**


