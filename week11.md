## Managing Pull Request

Before looking feature branches that required a code review at pull request stage, I looked at all the branches at New pull request status. Example provided in figure 1.

![](/images/week11-check-pull-requests.png "")

**figure 1 (Example of branch with new pull request**

In the example below, the Pull Request was not followed. Instead, it was indicated as read for code review in GitHub Project.  Before I undertook the code, I needed to create a pull request, as per figure 2.  Once of the lessons learnt earlier as that the master branch is automatically selected as the base branch. In GitHub, I need to change the base branch to the development branch. This is to comply with the workflow that only tested code that passed code review would be merged into the development branch. Only once the project is completed, which included testing the development branch, would the development branch be finally merged into the master branch.  Here, the code would be ready for deployment

![](/images/week11-create-pull-request.png "")

**figure 2 (Create a pull request)**

Here, it was noted there was a merge conflict. This neede to be fixed prior to code review, and based on the outcome, merged into the development branch.  Here, the conflicts could be resolved directly in GitHub (figure 3)

![](/images/week11-merge-conflict.png "")

**figure 3 (Merge conflict)**

Figure 4 shows the conflict.  This was very straight forward to fix as there was no issue with the code. Instead, it was a case of removing git Header information, inlcuding HEAD, <<<< and  >>>> symbols as well as the name of the branches.  Changes can be seen in figure 4

![](/images/week11-pre-merge-conflict-fix.png "")

**figure 4 (merge conflicts prior to fixing)**

![](/images/week11-post-merge-conflict-fix.png "")

**figure 5 (merge conflicts fixed)**

Once the merge conflicts were fixex, a code reivew was undertaken

## Code Review

In figure 6, it was noted that the OnClickSave event initiation of the FinanceModel class referenced the GetNewParter.  Instead of FinanceModel newTask = GetNewPartner, it should have been something similiar to FinanceModel financeModel - FinanceModel.  

![](/images/week11-code-review1.png " ")

**figure 6 (code review example 1)**


**figure 7 (code review 1 comments)**

The review example in figure 8 lacked comments. However, it was recognised that there was a newer feature branch which superceeded it to fix some issues. Here, the code was commented.

![](/images/week11-code-review2.png " ")

**figure 8 (code review example 2)**

![](/images/week11-code-review3.png " ")

In figure 10, lines of 
