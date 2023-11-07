
## Issue

I took on the issue that dealt with storing information on equipment.  Looking at the ERD, there are three tables that relate to this.
  1.  Equipmennt.  This table stores information on each piece of equipment.
  2.  Equipment_Type. This table stores a list of equipment categories
  3.  Equipment_Allocation.  This table stores information on where and when equipment is allocated

## Maintaining agreed architecture

My code base followed the following code architecture. This was decided by the group after undertaking the ToDoList example.

  1.  Database class for CRUD operations was added to the Data folder
  2.  The table structures were added to the models folder
  3.  The views and their underlying code were added to the Views folder.

The table structures were added to the models architucture. The example below (fig 1) is for the Equipment Allocation table.  The knowledge gained from last week was applied in the method of adding a foreign key.  Furthermore, I learnt that SQLite does not use the DATE data structure, ratht that the dates are stored in strings.

![](/images/week9-add-model.png "")

**fig 1 (Equipment Table model)**

A seperate database class was created to store the CRUD functions for the Equipment related tables.  In figure 2, the InitiateDataBase method creates a new local database if it does not already exists 

![](/images/week9-add-initiate.png "")
  
**fig 2 (Initiate Database and tables)**

The code below shows 2 CRUD methods in the database class. They have comments placed on top to add Doxygen documents, have single responsbility and short.  Improvments would include changing the name strings in line 80 to something more meaningfull, such as names_returned. The SQL statement for the GetEquipment method is vulnerable to SQL injection attacks as the serach query is embedded in the statement.  Given the scope of this project, it was decided not to add protection this week. However, this is something I will learn and implement in future projects. 

There are three seperate views for the graphical interface which was added to the view model. A equipment UI was created with three buttons: add equipment type, add equipment and allocate equipment.

Error capturing was added to the Add Equipment Page. Fig 3 shows an error message when data fields are null prior to saving.  Fig 4 shows the code that validates user input by checking if the editor boxes is null. If so, it returns false.

Fig 4 shows how the error capture is handled if the validation is false, by the use of a condition. If it is false, a error message will apear as in fig 3, otherwise it will save the record

![](/images/week9-error-capture.png "")

**fig 3(Error capturing)**

![](/images/week9-validate-date.png "")

**fig 4(Validate user input method)**

![](/images/week9-error-capture-in-method.png "")

**fig 5(Error capture handling in AddEquipment method)**

## Documentation



## Code Review

I undertook the code view (fig 6). Whilst most of the code was clean, it did lack comments and some lines of code was commented out.  I provided this in a feedback (fig 7)
and requested for changes.




## Reflection

The following reflections were made from this portfolio

1.  There could be a debate of having a database class for each of the equipment related tables. However, it was decided to keep them in one database class using the following that the InitateDataBase function creates all related equipoment tables. This was decided to do this in one function given that they are linked with foreign keys. This was to minimise the risk of tables not being created properly if a foreign key does not yet reference an existing table.  Furthermore, given that there were only 8 methods, it was decided that this was not too much for one class.
   
2. Whilst using a local database in the early development, I have recognise that this is problematic in the following ways
     2.1  There is the requirement for features to be merged into the development branch in order to sync the local database with changes due to added tables.
     2.2  Datasets would need to be provded to be added to the local database to sync up data.
     2.3  Not having a fully sync database would provide difficulty in testing for system wide compatability.

3.  No unit tesing was put in place. I was able to figure out using mock tests for this week. This is an area I recognise I need to gain knowledge and skilsl on for both the project module for semester 2, as well as for professional practice.
4.  Given that SQL injection vulnerability was recognised, I would need to read up on optimising SQL statments to mitigate for these risks.  
