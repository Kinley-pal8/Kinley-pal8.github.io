---
Title: DBS101 Flipped Class 5
categories: [DBS101, Flipped_Class]
tags: [DBS101]
---

### Topic : Normal Forms

---

Database normalization is a fundamental concept in database management that plays a critical function in optimizing database structure, reducing statistics redundancy, and enhancing data integrity. Normalization includes organizing records efficaciously to save you not unusual anomalies like insertion and deletion anomalies.The process of normalization is guided by a set of rules and pointers that help in structuring statistics successfully.

Purpose of Normalization:
Normalization serves several key purposes which might be vital for maintaining a nicely-structured database machine:
-  Data Integrity: By lowering redundancy, normalization  allows in preserving records accuracy and consistency.

- Efficient Storage: Normalized databases occupy much less garage space as reproduction facts is minimized, main to fee savings.

- Query Optimization: Queries come to be more efficient in normalized databases as they get admission to smaller, properly-based tables as opposed to big denormalized ones.

- Flexibility: Normalized databases are more flexible in accommodating modifications in facts requirements or commercial enterprise policies.

Levels of Normalization:
Database normalization is normally categorised into exceptional stages called ordinary paperwork. The maximum usually used regular paperwork encompass:

- First Normal Form (1NF): Ensures that every column in a desk carries atomic, indivisible values with specific names and no repeating corporations.

- Second Normal Form (2NF): Eliminates partial dependencies via making sure all non-key attributes are functionally dependent on the entire primary key.

- Third Normal Form (3NF): Eliminates transitive dependencies via making sure all non-key attributes are functionally depending on the primary key but now not on 
  different non-key attributes.

- Boyce-Codd Normal Form (BCNF): A stricter version of 3NF that ensures every non-trivial purposeful dependency is a superkey.

--- 

There are numerous levels of normal bureaucracy, each building upon the preceding one to make sure a properly-based database design.

- First Normal Form (1NF):
  In 1NF, every column in a desk includes atomic values, meaning no repeating companies or arrays.
  It guarantees that every attribute contains most effective a single value, warding off complex facts sorts like arrays or nested tables.


![alt text](https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcTNC2f8Cg2mUocoHelaeoemW2NHl4Cz_OheSKAdJTFZDC-W2hG0)


- Second Normal Form (2NF):
  2NF builds on 1NF with the aid of ensuring that all non-key attributes are fully useful dependent on the primary key.
  It gets rid of partial dependencies in which an characteristic relies upon on best part of the number one key.


![alt text](https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcRAm0TjfWokxrdqAbOWrHuSxFwr6jmujQCtNpxC0Wq_oevxUtDl)


- Third Normal Form (3NF):
  3NF similarly refines the normalization manner through getting rid of transitive dependencies.
  It guarantees that non-key attributes are not depending on different non-key attributes in the same table.


![alt text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTGWewQhThj1--CVAv2sneSEZ8yfvtct8r1vUdRmSdOhygxcLTB)


- Boyce-Codd Normal Form (BCNF):
  BCNF is a stricter version of 3NF where every determinant ought to be a candidate key.
  It gets rid of anomalies associated with purposeful dependencies and ensures statistics integrity.


![alt text](https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcRk3bxrSjMxyvzGzQdC3KdhOj6AsH8IRCD-dYgKBhL5Yc9FZS4E)


- Fourth Normal Form (4NF):
  4NF offers with multi-valued dependencies, in which one or extra attributes depend on multiple independent attributes.
  It helps in breaking down complex records systems into simpler, more potential bureaucracy.

- Fifth Normal Form (5NF):
  5NF entails in addition decomposition of tables to cast off be a part of dependencies.
  It objectives to lessen redundancy and make sure that every table serves a single purpose without overlapping records.

These process play a crucial position in database design via step by step lowering redundancy and making sure records integrity through well-described relationships among tables and attributes. By adhering to those normalization ranges, databases may be based correctly to minimize anomalies and optimize records garage.


