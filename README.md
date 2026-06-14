SQL

sql commands are categorized into 4 types 

DDL (data definition language)
. define
. alter
. delete 

DML (data manipulation language)

.insert
.update
.delete

DQL (data query language)

. query
. retrieve

DCL (data control language)

. manage  userrs
. permission
. pivileges

-----------------

sql comparison operators help retrieve update analyze data
filter data manipulate data

--------








operator                 explanation
 =                        equal to 
<> or !=                  exclude records
< or >                    exceeds or less than specified value
>= or <= or between       records within a specified range 
NULL                      missing records/values
NOT NULL                 no missing records or value

IN                      records ewxists within a set

LIKE                    matches pattern indicated with wildcards % multiple characters _ single characters 

EXISTS                 subquery returns any row

ANY                    compare value to any in a list 

ALL                  compare value to all in a list

NOT                 exclude value from a list


---------------------


select 

SELECT title , author FORM  books;


insert

INSERT INTO books (bookid,bookname,author)
VALUES (12,'lion king','james');

update

UPDATE books
SET bookname = 'CLASSIC FIGHT'
WHERE bookname = 'lion king';

delete 

DELETE FROM books WHERE bookname = 'CLASSIC FIGHT';









