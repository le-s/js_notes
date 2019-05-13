# Skills
## PostgreSQL
- what is it?
## MySQL
- what experience do you have with MySQL?
## MongoDB
- how is mongoDB implemented into your project?
- What experience do you have with this?
- What is MongoDB?
- What are the benefits of a non-relational db?
- What are the drawbacks?
## React
- What is React?
- Benefits?
- Drawbacks?
- Stateless vs stateful?
  - Stateless
    - presentational component => used to display information; does not have state, passed props
  - Stateful => functional component => 
    - logic involved; handling of state (ex. form inputs and storing those inputs); can mutate state (setState)
## Redux
- What is Redux?
## Node
- What is Node?
- How is it implemented into your project?
## Ruby
## Ruby on Rails
- How does the backend interact with the frontend?
- How does it work? MVC?
## Express
- What is Express?
- How is it implemented?
## AWS S3
## How does frontend and backend interact with each other?
- when on a website and a user clicks on a button => the button has a specific action and makes an AJAX call => in this call it has a url that matches a backend route with the type of request it is (POST/GET) => because the request knows what endpoint and method it has, it passes it to the correct controller => the controller returns a JSON object => the frontend determines what to do with the object

# Flex-o
## Single page application vs multi-page application?
- Multi Page
  - Traditional web apps that reload an entire page and displays a new one
  - Pros: 
    - Performs well on search engines
    - Provides a visual map of the web app to the user
  - Cons:
    - Complex development
    - Coupled backend and frontend
- Single Page
  - Consists of a single page; faster because logic is executed on the web browser vs on the server
  - After the page is loaded, only data is sent back and forth vs the entire HTML
  - Pros:
    - Smooth and fast UX
    - Easier to develop and deploy
    - Easier to debug => not sure why
    - Can be transitioned to mobile by reusing the same backend code
  - Cons: 
    - Perform poor on search engines, but with isomorphic/server-side rendering can utilize SEO as well
    - Provide a single sharing link
    - Less secure than Multi page applications due to cross-site scripting
## How is Postgres implemented into your project?
- it is setup when you create your project, setting what you want your DB to be
- there are databases for different environments (test, development, production)
  - you can set a DB for each of these environments
- incorporated in the YAML file of the project directory, usually "database.yml"
  - database.yml is used by rails to connect the appropriate database to the Rails environment
- DB have tables and rows, Rails has models(classes) & objects
  - use rails g migration {tableName} to create a table => add column names after => rails db:migrate to create the table
  - then create the model for assocications 
## How do you implement AWS S3 into your project?
## How do you avoid (n + 1) queries?
## What's the benefit to avoiding multiple queries?
## How does a query find what it's looking for? In PostgreSQL

## What is an API? How do you know what type of API it is?
## How is Google maps API implemented into your project?
