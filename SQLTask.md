Scenario
Imagine you are managing a magazine shop and want to digitize your inventory by creating a table that captures essential information about each magazine. You need a streamlined table structure with only the most relevant details to keep things simple and effective.

Instructions
Create a Magazine table with four key attributes representing each magazine in your shop. You can use an application like Excel or Google Sheets for the structured data entry and analysis. Complete these steps to build your table:

Define the attributes for the Magazine table and identify four key data elements needed to manage a magazine’s information.

Title: The name of the magazine.

Publisher: The company or individual responsible for publishing the magazine.

Publication Date: The date when the magazine was published.

Price: The selling price of the magazine.

Assign data types and constraints by defining the appropriate ones for each attribute.

Set up the Primary Key and choose an attribute as the primary key to identify each record uniquely.

Examine the table when created and review its structure to ensure it matches the desired attributes and constraints.

Solution :

create schema/database first 

CREATE DATABASE magazine;

NOW SELECT IT SO YOU CAN CREATE TABLE INSIDE IT 

USE magazine;

NOW CREATE TABLE

CREATE TABLE Magazine (
    Title VARCHAR(255) NOT NULL PRIMARY KEY,
    Publisher VARCHAR(255) NOT NULL,
    Publication_Date DATE NOT NULL ,
    Price DECIMAL(5,2) NOT NULL

)
IF NEEDED TWO PRIMARY KEY USED THIS     PRIMARY KEY (Title, Publication_Date)