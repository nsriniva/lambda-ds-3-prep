# [Sprint 2 - SQL and Databases](https://learn.lambdaschool.com/ds/sprint/recV8wEgPdwWmUInW)

Helpful links:

  + https://github.com/prof-rossetti/gwu-istm-4121-201509
  + https://tableplus.com/
  + https://github.com/prof-rossetti/radio-data
  + https://tableplus.com/blog/2018/07/sqlite-how-to-create-a-local-database-file-on-mac.html
  + https://pandas.pydata.org/pandas-docs/stable/getting_started/comparison/comparison_with_sql.html
  + https://elephantsql.com/
  + https://www.hackerrank.com/domains/sql


```sh
which sqlite3
```

```sh
which postgres
```

```sh
which mysql
```

---

Setup:

```sh
touch data/radio_data.db
# open table plus and import all radio data CSV files
```

```sql
CREATE UNIQUE INDEX `listeners_pk` ON `listeners` (`id` ASC);
CREATE UNIQUE INDEX `listener_accounts_pk` ON `listener_accounts` (`listener_id` ASC);

CREATE UNIQUE INDEX `songs_pk` ON `songs` (`id` ASC);

CREATE UNIQUE INDEX `plays_pk` ON `plays` (`id` ASC);
CREATE INDEX `plays_fk_listener` ON `plays` (`listener_id` ASC);
CREATE INDEX `plays_fk_song` ON `plays` (`song_id` ASC);

CREATE UNIQUE INDEX `skips_pk` ON `skips` (`id` ASC);
CREATE INDEX `skips_fk_play` ON `skips` (`play_id` ASC);

CREATE UNIQUE INDEX `thumbs_pk` ON `thumbs` (`id` ASC);
CREATE INDEX `thumbs_fk_play` ON `thumbs` (`play_id` ASC);
```


## [Class 5 - Introduction to SQL](https://learn.lambdaschool.com/ds/module/recmwiPQG5zueKFCG/)

> Challenges:
>  + Imagine the customers table also has address and customer_since attributes (where customer_since is a year). Write a query to get all names and addresses of customers living in Colorado who have been customers for at least 10 years.
>  + Come up with your own real-world examples of situations/data that can be modeled with one-to-one, one-to-many, and many-to-many relationships. Write “pseudo-SQL” to describe and query the data.

  + Remember to count rows and "row by what?"

A Side:

  + Databases
  + DBMS
  + Entities
  + Single-table SQL (SELECT, FROM, WHERE, ORDER BY, LIMIT)
  + Aggregations (GROUP BY)

B Side:

  + ERD
  + Relationships (1:1, 1:M, M:M)
  + Multi-table SQL (JOIN, LEFT JOIN)
  + ERD / Normalization practice?

C Side / Next Class:

   + DB Management SQL (CREATE DATABASE, CREATE TABLE, INSERT INTO, ETC.)
   + SQLite Python (connections, cursor, queries, etc).

Next Class:



## [Class 6 - SQL for Analysis](https://learn.lambdaschool.com/ds/module/recSdx6IFkDxqgxGb/)

> Challenge: Write a Python function to generate random data for insertion, and execute it in a loop in order to generate and insert a large quantity of data.

   + DB Management SQL (CREATE DATABASE, CREATE TABLE, INSERT INTO, ETC.)
   + PG Python (connections, cursor, queries, etc).

## [Class 7 - NoSQL and Document-Oriented Databases](https://learn.lambdaschool.com/ds/module/rec3JRFsRH2yeALwS/)


> Objectives:
>  +  Come up with two situations, one where relational is appropriate and another where non-relational is. Describe both in writing, as if you were making a recommendation to your manager for which database to choose.
>  + Use dir() and help() to inspect the db.test object, and see what else you can do. In particular, check out db.test.insert_many and db.test.find_many, to let you work with lots of data at once!

  + MongoDB

## [Class 8 - ACID and Database Scalability Trade-offs](https://learn.lambdaschool.com/ds/module/rec9c9nW20Sn6TBAO/)

> Objectives:
>  + Think of a situation (besides finance) where ACID guarantees are mission-critical, and another where it may be okay to weaken them. Describe both to a fellow student, and explain your reasoning.
>  + Think about how you’d apply MapReduce to calculate gradient descent (the algorithm underpinning many statistical models). Try to sketch at a conceptual level/pseudocode, and then search for existing implementations and resources. Spend at least 20 minutes thinking about it before you look things up!
