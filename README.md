Permalist Application

Permalist is a simple to-do list application built with Express.js and PostgreSQL. It allows users to add, edit, and delete tasks in real time, with a modern and responsive design. 

Features 

Add Tasks: Users can create new tasks. 

Edit Tasks: Users can edit existing tasks. 

Delete Tasks: Users can delete tasks when completed. 

Persisted Storage: All tasks are stored in a PostgreSQL database, ensuring data is retained across sessions. 

Project Structure 

The project has a front-end and back-end structure with the following files: 

Front-end 

public/styles/main.css: Main CSS for styling the to-do list. 

views/index.ejs: Main view for rendering the list of tasks. 

views/partials/header.ejs & views/partials/footer.ejs: Reusable components for the page header and footer. 

Back-end 

index.js: Main server file, handling all routes and database interactions. 

Installation 

Clone the repository: 

bash 

Copy code 

git clone https://github.com/yourusername/permalist.git 
cd permalist 
 

Install dependencies: 

bash 

Copy code 

npm install 
 

Set up PostgreSQL database: 

Create a PostgreSQL database named permalist. 

Add a table named items with the following structure: 

sql 

Copy code 

CREATE TABLE items ( 
  id SERIAL PRIMARY KEY, 
  title VARCHAR(255) NOT NULL 
); 
 

Configure database: 

Update the database credentials in index.js if necessary: 

js 

Copy code 

const db = new pg.Client({ 
  user: "postgres", 
  host: "localhost", 
  database: "permalist", 
  password: "1234", 
  port: 5432, 
}); 
 

Run the application: 

bash 

Copy code 

npm start 
 

Access the application: Open your browser and navigate to http://localhost:3000. 

Usage 

Add a task: Type the task name in the input field and click the + button. 

Edit a task: Click the pencil icon next to the task, make edits, and submit. 

Delete a task: Check the box next to the task to delete it. 

 
