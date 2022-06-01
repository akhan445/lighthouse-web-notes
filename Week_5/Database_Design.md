# Database Design

Databases have been around for a while so the process of designing one is well documented.

The steps to design a database:
1. Determine the data that needs to be stored (usually by professionals with the domain knowledge).
2. Determine the data relationships.
    - where is the dependancy in the data (which parts are/are not unique, which parts rely on other data to to be retrieved)
3. Arrange the data into a logical structure which can then be mapped into storage objects (i.e tables).

## **ER Diagram**

Include the entity relation diagram which maps the blueprint of the database.

## **Normalization**

**Normalization** is the systematic way of ensuring that the database structure is suitable for general-purpose querying and free of undesirable characterstics (like update, delete, insert anomalies that could lead to loss of data integrity)
  - ensures data integrity
  - **reduced redundancy**

In a normalized database, data that maybe be repeated (i.e cohort names in students table) is not included in a table. Instead a ***referece is passed to refer to the table with the data***

Usually with normalization you would add seperate table for redundant data. 

## **Relationships in Databases**

Most common are one-to-one and one-to-many relationships

### One-to-many

Steps to determine 1 to many relationships:
| # | Step                                       | Example |
|:-:|:-------------------------------------------|:--------|
| 1 | Understan what is a 1 to many relationship | One record in a table can be related to many records in another table        |
| 2 | Write as sentence                          | Store the customer information and the orders that they have made       |
| 3 | Write down **objects** from sentence       | customer information, orders         |
| 4 | Determine if 1 to Many                     | For each ask: Does object1 have many object2s or does object2 have many object1s?  (only one would make sense)       |
| 5 | Create the diagram                         | -      |
| 6 | Draw a line between the tables             | -      |
| 7 | Add the crow's foot notation to the line   | - (***NOTE: Foreign key goes on the many side***)     |


### Many-to-many

Generally should be **avoided**. WHY? Because they interefere with normalization principles of the relational database. You will end up repeating values or foreign IDs.

To deal with this- create a **joining table**
- the joining table acts as a bridge and creates two one-to-many relationships