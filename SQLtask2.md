The bookshop aims to digitize its inventory by creating a digital catalog. This catalog will store all the essential information about each book, such as the book title, author details, genre, publication year, and more.

Let’s define the data elements you need for the Books table.

Instructions
Identify key data elements by considering what information is necessary for a comprehensive book catalog and the details needed to represent each book in the shop. For example:

Title: The name of the book.

Author: The person or people who wrote the book.

Author gender: The author's gender is useful for demographic studies or targeted marketing.

Publication year: The year the book was published.

Genre: The book category, such as fiction, non-fiction, mystery, etc.

Book price: The selling price of the book.

Book availability: Indicates whether the book is in or out of stock.

Book cover: The file URL of the book’s cover image.

ISBN: A unique identifier for the book.

Condition: The physical or digital condition of the book (e.g., new, used).

solution :

CREATE DATABASE bookstore;
USE bookstore;

CREATE TABLE books (
ISBN char(17) not null primary key,
Title varchar(255) not null,
Author varchar(255) not null,
AuthorGender enum('Male','Female') ,
PublicationYear year not null,
Genre varchar(255) not null,
BookPrice decimal(10,2) not null,
BookAvailability boolean not null,
BookCover varchar(255) not null,
bookCondition varchar(50) not null
)

Task 2: Establish relationships between tables
This task focuses on correctly linking the Sales table to the Book table to provide a reliable, integrated data structure for tracking sales corresponding to specific books. To establish a relational connection between the tables, you must define foreign key constraints and understand the relationships' cardinality.

The first step is to establish a link.

Instructions
To establish a relational link between the Sales and Books tables, you need to define a foreign key in the Sales table that references the Books table. This is how:

Review the table structures:

Ensure the Book table has a primary key defined, typically the ISBN which uniquely identifies each book.

Verify that the Sales table has a column ready to hold the ISBN values that will link sales records to the books they represent.

Define the foreign key constraint:

Identify the column in the Sales table that will act as the foreign key. This column should have the same data type as the ISBN in the Book table to ensure compatibility.


CREATE TABLE sales (
TransactionID  int not null AUTO_INCREMENT primary key,
DateofSale date not null,
QuantitySold int not null,
BookISBN char(17) not null ,
foreign key (BookISBN)
references books(ISBN)

)

Once you’ve established a link, the next step is to identify cardinality.

Instructions
Define the nature of the relationship between the Book and Sales tables, focusing on the cardinality of this relationship. Here’s how:

Understand cardinality: Review the concept of cardinality in database relationships.  

Identify relationship features: Determine how each entry in the Book table, identified uniquely by ISBN, can be associated with entries in the Sales table based on One-to-One, One-to-Many, or Many-to-Many relationships. 

Visual representation: Create a suitable ER diagram to visually represent the relationship.  

Solution
Understand cardinality: Cardinality refers to the numerical relationship between rows in two connected tables. In this case, how many entries in the Sales table can be associated with entries in the Book table (e.g., one-to-one, one-to-many, or many-to-many)?

Identify relationship features: Note that each entry in the Book table, identified uniquely by ISBN, can be associated with multiple entries in the Sales table. This is because a single book can be sold many times.

This means that the relationship between the Book and Sales tables is a One-to-Many relationship:

One book (one ISBN) can be related to many sales transactions in the Sales table.

Each record in the Sales table refers to one and only one record in the Book table (via the ISBN).


For clarification, the cardinality between the Book and Sales tables is One-to-Many. Each book, uniquely identified by its ISBN, can be associated with multiple sales transactions, while each individual sale references exactly one ISBN from the Book table. This relationship is fundamental for tracking the number of times each book is sold and linking each sale to the specific details.