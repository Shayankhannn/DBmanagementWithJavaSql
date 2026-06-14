Challenge 1: Calculate average track length by genre
Now it’s your turn! You want to find the average length of tracks for each genre to understand how long tracks typically are in each category.

You have the following columns in the Tracks table:

TrackId: Unique identifier for each track.

GenreId: Identifier for the track's genre.

Milliseconds: The duration of the track is in milliseconds.

Requirements
Complete these steps in the interactive code block:

Use the SELECT statement to retrieve the GenreId and use the AVG(Milliseconds) function to calculate the average length of tracks for each genre.

Use the FROM keyword to specify the Tracks table.

Use the GROUP BY clause to group the results by the GenreId column.

Run the query to view the output.


SOLUTION :

SELECT GenreId , AVG(Milliseconds) FROM Tracks 
GROUP BY GenreId;

--------------------------------------


Challenge 2: Count Tracks based on media type
What if you want to determine the number of tracks stored in each media type, such as MPEG or protected AAC? You can use the GROUP BY clause to group tracks by their media type and then count the number of tracks for each type.

You have the following columns in the Tracks table:

TrackId: Unique identifier for each track.

MediaTypeId: Identifier for the track's media type.

Requirements
Complete these steps in the interactive code block:

Use the SELECT statement to retrieve the MediaTypeId with COUNT(*) to count the number of tracks in each media type.

Use the FROM keyword to specify the Tracks table.

Use the GROUP BY clause to group the results by the MediaTypeId column.

Run the query to view the output.

SELECT MediaTypeId, COUNT(TrackId) FROM Tracks 
GROUP BY MediaTypeId;


-----------------------------------


Challenge 3:  Combine grouping by genre and composer
What if you want to find out how many tracks are available for each combination of genre and composer? This can provide deeper insights into which composers are most active in each genre.

You have the following columns in the Tracks table:

TrackId: Unique identifier for each track.

GenreId: Identifier for the track's genre.

Composer: Composer of the track (nullable).

Requirements
Complete these steps in the interactive code block:

Use the SELECT statement to retrieve the GenreId and Composer, and use COUNT(*) to count the number of tracks for each combination.

Use the FROM keyword to specify the Tracks table.

Use the GROUP BY clause to group the results by both the GenreId and Composer columns.

Run the query to view the output.

SOLUTION :

SELECT GenreId ,Composer , COUNT(TrackId) FROM Tracks
GROUP BY GenreId,Composer;