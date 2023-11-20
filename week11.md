## Managing Pull Request

Before looking feature branches that required a code review at pull request stage, I looked at all the branches at New pull request status. Example provided in figure 1.

![](/images/week11-check-pull-requests.png "")

** figure 1 (Example of branch with new pull request **

In the example below, the Pull Request was not followed. Instead, it was indicated as read for code review in GitHub Project.  Before I undertook the code, I needed to create a pull request, as per figure 2.  Once of the lessons learnt earlier as that the master branch is automatically selected as the base branch. In GitHub, I need to change the base branch to the development branch. This is to comply with the workflow that only tested code that passed code review would be merged into the development branch. Only once the project is completed, which included testing the development branch, would the development branch be finally merged into the master branch.  Here, the code would be ready for deployment

![](/images/week11-create-pull-request.png "")

** figure 2 (Create a pull request) **

Here, it was noted there was a merge conflict. This neede to be fixed prior to code review, and based on the outcome, merged into the development branch.  Here, the conflicts could be resolved directly in GitHub (figure 3)


