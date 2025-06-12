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


## Data Lake
* Storage repository for storing large amounts of raw, unstructured data.
* E.g.: S3

## Data warehouse
* Stores pre processed, structured data for analysis
* Redshift, pSQL, Snowflake

## Graph Databases
* Graph databases are specialized types of databases designed to store, query, and manage relationships between data efficiently. Unlike relational databases (which use tables), graph databases use nodes and edges
    * Nodes represent entities (e.g., people, places, things)
    * Edges represent relationships between them (e.g., "knows", "located in", "follows")
* They are ideal for scenarios with complex and interconnected data, such as:
    * Social networks (users, friends, followers)
    * Recommendation engines (users, products, ratings)
    * Fraud detection (transactions, devices, locations)
    * Knowledge graphs (concepts and their relationships)

## Geospatial Indexes
* Geospatial indexes are special data structures that allow a database to efficiently store, search, and query spatial data—that is, data representing physical locations on Earth (e.g., latitude and longitude, shapes, distances, areas).
* They are like regular indexes (used to speed up data lookups) but optimized for:
    * Points: GPS coordinates (e.g., lat=12.97, lon=77.59)
    * Shapes: Polygons, lines, bounding boxes (e.g., a city boundary or a route)
    * Distances: Radius-based lookups (e.g., "find all cafes within 5 km")
* MongoDB also lets you create geospatial indexes (`db.places.createIndex({ location: "2d" })`). Here's how it works
        * Internally MongoDB uses Google’s S2 Geometry Library, which:
            * Projects Earth onto a cube
            * Divides each face of the cube into a hierarchical grid of cells
            * Each cell gets a unique ID
            * These cell IDs are stored in a B-tree-like structure
    * It maps your Point/Polygon → set of S2 cell IDs
    * These IDs are encoded and stored in a B-tree
    