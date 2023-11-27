
## Code Review 1 ##

In the branch tab in GitHub, I could see that the below feature branch was ready for review (fig 1)

![](images/week12-review1-ready.png "")

**fig 1**

The code segment below was clear in that all the variable names were meaningfull and the datatypes matched what was expected from the variable name. For example, the DateTime was used for the date variable and int was used for the ID.  The model fitted the requirements of the Model, View architecture. (fig 2)

![](images/week12-review-1a.png "")

**fig 2**

The code segment below was again clear with good level of commentsl. However, the line StaffRotaModel newRota = GetNewRota was not particularly clean. Instead, I would have susggested using something on the line of StaffRota staffRota = GetNewRota. (Fig 3)

![](images/week12-review1b.png "")

**fig 3**

Once I reviewed the code, I added the comments and approved for changes. I decided to accept the changes as they did not neccessarily affect the code quality and that the project was comming to an end (fig 4).

![](images/week12-review1-comments.png "")

**fig 4**

I needed to resolve conflict merges prior to merging the feature branch into the development. Here, I was able to resolve the merge conflicts directly in GitHub (fig 5)

![](images/week12-reivew-conflict.png " ")

**fig 5**

Here is an example of a merge conflict.  The branch that requires merges has conflicts on lines 62 where a <Button label should have been added(fig 6). This was fixed by adding the button element.  The MAUI page would have failed to load if this fix was not applied.  See figure 7 for the change made.

![](images/week12-review1-pre-merge-fix.png " ")

**fig 6**

![](images/week12-post-conflict-merge.png " ")

**fig 7**



