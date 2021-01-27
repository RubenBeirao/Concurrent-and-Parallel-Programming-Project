# Concurrent-and-Parallel-Programming-Project

A project developed in the second year of my university degree in the scope of the Concurrent and Distributed Programming discipline.

The application to be implemented allows you to use a desktop grid to search for words in a news group. Thus the user must run a client that allows him to enter the words and start the search. 
The client must send this word to the server that will create tasks that are executed by workers. Each task consists in the search of an expression or phrase in the text of a news item. 
The worker must return to the server a list containing all the indexes of the occurrences of the word in the text of the news. After all the tasks have been executed, the server groups the results and sends them to the client. 
The information that the server must send to the client consists of a list with the titles of the news in which the word occurs as well as a list of the indexes of the occurrences for each one of these news. 
After received the titles of the news where the word appears, the client shows the user these results. When the user selects one of the news in the list, the client must send a message to the server requesting the text of the news.

When the server starts it must read all the news that are part of the corpus. These news are in a set of files in a folder that is passed to the server. 
A server when receiving a new search request will create a set of tasks, one to each news item, which consists of seeking the expression in one of the news items.
