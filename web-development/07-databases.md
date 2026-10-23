
# Databases — Complete Learning Guide

Welcome to databases! Databases allow applications to store, organize, retrieve, update, and protect information. Almost every real-world application—from social networks to online stores—depends on reliable data storage.

In this guide, you'll learn relational databases using PostgreSQL, practice SQL, understand database design, explore performance and security, and get an introduction to NoSQL databases.

**Goal:** Design a database, write useful SQL queries, and connect a database to a backend application.

**Prerequisites:** Complete [JavaScript Fundamentals](03-javascript-fundamentals.md) and [Backend Development](06-backend-development.md).

---

## How to Use This Guide

For each step:

1. Watch the recommended lecture or search for a suitable lesson.
2. Run the examples in your own database environment.
3. Complete the practice exercises.
4. Check your results and explain your queries.
5. Commit your project changes to Git.

**Video-link note:** The YouTube links below open topic-specific searches rather than individually verified videos. Choose a clear, up-to-date lecture covering the listed concepts. Prefer one comprehensive lecture per step when it covers everything required; use focused lessons only for gaps.

**Main learning path:** PostgreSQL and SQL.

**Additional learning path:** MongoDB and document databases.

---

## Step 1: Understand What a Database Is

### Learn

- What databases are and why applications use them
- Database management systems (DBMS)
- Relational vs. non-relational databases
- Structured data and unstructured data
- Tables, rows, columns, and records
- Database schemas
- Persistent storage vs. temporary application memory
- Basic examples of database use in websites

### Watch

