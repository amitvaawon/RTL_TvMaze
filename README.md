# RTL_TvMaze

TVMaze API Documentations

Requirements:
1. scrapes the TVMaze API for show and cast information; 
2. persists the data in storage; 
3. provides the scraped data using a REST API.

Business Requirements:
1. It should provide a paginated list of all tv shows containing the id of the TV show and a list of all the cast that are playing in that TV show.                   
2. The list of the cast must be ordered by birthday descending.                                         
Data Store Process from TvMaze:                                   
URL: http://localhost:51294/api/ShowsCast/StoreShowsCastData                                        
Run once above URL to store the data from TvMaze website to in your local storage.                                
API Details:                        
URL: http://localhost:51294/api/ShowsCast/Get?pageno=1&batchSize=10                         
Parameters: pageno, batchSize (batchSize is no of data per page)                            
Storage: Used JSON file to store the data. We can use SQL server, MySQL, MongoDB, XML etc to store this data.                           
Response:                     
 [{"id":1,"name":"Under the Dome","cast":[{"id":7,"name":"Mackenzie Lintz","birthday":"1996-11-22"},{"id":5,"name":"Colin Ford","birthday":"1996-09-12"},{"id":11,"name":"Britt Robertson","birthday":"1990-04-18"},{"id":8,"name":"Karla Crome","birthday":"1989-06-22"},{"id":35903,"name":"Kylie Bunbury","birthday":"1989-01-30"},{"id":3,"name":"Alexander Koch","birthday":"1988-02-24"},{"id":10,"name":"Natalie Martinez","birthday":"1984-07-12"},{"id":13,"name":"Jolene Purdy","birthday":"1983-12-09"},{"id":1,"name":"Mike Vogel","birthday":"1979-07-17"},{"id":2,"name":"Rachelle Lefevre","birthday":"1979-02-01"},{"id":4,"name":"Eddie Cahill","birthday":"1978-01-15"},{"id":12,"name":"Aisha Hinds","birthday":"1975-11-13"},{"id":9,"name":"Dean Norris","birthday":"1963-04-08"},{"id":14,"name":"Jeff Fahey","birthday":"1952-11-29"},{"id":6,"name":"Nicholas Strong","birthday":"0001-00-01"}]}]
 
If birthday is null then added hardcode value "0001-00-01"                          

Note: If you want frontend to visualize the data, I can Create another web application.                             
