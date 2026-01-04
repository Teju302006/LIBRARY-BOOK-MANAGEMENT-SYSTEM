Introduction

The Library Book Management System is a full-stack web application developed to automate and simplify the process of managing book records in a library environment. The system provides a structured and reliable platform to store, retrieve, update, and delete book information efficiently. By using a modern technology stack consisting of Node.js, Express.js, MongoDB, and React, the application ensures scalability, flexibility, and ease of maintenance. The project emphasizes real-time data handling, proper schema design, and robust error handling mechanisms to ensure data integrity and smooth user interaction.
Project Objectives

The primary objective of this project is to design and implement a reliable library management system that supports complete CRUD operations. The system aims to prevent invalid operations such as negative stock values, handle errors gracefully, and provide an intuitive interface for users. Additionally, the project focuses on demonstrating full-stack development skills, API design principles, and effective database management techniques.
Technologies Used

•  Node.js – JavaScript runtime for backend execution
•  Express.js – Framework for building RESTful APIs
•  MongoDB – NoSQL database for storing book records
•  Mongoose – ODM library for schema definition and database interaction
•  React (Vite) – Frontend library for building dynamic user interfaces
•  Postman – Tool for API testing and verification
•  MongoDB Compass / Shell – Database inspection and direct query testing
•  Visual Studio Code – Development environment

Backend Architecture

The backend of the Library Book Management System was developed using Node.js and Express.js.
•	The backend project was initialized using npm init to generate the package configuration file.
•	Required dependencies such as express and mongoose were installed to handle API routing and database connectivity.
•	A MongoDB database named libraryDB was created, and a books collection was used to store book records.
•	A Mongoose schema was defined with fields such as title, author, category, publishedYear, and availableCopies.
•	Validation rules were applied to prevent invalid data, including negative stock values.
•	RESTful API routes were implemented to handle Create, Read, Update, and Delete operations.
•	The backend server was successfully connected to MongoDB and verified through console logs.

Frontend Architecture

The frontend was developed using React with Vite to ensure faster development and optimized performance.
•	A clean and responsive user interface was designed to display library statistics and book details.
•	Dashboard cards show Total Books and Total Copies in real time.
•	Forms were implemented to allow users to add new books with proper input fields.
•	A tabular view displays all available books with their title, author, category, year, and copies.
•	Buttons were provided to increase or decrease book copies dynamically.
•	A delete option was included to remove books based on backend validation rules.
•	The frontend communicates with backend APIs using fetch / axios to perform CRUD operations.
•	Proper error messages are displayed based on API responses.

CRUD Operations

INSERT OPERATION
•	Book records were inserted using a POST request.
•	A minimum of seven books were added to the database.
•	The request body contained all required fields defined in the schema.
•	The successful insertion was verified through Postman responses and database records.

READ OPERATIONS
a) Retrieve All Books
•	A GET request was used to fetch all book records.
•	The API returned all documents stored in the books collection.
•	Results were verified in Postman and displayed in the frontend.
b) Retrieve Books by Category
•	Books were filtered using category-based queries.
•	The API returned only books matching the specified category.
•	The filtered output was verified using Postman.
c) Retrieve Books Published After 2015
•	A conditional query was applied on the publishedYear field.
•	Books published after the year 2015 were retrieved successfully.
•	The output was verified using Postman.

UPDATE OPERATIONS
a) Increase / Decrease Copies
•	Book copies were updated using PATCH requests.
•	Increment and decrement operations were handled dynamically.
•	Validation ensured that available copies never dropped below zero.
•	Updated values were reflected immediately in the frontend.
b) Change Category
•	Book category was updated using a PATCH request.
•	The category field was modified for a specific book.
•	The updated category was verified in both Postman and frontend UI.

DELETE OPERATION
•	Book deletion was performed using a DELETE request.
•	A book could only be deleted when its available copies were equal to zero.
•	Attempts to delete books with remaining copies were blocked.
•	Successful deletion was verified through Postman and reflected in the frontend.

CRUD OPERATIONS USING MONGODB SHELL

INSERT
•	Multiple book records were inserted using insertMany.
•	MongoDB automatically created the books collection.
•	Inserted documents were verified using find() queries.
READ
•	All books were retrieved using find().
•	Category-based filtering was done using conditional queries.
•	Books published after 2015 were retrieved using comparison operators.
UPDATE
•	Copies were updated using $inc operators.
•	Category updates were performed using $set.
•	All updates were verified using find queries.
DELETE
•	Books were deleted using deleteOne.
•	Deletion was allowed only after setting available copies to zero.
•	Successful deletion was verified in both database and frontend.

Error Handling and Validation
The following error scenarios were tested and verified:
1.	Book Not Found
o	Requests made with invalid or non-existent IDs returned appropriate error messages.
2.	Negative Stock Prevention
o	Attempts to reduce copies below zero were blocked.
3.	Invalid Update
o	Empty request bodies or invalid fields resulted in error responses.
4.	Cannot Delete Book with Available Copies
o	Deletion requests were restricted unless copies were zero.

Conclusion
The Library Book Management System successfully demonstrates a complete full-stack CRUD application using MongoDB, Express, React, and Node.js. All operations were tested through Postman, MongoDB Shell, and verified in the frontend UI.
The project effectively implements schema validation, business rules, and robust error handling. It provides hands-on experience in API development, database design, and frontend-backend integration, making it a strong practical project for academic and real-world applications.
