# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**



<img width="883" height="268" alt="image" src="https://github.com/user-attachments/assets/9e67ffc1-e14b-4b5e-b72e-6141f874d2ab" />

**SQL**


<img width="359" height="152" alt="image" src="https://github.com/user-attachments/assets/a6ec793d-6877-4e65-b909-b75b2aabe5b9" />

**Output:**



<img width="872" height="346" alt="image" src="https://github.com/user-attachments/assets/0a3dcaa9-db99-4bc3-9629-695b02b7db11" />



**Question 2**




<img width="867" height="206" alt="image" src="https://github.com/user-attachments/assets/195c7451-2081-4989-b0c2-bcbbc8c58df8" />

**SQL**


<img width="584" height="145" alt="image" src="https://github.com/user-attachments/assets/ee36447a-711e-4813-9866-0c56965544e3" />


**Output:**




<img width="877" height="311" alt="image" src="https://github.com/user-attachments/assets/c977d305-bc04-40db-bd5d-fa196a2dad0d" />



**Question 3**



<img width="837" height="350" alt="image" src="https://github.com/user-attachments/assets/f691f38e-f97d-486a-a265-1645af3b6be0" />

**SQL**



<img width="751" height="196" alt="image" src="https://github.com/user-attachments/assets/1182c409-7985-446b-bf21-0cefbff56c2c" />

**Output:**



<img width="861" height="293" alt="image" src="https://github.com/user-attachments/assets/3c27ad41-a281-4e1d-ba47-d68162f7cbe9" />



**Question 4**



<img width="878" height="308" alt="image" src="https://github.com/user-attachments/assets/b137534d-17a0-41b0-80eb-5aea1e702131" />

**SQL**



<img width="442" height="163" alt="image" src="https://github.com/user-attachments/assets/f704e09a-3af8-4a8c-b536-17d56922de38" />

**Output:**



<img width="866" height="339" alt="image" src="https://github.com/user-attachments/assets/339c26c8-4dec-4c50-8c4f-eeec9d4b913e" />



**Question 5**




<img width="873" height="302" alt="image" src="https://github.com/user-attachments/assets/a281d84b-b2a6-48e5-bb61-020c0f3ff267" />

**SQL**



<img width="516" height="164" alt="image" src="https://github.com/user-attachments/assets/4a4d4698-f2a2-4227-b7dc-3c0ad77b6ca3" />

**Output:**



<img width="863" height="334" alt="image" src="https://github.com/user-attachments/assets/0f341dcd-28b0-4c55-ac90-8cf973e93a06" />



**Question 6**



<img width="545" height="265" alt="image" src="https://github.com/user-attachments/assets/70a50fc8-6a3e-495b-90e3-3c43a7fbdccd" />

**SQL**



<img width="504" height="121" alt="image" src="https://github.com/user-attachments/assets/bbceb9af-f7c1-4dc5-97f2-d8a0c7d201c6" />

**Output:**



<img width="867" height="334" alt="image" src="https://github.com/user-attachments/assets/5fef3325-afe4-45f1-aafd-4f7118d4f0a9" />



**Question 7**



<img width="733" height="300" alt="image" src="https://github.com/user-attachments/assets/0b9a5183-5502-4bc2-b159-cfe326bd9bc3" />

**SQL**



<img width="259" height="145" alt="image" src="https://github.com/user-attachments/assets/9c990044-c519-44ae-9a12-2c17ed0398a1" />


**Output:**



<img width="844" height="576" alt="image" src="https://github.com/user-attachments/assets/44f09cfc-fcab-4a4c-a40d-1b2b62a3f8a9" />



**Question 8**




<img width="855" height="295" alt="image" src="https://github.com/user-attachments/assets/09fc4577-40fa-4c12-b8eb-9e4605f37b7d" />

**SQL**



<img width="549" height="142" alt="image" src="https://github.com/user-attachments/assets/1be9dbae-80e3-46a2-8b06-aae2113bd4f7" />


**Output:**




<img width="862" height="374" alt="image" src="https://github.com/user-attachments/assets/07a42369-1676-4231-9347-487a2a590761" />



**Question 9**



<img width="602" height="256" alt="image" src="https://github.com/user-attachments/assets/acdf923c-cd3d-4f2e-8b77-c60988aa5cbe" />

**SQL**



<img width="340" height="178" alt="image" src="https://github.com/user-attachments/assets/69a2f77e-a3a9-496b-8839-0682c5dffb4e" />


**Output:**




<img width="855" height="298" alt="image" src="https://github.com/user-attachments/assets/70c67590-505a-4daa-90f0-804284489e07" />




**Question 10**




<img width="725" height="315" alt="image" src="https://github.com/user-attachments/assets/c949157e-f9f0-4166-b0b6-532b6718c5ea" />

**SQL**



<img width="338" height="100" alt="image" src="https://github.com/user-attachments/assets/8a50ed2d-942b-4824-a056-15c01e5c9fa3" />


**Output:**




<img width="870" height="311" alt="image" src="https://github.com/user-attachments/assets/4805567b-cb0c-4c64-84eb-0d664efe187d" />



## SCREENSHOT OF M1-SEB GRADE





<img width="454" height="262" alt="image" src="https://github.com/user-attachments/assets/0e32cc85-8a36-48a1-8224-2c61ab2a9d47" />




<img width="921" height="881" alt="image" src="https://github.com/user-attachments/assets/66e29c04-2353-488a-8a36-10725dd0b2ed" />



## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
