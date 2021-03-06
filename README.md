# Twitter-Streaming-
A REST API that streams Twitter data and stores them in a database.

Twitter Streaming API was used to stream tweets and their metadata in real time. The search is based on some keywords and the user can limit the number of tweets to be extracted. The tweets are stored in a database (NoSQL).

The stored data can be accessed through some built-in queries.

The data can also be exported as a csv file on the local machine.

Sorting (ascending/descending) can be specified at the time of accessing data. Pagination is also implemented.

The implemented functionalities are:-

1. Stream_Data - This class streams Twitter data and stores them in a database. 
   It takes 2 arguments:
   1. hash-tag: The tweets pertaining to this keyword are streamed.
   2. count: The number of tweets to be streamed and stored.
   
   eg. <ip_address>/stream_data/car/10

2. Get_Data - This class gets the data stored in the database.
   It takes 2 arguments:
   1. sort_by: The cloumn by which the data should be sorted.
   2. order: The order in which you want the data to be sorted (ascending/descending).
   
   eg. <ip_address>/get_data/tweet/asc
   
3. Filter_Integer: This class filters the data stored based on the integer columns with sorting.
   It takes 5 arguments.
   1. integer: The column to filter the data by.
   2. operator: (<, =, >)
   3. number: The number by which to filter.
   4. sort_by: The cloumn by which the data should be sorted.
   5. order: The order in which you want the data to be sorted (ascending/descending).

   eg. 

4. Filter_String: This class filters the data stored based on the string columns with sorting.
   It takes 5 arguments.
   1. column: The column to filter the data by.
   2. pos: ('ends with', 'contains', 'starts with').
   3. search_text: The text by which to filter.
   4. sort_by: The cloumn by which the data should be sorted.
   5. order: The order in which you want the data to be sorted (ascending/descending).
   
   eg. <ip_address>/filter_string/name/contains/a/followers/asc
   
5. Filter_Date: This class filters the data stored based on a date range with sorting.
   It takes 4 arguments.
   1. date1: Starting date
   2. date2: ending date
   3. sort_by: The column by which the data should be sorted.
   4. order: The order in which you want the data to be sorted (ascending/descending).
   
   eg. <ip_address>/filter_date/2018-10-04/2018-10-05/friends/desc
 
6. Export_CSV: This class exports the database as a csv file on the local machine.
   
   eg. <ip_address>/export_csv
   
7. Get_Count: This class returns the total number of tweets stored in the database.
   
   eg. <ip_address>/get_count

NB. I have also completed the assignment for SDE(Applications) profile. The project can be accessed through https://github.com/DivyaSanjay/Medical-API
