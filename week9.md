
## Issue

I took on the issue that dealt with storing information on equipment.  Looking at the ERD, there are three tables that relate to this.
  1.  Equipmennt.  This table stores information on each piece of equipment.
  2.  Equipment_Type. This table stores a list of equipment categories
  3.  Equipment_Allocation.  This table stores information on where and when equipment is allocated

The table structures were added to the models architucture. The example below (fig 1) is for the Equipment Allocation table.  The knowledge gained from last week was applied in the method of adding a foreign key.  Furthermore, I learnt that SQLite does not use the DATE data structure, ratht that the dates are stored in strings.

![]("/images/week9-add-model.png "")

**fig 1 (Equipment Table model)**
  

## Code Review

## Reflection
