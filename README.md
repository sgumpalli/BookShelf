# BookShelf

1) User Management
2) Shelf
3) Books
4) Search
5) Conversations

Spring boot, hibernate, Angular JS, node js

Entities: User,  Book, Shelf, Conversation

Services: 

1) User Services 
•	createUser
•	updateUser
•	deleteUser
•	getUser
2) Book
•	addBook
•	shareBook
•	deleteBook
•	updateBook
3) Shelf
•	addBookToShelf
•	deleteBookFromShelf
•	getBookInfoInShelf

4) Search
•	searchBook
5) Conversation
•	getUserConversations
•	getConversation
•	sendMessageToUser

Plan
	25/05 : ER diagram


User Shelf scenarios: (28/05/2016)
1)	User can have his own books but not shared yet
2)	User can have his own books shared with public
3)	User can have books of his interest shared by others 
Question is how we can display all 3 types in only one place for user called Shelf ?
1)	We can give different colored tick marks for each category and display them under one single shelf without any line gap between each type. That means all in one with colored tick marks
•	Can sort based on the color i.e. type
•	Can sort based on name, date, zoner, size etc;
Pros:
•	Can see all types at one place without any gaps or something.
Cons:
•	Little confusion with colors. 
•	Seems not properly ordered.

2)	We can give different colored tick marks for each category and display them under one single shelf with line separation between each type and type names as headers. That means different sections with colored tick marks.
•	Can sort based on the color i.e. type
•	Can sort based on name, date, zoner, size etc;
Pros:
•	Beautifully organized
Cons:
•	Don’t know till now

So as of now, decided to go with second approach – 28/05/2016

Thumb rule – Same User cannot upload a book with same name, author and zoner. -  28/05/2016

Uploading a book (flow):  (28/05/2016)
1)	Go to upload book page
2)	Add book image and fill details like name, author, zoner(required fields), share with others(optional).
3)	Click on upload and then book will be added into Shelf scenario 1 if share with others is not checked OR Shelf scenario 2 if share with others is checked
4)	Done
Contact Disclosure Scenarios: (28/05/2016)
1)	User would like to display his/her contact info to the public
2)	User would like to display his/her contact info to specific user
3)	User would like to hide the contact info.
Search and Add to Shelf (flow):  (28/05/2016)
1)	Search bar is placed in the User Home page after logging in.
2)	When user types something in the search bar, it should search in title, author, zoner.
3)	It should show results in proper order
4)	Filtering the search results is very important
5)	Results:
a)	Thumbnail image, Title, Author, Zoner, Shared User, Add to Shelf, Contact Person. When Add to Shelf is clicked book should be added to user’s shelf mentioned in shelf scenario 3. When Contact Person is clicked, a popup should be opened which will display contact info as per book owner’s Contact Disclosure Scenario.

