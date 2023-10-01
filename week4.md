# Code Review - Week 4 #
## Tim Honisett 40595819 ##

## Contents ##
1.  [The Code to Review](#the-code-to-review)
2.  [Identifying problems](#identifying-problems)
3.  [Suggested fixes](#suggested-fixes)
4.  [Documentation](#Documentation)


### The code to review ###

The code review is based on the snippet of code below

![](/images/code-review.png "")


### Identifying problems ###

1.  The method for creating a new invoice is embedded in the Main method which violates single responsbility principle.
2.  The Open/Close principle would be argued as broken given that the new invoice method is in the program class. It could be extrapulated that there would be a specific class that handles invoice functions.  It       could be argued that an application that manages invoices would have other functions.
3.  The constructor is immutable. The same invoice data will be created for each new invoice object
4.  The amount object is an integer, rather than having a decimal point
5.  The object names are in pascal case 

### Suggested Fixes ###

1.  Remove the invoice constructor and move into an invoice class. This would also correct point 2 from above
2.  Have objects passed as parameters to the constructor so that it will be mutable.
3.  Change the amount object datatype from integer to float
4.  Change the naming convention of the object names to camel case


### Documentation ###

workflow.md has been updated to provide instructions on the following

1.  Assign a review
2.  Perform a code review
3.  Respond to a code review
4.  Close an issue

