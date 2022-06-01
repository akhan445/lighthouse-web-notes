# Entity Relationship Diagrams

**ERD** is a graphical representation of the requirements of a database. This diagram summarizes a database through representing the information in tables and marks the relationships between these tables.
- serves as a blueprint of the database

Each ERD has 5 major parts: 
  1. **Entity**- represents a person, place of thing that you want to track in a database
      - This becomes **a table in the databse**
      - Each occurence appearing as a "row" in the database table will represent *an instance*. For example, if the entity is Student, each student is an instance
  2. **Attribute**- describes various characteristics about individual entity
      - a "colum" in the table, i.e id, name, etc.
  3. **Primary Key/Identifier**- is a **unqiue** attribute or set of attributes which identifies an insstance of the entity.
  4. **Relationship**- describes how one or more entities interact with each other
      - usually use a verb to describe the relationship. For example, student **has** a phone number 
  5. **Cardinality**- is the count of instances that are allowed/required between entity relationships
      - described using **minimum/maximum** values.
      - | Symbol                           | Meaning                     | Min : Max |
        |:--------------------------------:|:----------------------------|:----------|
        | ![one][one-link]                 | **Mandatory**- 1 and only 1 | 1 : 1     |
        | ![one-or-n][one-or-n-link]       |  **Mandatory**- At least 1  | 1 : N     |
        | ![zero-or-one][zero-or-one-link] | Optional- 0 or 1 only       | 0 : 1     |
        | ![zero-or-n][zero-or-n-link]     | Optional- 0 or more         | 0 : N     |






[one-link]: https://support.content.office.net/en-us/media/637523c1-13d1-4115-b283-b74f1cb26b04.png
[one-or-n-link]:https://support.content.office.net/en-us/media/bb23dbe2-469c-4855-b1d3-60f152219e74.png 
[zero-or-one-link]: https://support.content.office.net/en-us/media/2c940893-a22e-4a59-8ed3-02afef9624ec.png
[zero-or-n-link]: https://support.content.office.net/en-us/media/eb23b8f6-10cb-4b76-a0fe-f86a8f75823b.png