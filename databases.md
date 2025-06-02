## Normal Forms
* 1NF (First Normal Form), 2NF (Second Normal Form), and 3NF (Third Normal Form) are levels of database normalization designed to reduce redundancy and ensure data integrity. 
* 1NF eliminates repeating groups of columns, 2NF removes partial dependencies, and 3NF eliminates transitive dependencies. 
    ### 1NF
    *  Ensures that each column in a table contains only atomic (indivisible) values. This means that a field should not contain multiple values or a set of values; rather, it should represent a single, indivisible piece of information. 
    * If a table has a column for "Addresses," and each row has multiple addresses in one column, 1NF would require that each address be moved to its own separate column, creating a new table for addresses if needed. 

    ### 2NF
    * Builds on 1NF by ensuring that non-key attributes (those not part of the primary key) are fully dependent on the entire primary key, not just part of it. 
    * If a table tracks course enrollments and has both Student ID and Course ID as part of the primary key, but Course Name only depends on the Course ID, 2NF would separate the Course Name into its own table that references the Course ID as a foreign key, eliminating the partial dependency. 
    
    ### 3NF
    * Builds on 2NF by eliminating transitive dependencies. 
    * Ensures that non-key attributes are only dependent on the primary key and not on any other non-key attributes. 
    * If a table has a column for "Department ID" and another column for "Department Name," and the Department Name is stored in the same table as the Department ID, 3NF would move the Department Name to a separate "Departments" table, reducing the redundancy by making the table only contain attributes that are directly dependent on the primary key. 