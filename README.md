# CQRS command query responsibily segregation

This is a practical example of the concepts and principles of CQRS (Command and Query Responsibility Segregation)

where I use docker to create images of a database in PostgreSQL and mongoDB

one for reading and one for writing, as we already know one of the typical problems in a relational database will be reading data since it will make at least two queries to different tables and a join to unite them, therefore a non-relational database It will fetch all the data in a shorter period of time, but the writing will be slower since the document to be saved will be developed.

We have 4 options immediate consistency with synchronous methods to insert updated information in two different databases so it will be an even slower process, the second is eventual consistency with asynchronous method where the information will be inserted but not updated immediately, the The third is scheduled consistency where we can update the data in a defined section either one hour a day or once a week and the fourth is consistency on demand where we would synchronize in a required situation or event, the most recommended is eventual consistency.

In this small project you can also see how to perform the synchronization, how to separate the query stack from the command stack and you will notice that the models are different in the definition of the read or write request.
