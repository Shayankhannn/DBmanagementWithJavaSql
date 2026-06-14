Explore an example: Filtering by equality
Imagine you want to create a playlist of all "Rock" tracks from your music store's database. You know that the GenreId for Rock is 1, so you can use an equality condition to filter tracks with GenreId = 1.

You have the following columns in the Tracks table:

TrackId: Unique identifier for each track.

Name: Name of the track.

AlbumId: Identifier for the associated album.

GenreId: Identifier for the track's genre.

Composer: Composer of the track.

Instructions
Follow these steps in the interactive code block:

Select all columns from the Tracks table.

Use the WHERE clause to filter rows where GenreId = 1.

Run the query to view the output. 


SOLution :

SELECT * FROM Tracks WHERE GenreId = 1 ;

-----------

Challenge 1: Filter by range
Now it’s your turn! Imagine you want to analyze all invoices issued between November 1, 2013, and December 31, 2013. Using a date range condition can help you narrow down the results to only those invoices.

The Invoices table includes the following columns:

InvoiceId: Unique identifier for each invoice.

InvoiceDate: The date the invoice was issued.

CustomerId: Identifier for the customer who made the purchase.

Total: The total amount of the invoice.

Requirements
Complete these steps in the interactive code block:

Select all columns from the Invoices table.

Use the WHERE clause and the BETWEEN keyword to specify a date range for the InvoiceDate column.

Set the range between '2013-11-01' and '2013-12-31'.

Run the query to view the output.

SOLUTION :

SELECT * FROM Invoices WHERE InvoiceDate BETWEEN  '2013-11-01' AND '2013-12-31'



------------------



Challenge 2: Pattern matching
A customer cannot remember the exact title of a song but tells you it has something to do with "Love". You can use pattern matching with the LIKE operator to find track names starting with "Love".

You have the following columns in the Tracks table:

TrackId: Unique identifier for each track.

Name: Name of the track.

AlbumId: Identifier for the associated album.

GenreId: Identifier for the track's genre.

Composer: Composer of the track.

Requirements
Follow these steps in the interactive code block:

Select all columns from the Tracks table.

Use the WHERE clause and the LIKE operator.

Specify the pattern as 'Love%' to filter rows based on pattern matching.

Run the query to view the output.

SELECT * FROM Tracks WHERE Name LIKE 'Love%';


----------