- [Database Fundamentals for Beginners](https://www.youtube.com/results?search_query=database+fundamentals+for+beginners+DBMS+SQL+NoSQL)

### Practice

1. List five applications that use databases.
2. Identify the kinds of information each application stores.
3. Sketch a simple database for a student registration system.
4. Explain why storing application data only in a JavaScript array is insufficient for a real production application.

**Checkpoint:** You can explain what a database does and why applications need persistent storage.

---

## Step 2: Choose a Database and Set Up PostgreSQL

### Learn

- What PostgreSQL is
- Installing PostgreSQL or using a suitable hosted development environment
- Database servers and client tools
- Connecting to a database
- Creating a database
- Basic use of `psql` or a graphical database client
- Development databases vs. production databases

### Watch

- [PostgreSQL for Beginners — Installation and Setup](https://www.youtube.com/results?search_query=PostgreSQL+for+beginners+installation+setup+database)

### Practice

1. Install PostgreSQL or choose an appropriate learning environment.
2. Connect using `psql` or a database GUI.
3. Create a database named `learning_db`.
4. List the available databases.
5. Connect to `learning_db`.

Example SQL:

```sql
CREATE DATABASE learning_db;
```

If you use `psql`, you can connect with:

```text
\c learning_db
```

The `\c` command is specific to the `psql` client; it is not standard SQL.

**Checkpoint:** You can connect to PostgreSQL and work inside your own practice database.

---

## Step 3: Learn SQL Fundamentals

SQL (Structured Query Language) is used to work with relational databases.

### Learn

- What SQL is
- Creating tables with `CREATE TABLE`
- Adding records with `INSERT`
- Reading records with `SELECT`
- Updating records with `UPDATE`
- Deleting records with `DELETE`
- Filtering with `WHERE`
- Sorting with `ORDER BY`
- Limiting results with `LIMIT`
- Understanding `NULL`

### Watch

- [SQL Full Course for Beginners](https://www.youtube.com/results?search_query=SQL+full+course+for+beginners+SELECT+INSERT+UPDATE+DELETE)

### Practice

Create a table:

```sql
CREATE TABLE students (
    id INTEGER GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(255) UNIQUE NOT NULL,
    age INTEGER
);
```

Insert sample records:

```sql
INSERT INTO students (name, email, age)
VALUES
    ('Asha', 'asha@example.com', 20),
    ('Rahul', 'rahul@example.com', 22),
    ('Maya', 'maya@example.com', 19);
```

Retrieve the records:

```sql
SELECT * FROM students;

SELECT name, age
FROM students
WHERE age >= 20
ORDER BY age DESC;
```

Update a record:

```sql
UPDATE students
SET age = 21
WHERE email = 'asha@example.com';
```

Delete a record only when you intend to remove it:

```sql
DELETE FROM students
WHERE email = 'maya@example.com';
```

### Additional practice

1. Retrieve only student names.
2. Find students older than 20.
3. Sort students alphabetically.
4. Change one student's email.
5. Delete a test record and verify the result.

**Checkpoint:** You can perform basic CRUD operations using SQL.

---

## Step 4: Data Types and Constraints

### Learn

- Integer and decimal types
- `VARCHAR` and `TEXT`
- `BOOLEAN`
- `DATE` and timestamp types
- Primary keys
- Foreign keys
- `NOT NULL`
- `UNIQUE`
- `CHECK`
- Default values
- Choosing suitable types for each field

### Watch

- [SQL Data Types, Primary Keys, and Constraints](https://www.youtube.com/results?search_query=PostgreSQL+SQL+data+types+primary+key+foreign+key+constraints)

### Practice

Create a products table:

```sql
CREATE TABLE products (
    id INTEGER GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
    name VARCHAR(150) NOT NULL,
    price NUMERIC(10, 2) NOT NULL CHECK (price >= 0),
    stock INTEGER NOT NULL DEFAULT 0 CHECK (stock >= 0),
    is_active BOOLEAN NOT NULL DEFAULT TRUE
);
```

Try inserting valid and invalid records. Observe how the constraints protect the database from incorrect data.

### Practice tasks

1. Add a product with a valid price.
2. Try inserting a negative price.
3. Try omitting a required field.
4. Add a unique product code.
5. Explain why constraints should be enforced in the database, not only in the frontend.

**Checkpoint:** You can choose appropriate data types and use constraints to protect data integrity.

---

## Step 5: Relationships and Database Design

Most applications store information across multiple related tables.

### Learn

- One-to-one relationships
- One-to-many relationships
- Many-to-many relationships
- Primary and foreign keys
- Junction tables
- Entity-relationship diagrams (ERDs)
- Referential integrity
- Cascading updates and deletes
- Avoiding duplicated information

### Watch

- [SQL Table Relationships and Database Design](https://www.youtube.com/results?search_query=SQL+database+relationships+one+to+many+many+to+many+ERD+beginner)

### Practice

Design a simple course enrollment database with three tables:

- `students`
- `courses`
- `enrollments`

A student can enroll in multiple courses, and each course can have multiple students.

Example structure:

```sql
CREATE TABLE courses (
    id INTEGER GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
    title VARCHAR(150) NOT NULL
);

CREATE TABLE enrollments (
    student_id INTEGER NOT NULL REFERENCES students(id),
    course_id INTEGER NOT NULL REFERENCES courses(id),
    enrolled_at TIMESTAMPTZ NOT NULL DEFAULT CURRENT_TIMESTAMP,
    PRIMARY KEY (student_id, course_id)
);
```

The `students` table was created in Step 3. The `enrollments` table uses a composite primary key to prevent duplicate enrollment records for the same student and course.

### Practice tasks

1. Draw an ERD for the enrollment system.
2. Explain why enrollments need a separate table.
3. Insert sample students and courses.
4. Enroll students in different courses.
5. Try creating an enrollment that references a nonexistent student.

**Checkpoint:** You can model relationships and explain why foreign keys matter.

---

## Step 6: Filtering, Aggregation, and Grouping

### Learn

- `AND`, `OR`, and `NOT`
- `IN`, `BETWEEN`, and `LIKE`
- `IS NULL` and `IS NOT NULL`
- Aggregate functions: `COUNT`, `SUM`, `AVG`, `MIN`, and `MAX`
- `GROUP BY`
- `HAVING`
- The difference between `WHERE` and `HAVING`
- Basic date filtering

### Watch

- [SQL Filtering, Aggregate Functions, GROUP BY, and HAVING](https://www.youtube.com/results?search_query=SQL+WHERE+GROUP+BY+HAVING+aggregate+functions+tutorial)

### Practice

Using your students and courses data:

1. Count the total students.
2. Find the average student age.
3. Count enrollments for each course.
4. Find courses with more than one enrollment.
5. Filter students using multiple conditions.
6. Search for names matching a pattern.

Example:

```sql
SELECT course_id, COUNT(*) AS enrollment_count
FROM enrollments
GROUP BY course_id
HAVING COUNT(*) > 1;
```

**Checkpoint:** You can filter, summarize, and group data to answer useful questions.

---

## Step 7: SQL Joins

Joins combine information from related tables.

### Learn

- `INNER JOIN`
- `LEFT JOIN`
- `RIGHT JOIN`
- `FULL OUTER JOIN`
- Joining more than two tables
- Table aliases
- Join conditions
- Common mistakes that create duplicate rows
- When a subquery may be useful instead

### Watch

- [SQL Joins Explained with Examples](https://www.youtube.com/results?search_query=SQL+joins+inner+left+right+full+join+explained+beginner)

### Practice

Retrieve student names alongside their courses:

```sql
SELECT
    s.name AS student_name,
    c.title AS course_title
FROM enrollments e
JOIN students s ON s.id = e.student_id
JOIN courses c ON c.id = e.course_id
ORDER BY s.name, c.title;
```

Try additional queries:

1. List all students and their courses.
2. Find students who have not enrolled in a course.
3. List every course, including courses with no enrollments.
4. Count the number of students enrolled in each course.

**Checkpoint:** You can combine related tables and understand how different joins affect the results.

---

## Step 8: Subqueries, CTEs, and Views

### Learn

- What a subquery is
- Subqueries in `WHERE` and `FROM`
- Common table expressions using `WITH`
- Views
- When to break a complex query into smaller steps
- Basic window-function concepts

### Watch

- [SQL Subqueries, CTEs, and Views](https://www.youtube.com/results?search_query=PostgreSQL+SQL+subqueries+CTE+WITH+views+beginner)

### Practice

1. Find students older than the average age.
2. Use a CTE to calculate enrollment counts.
3. Create a view that lists courses and their enrollment totals.
4. Rewrite one complex query using a CTE.
5. Explore a window function such as `ROW_NUMBER()`.

Example CTE:

```sql
WITH course_counts AS (
    SELECT course_id, COUNT(*) AS total
    FROM enrollments
    GROUP BY course_id
)
SELECT *
FROM course_counts
ORDER BY total DESC;
```

**Checkpoint:** You can organize more complex queries into understandable parts.

---

## Step 9: Normalization and Data Integrity

### Learn

- Why duplicated data causes problems
- Insert, update, and delete anomalies
- First, second, and third normal forms (1NF, 2NF, and 3NF)
- Separating entities into appropriate tables
- Functional dependencies at a basic level
- When denormalization may be useful
- Why normalization is a design tool rather than a goal to pursue blindly

### Watch

- [Database Normalization Explained — 1NF, 2NF, and 3NF](https://www.youtube.com/results?search_query=database+normalization+1NF+2NF+3NF+examples)

### Practice

1. Start with a table that stores a student and several course names in one field.
2. Identify the duplicated data.
3. Separate students, courses, and enrollments into related tables.
4. Explain how your design avoids repeating course information.
5. Check that your foreign keys and constraints enforce valid relationships.

**Checkpoint:** You can design a database that minimizes unnecessary duplication and maintains consistent data.

---

## Step 10: Transactions and Concurrency

Transactions help multiple database operations succeed or fail as one logical unit.

### Learn

- What a transaction is
- `BEGIN`, `COMMIT`, and `ROLLBACK`
- The ACID properties
- Why partial updates can be dangerous
- Concurrent requests and conflicting changes
- Isolation levels at a conceptual level
- Locking and deadlocks at a basic level

### Watch

- [PostgreSQL Transactions and ACID Properties](https://www.youtube.com/results?search_query=PostgreSQL+transactions+ACID+COMMIT+ROLLBACK+beginner)

### Practice

Run a transaction:

```sql
BEGIN;

UPDATE products
SET stock = stock - 1
WHERE id = 1 AND stock > 0;

-- Inspect the result before committing.
ROLLBACK;
```

This example deliberately rolls back the change. In a real application, verify that the intended update occurred before committing.

### Practice tasks

1. Insert a record inside a transaction and roll it back.
2. Repeat the operation and commit it.
3. Explain why a payment and its related order update should not be left half-completed.
4. Learn how transactions help preserve data consistency.

**Checkpoint:** You understand how transactions protect multi-step database operations.

---

## Step 11: Indexes and Query Performance

Indexes can make some queries faster, but they also require storage and can add overhead to writes.

### Learn

- What an index does
- Primary-key indexes
- Unique indexes
- Indexing frequently queried columns
- Composite indexes
- The impact of indexes on inserts and updates
- Reading query plans with `EXPLAIN`
- Why measuring matters more than guessing

### Watch

- [PostgreSQL Indexes and Query Optimization](https://www.youtube.com/results?search_query=PostgreSQL+indexes+EXPLAIN+ANALYZE+query+optimization+beginner)

### Practice

1. Create a larger set of sample records.
2. Inspect a query plan using `EXPLAIN`.
3. Add an index to a frequently filtered column.
4. Compare query plans before and after the index.
5. Explain why adding an index to every column is not a good strategy.

Example:

```sql
CREATE INDEX idx_students_age
ON students(age);

EXPLAIN
SELECT *
FROM students
WHERE age >= 20;
```

**Checkpoint:** You can explain why indexes exist and use query plans to investigate performance.

---

## Step 12: Database Security and Backups

### Learn

- Database users and roles
- Least-privilege permissions
- Safe connection settings
- SQL injection
- Parameterized queries
- Secrets and environment variables
- Backups and restoration
- Data retention and privacy
- Why production data must be handled carefully

### Watch

- [PostgreSQL Security, Roles, and Backups](https://www.youtube.com/results?search_query=PostgreSQL+roles+permissions+pg_dump+backup+restore+security)

### Practice

1. Create a separate database user for an application.
2. Grant only the permissions it needs.
3. Use parameterized queries in backend code.
4. Learn how `pg_dump` creates a PostgreSQL backup.
5. Practice restoring a backup into a test database.
6. Ensure database credentials are not committed to Git.

**Checkpoint:** You understand the fundamentals of database access control, safe queries, and recovery.

---

## Step 13: Connect PostgreSQL to a Node.js Backend

Now connect your database knowledge to the backend skills from the previous guide.

### Learn

- Installing a PostgreSQL client library
- Connection strings and environment variables
- Connection pools
- Parameterized queries
- Mapping API operations to database queries
- Handling database errors
- Schema changes and migrations
- Why database calls should not block the application through careless resource handling

### Watch

- [Node.js and PostgreSQL — Full Integration Tutorial](https://www.youtube.com/results?search_query=Node.js+PostgreSQL+pg+connection+pool+parameterized+queries+tutorial)

### Practice

1. Install a PostgreSQL driver such as `pg`.
2. Configure the database connection using environment variables.
3. Create an API endpoint that lists products.
4. Add an endpoint that creates a product using validated input.
5. Use parameterized queries instead of building SQL through string concatenation.
6. Handle missing records and database failures.
7. Close or manage database resources appropriately.

Example parameterized query:

```javascript
const result = await pool.query(
  "SELECT id, name, price FROM products WHERE id = $1",
  [productId]
);
```

This assumes that `pool` is a configured PostgreSQL connection pool and that the surrounding function handles asynchronous errors.

**Checkpoint:** Your backend can safely read and write persistent database records.

---

## Step 14: Introduction to NoSQL and MongoDB

Relational databases are an excellent foundation, but document databases are also useful for certain applications.

### Learn

- What NoSQL means
- Relational tables vs. document collections
- MongoDB databases, collections, and documents
- Basic CRUD operations in MongoDB
- Flexible document structures
- Embedding vs. referencing related documents
- Basic indexing
- Why choosing a database depends on the application's requirements

### Watch

- [MongoDB for Beginners — Complete Course](https://www.youtube.com/results?search_query=MongoDB+full+course+beginners+CRUD+collections+documents)

### Practice

1. Install MongoDB locally or use an appropriate learning environment.
2. Create a collection for products.
3. Insert a few documents.
4. Find documents using filters.
5. Update and delete a document.
6. Compare the same product data modeled in PostgreSQL and MongoDB.

Example MongoDB shell operations:

```javascript
db.products.insertOne({
  name: "Notebook",
  price: 5.99,
  inStock: true
});

db.products.find({ inStock: true });
```

The JavaScript-like commands above are for the MongoDB shell, not ordinary SQL.

**Checkpoint:** You understand the main differences between relational and document databases and can perform basic MongoDB operations.

---

## Step 15: Build a Complete Database Project

Build a **Course Enrollment Database** that combines the concepts from this guide.

### Requirements

- Students table
- Courses table
- Enrollments table
- Appropriate primary and foreign keys
- Constraints for valid data
- Queries for common operations
- Joins to display related information
- Aggregations for enrollment statistics
- Transactions where multiple operations must succeed together
- Indexes for justified query-performance needs
- A database backup
- A documented way to set up the database from scratch

### Build it in stages

1. Draw an entity-relationship diagram.
2. Create the database and tables.
3. Add appropriate data types and constraints.
4. Insert sample data.
5. Write CRUD queries.
6. Write joins and aggregate queries.
7. Add transactions for suitable multi-step operations.
8. Inspect query plans and add indexes when justified.
9. Connect the database to a Node.js API.
10. Back up and restore the database in a test environment.
11. Document the schema, example queries, and setup instructions.

### Optional challenges

- Add course instructors.
- Add enrollment dates and status.
- Prevent duplicate enrollments.
- Add search, sorting, and pagination to the API.
- Add a database migration workflow.
- Build a simple frontend to display courses and enrollment statistics.

**Project completion:** You can explain the schema, write queries independently, connect the database to an API, and demonstrate that the data persists correctly.

---

## Recommended Learning Resources

- [PostgreSQL Official Documentation](https://www.postgresql.org/docs/) — reference material and tutorials.
- [PostgreSQL Tutorial](https://www.postgresqltutorial.com/) — structured PostgreSQL lessons.
- [SQLBolt](https://sqlbolt.com/) — interactive SQL exercises.
- [SQLZoo](https://sqlzoo.net/) — hands-on SQL practice.
- [MongoDB University](https://learn.mongodb.com/) — MongoDB learning courses.
- [Node.js PostgreSQL Client — node-postgres](https://node-postgres.com/) — connect Node.js to PostgreSQL.
- [OWASP SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html) — learn safe database query practices.

---

## Final Completion Checklist

- [ ] Explain what a database and DBMS do.
- [ ] Set up and connect to PostgreSQL.
- [ ] Write SQL CRUD queries.
- [ ] Choose suitable data types and constraints.
- [ ] Design relationships using primary and foreign keys.
- [ ] Filter, sort, group, and aggregate data.
- [ ] Write joins and subqueries.
- [ ] Understand normalization.
- [ ] Use transactions appropriately.
- [ ] Investigate query performance with indexes and query plans.
- [ ] Understand database permissions, backups, and SQL injection prevention.
- [ ] Connect PostgreSQL to a Node.js API.
- [ ] Perform basic MongoDB operations.
- [ ] Complete and document the Course Enrollment Database project.

## What's Next?

Continue to [Full-Stack Development](08-full-stack-development.md) to combine frontend, backend, and database skills into a complete application.

---

**Remember:** Good database design is about more than storing information. It is about keeping data accurate, making it easy to retrieve, protecting it, and ensuring it remains reliable as an application grows.
