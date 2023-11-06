
## Issue

I took on the issue that dealt with storing information on equipment.  Looking at the ERD, there are three tables that relate to this.
  1.  Equipmennt.  This table stores information on each piece of equipment.
  2.  Equipment_Type. This table stores a list of equipment categories
  3.  Equipment_Allocation.  This table stores information on where and when equipment is allocated

The table structures were added to the models architucture. The example below (fig 1) is for the Equipment Allocation table.  The knowledge gained from last week was applied in the method of adding a foreign key.  Furthermore, I learnt that SQLite does not use the DATE data structure, ratht that the dates are stored in strings.

![](/images/week9-add-model.png "")

**fig 1 (Equipment Table model)**

A seperate database class was created to store the CRUD functions for the Equipment related tables.  In figure 2, the InitiateDataBase method creates a new local database if it does not already exists 


  

## Code Review

## Reflection

The following reflections were made from this portfolio

1.  There could be a debate of having a database class for each of the equipment related tables. However, it was decided to keep them in one database class using the following that the InitateDataBase function creates all related equipoment tables. This was decided to do this in one function given that they are linked with foreign keys. This was to minimise the risk of tables not being created properly if a foreign key does not yet reference an existing table.  Furthermore, given that there were only 8 methods, it was decided that this was not too much for one class.
   
2. Whilst using a local database in the early development, I have recognise that this is problematic in the following ways
     2.1  There is the requirement for features to be merged into the development branch in order to sync the local database with changes due to added tables.
     2.2  Datasets would need to be provded to be added to the local database to sync up data.
     2.3  Not having a fully sync database would provide difficulty in testing for system wide compatability.

3.  No unit tesing was put in place. I was able to figure out using mock tests for this week. This is an area I recognise I need to gain knowledge and skilsl on for both the project module for semester 2, as well as for professional practice. 
