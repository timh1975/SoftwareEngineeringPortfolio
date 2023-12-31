### Week 5 - Software Engineering - Tim Honisett - 40595819

## Contents

1.  [Clean Code](#clean-code)
2.  [Code Documentation with Doxygen](#code-documentation-with-doxygen)
3.  [Process Documentation](#process-documentation)
4.  [References](#references)


## Clean Code

Martin(2009) was used as a template for determing clean code for the code that was written in week 3.

### Meaningful Names

Classes and methods were provided with meaningful names to indicate their functions.  Folders added and named according to the function of their specific classes which included DataBase, Views, Models and, Images. This is to allow for the application to use the View/Model architecture.

Several of the class names were updated to make their functions clearer.  Constrant was changed to Config, Note to NoteTable.

### Functions

Methods are kept small and had one specific function.  Some of the functions were renamed to make then more descriptive. Db.Init was changed to InitaliseDataBase, NotePage.SaveButton_Clicked to SaveNote_Clicked and, NotePage.DeleteButton_Clicked to DeleteNote.

It was decided to leave the DeleteNote_Clicked method blank at present. This is to allow for the view to have the delete button.  The delete functionality will be added to the method.

### Comments

Comments were added to the methods using Visual Studio IntelliSense.  Doxygen used to create the API documentation. [See Doxygen section.](#code-documentation-with-doxygen)

### Formatting

Consistant formatting applied thought out application including:

1.  Having opening and closing brackets on their own line and indendent these code sections.
2.  Space between inport, using, clas, and method statements.
3.  Classes and methods kept short, applying single responsbility policy.
4.  Statements fit in the width of the screen.

### Objects and Data Structures

To comply with data abstraction principles, the following were applied to the application.  
1.  Getters and setters were applied to the NotesTables class
2.  Database abstraction was added to the notes view by having the database functions moved to their own class.

However, a better approach to the application would have been to add the three level architecture model. This is where a layer of abstraction would be added between the view and database class.  Instead of the view being able to communicate directly to the database, the view would communicate to the business layer, which in terms, communicates directly to the database class.  This way, the view does not need to concern itself with the workings of the database thus removing the coupling between view and database.  This would also apply to the principles of the law of demeter where an object should not expose its internal structure.

### Error Handling

Error handling has not yet been added to the application.  The following would need to be added to the next iteration

1.  Validating path name for database
2.  Validating that notes page is not blank prior to saving data

### Classes

Class objects have getters and setters for encapsulation. Classes are small and are dedicated to a particular set of related functions. For example, classes were created to 

1.  Provide database configuration
2.  Database CRUD operations
3.  Note table definitions

Class names where chosen to provide a descriptive definition.

## Code Documentation with Doxygen

Doxygen was used to create API document.The next step is to add parameters to the documentation.  Figure (1) list of classes, figure (2) list of  methods, figure (3) methods in database class

![](/images/doxygen-class-list.png "")

Figure(1) class list

![](/images/doxygen-function-list.png "")

Figure(2) method list

![](/images/doxygen-function-method.png "")

Figure(3) methods in Database class

## Process Documentation

Doxygen.md added to the document folder in the remote repo.  Communicated to team that this has been added.


## References

Martin, RC. (2009). *Clean code: a handbook of agile software craftmanship*. Pearson 
