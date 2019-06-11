# Skills
## PostgreSQL
- what is it?
  - Relational database
  - Used for my fullstack; declared when creating my project to use postgres as the db locally
## MongoDB
- how is mongoDB implemented into your project?
  - in the root file import mongoose and use the connect function to connec the db to project. DB should include key value pairs of the key to the bucket of your DB
- What are the benefits of a non-relational db?
  - Flexible, if your data is not structured in a certain way, or you didn't plan for it to be structured in a certain way, no biggie; you can scale without thinking about rows/columns
  - Faster, at the expense of ACID compliance.
  - Ease of use, everything is an object
- What are the drawbacks?
  - Cannot join different sets of data; may cost you the speed you gain if you queries to the DB to get the data you need
## React
- What is React?
  - A library that leverages the VirtualDOM to render HTML more efficiently. The virtualDOM would check for any changes and only change the nodes that are affected versus reloading the entire HTML tree
- Benefits?
  - Virtual DOM => makes the user experience better and faster
  - Reusable components => keeps code DRY
  - One-direction data flow => downward data binding ensures children cannot affect their parents (setState)
  - Open-source FB library => constant support
- Drawbacks?
  - High pace development => because there's a lot of support and constant development; programmers must constantly keep up with the new additions
  - Poor documentation => constant development means less documentation; new libraries also must update as well
  - SEO hassle => due to client-side rendering search engines can't index or index poorly on dynamic pages
- Stateless vs stateful?
  - Stateless
    - presentational component => used to display information; does not have state, passed props
  - Stateful => functional component => 
    - logic involved; handling of state (ex. form inputs and storing those inputs); can mutate state (setState)
## Redux
- What is Redux?
  - A library that allows you to create a store that contains the entire state of your app
    - To change the state you must deploy an action that gets traced to the reducer that will return how you want the state returned
## Node.js
- What is Node?
  - run-time environment that includes everything you need to execute a program written in JS
  - event driven, non-blocking I/O model that makes it lightweight and efficient
    - Blocking I/O takes time and blocks other function; one user's info has to be printed before requesting for user 2
    - Non-block I/O allows for multiple requests carried out independently and returning responses at different times
  - allows you to write JS code for the backend
    - makes it highly scalable since you can have a single thread handle multiple requests utilizing the event queue
    - good for data intensive or real-time apps
- How is it implemented into your project?
## Ruby
## Ruby on Rails
- How does the backend interact with the frontend?
  - When the user starts makes a request it'll eventually make an AJAX call. In this call there will be an endpoint that will match a Rails Route. This route will match a controller and return a response to the frontend.
- How does it work? MVC?
## Express
- What is Express?
- How is it implemented?
## MERN Frontend + Backend
- Create the Frontend with React. Backend with Express. Frontend and Backend interact with the use of Axios.
- EX. Fill out form in the frontend. The submit button has an action that gets dispatched with the form data. Inside that action there is an axios call with the post method and the backend endpoint. The backend will return new data that will be passed to the reducer and change the state.
## AWS S3
## How does frontend and backend interact with each other?
- when on a website and a user clicks on a button => the button has a specific action and makes an AJAX call => in this call it has a url that matches a backend route with the type of request it is (POST/GET) => because the request knows what endpoint and method it has, it passes it to the correct controller => the controller returns a JSON object => the frontend determines what to do with the object
## AJAX
- make requests to the server without reloading the page
- receive and work with data from the server
- "asynchrous" in nature
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
- 
## How do you avoid (n + 1) queries?
## What's the benefit to avoiding multiple queries?
- Reduced server load results in smoother user experience
## What is Webpack? What does it do?
- Webpack modularizes code
- Creates a version of your code that different browsers can read
## How does a query find what it's looking for? In PostgreSQL
- 
## What is an API? How do you know what type of API it is?
## How is Google maps API implemented into your project?
## 6 Steps to Usability Concerns
- Record the undesirable outcome
  - Did users make a mistake, not notice an element, take too long to complete a task or fail to complete the task entirely?
- Identify what on the interface is causing the problem
- Is the problem local or global
- Assign a severity rating
- Recommend possible solutions
- Present usability problem

## Difference between HTML & HTML5
- SVG, Canvas & other virtual vector graphics are supported on HTML5
  - on HTML you had to use other technologies in conjunction to make it work like Flash, VML & Silver-light
- HTML5 uses web SQL databases, application cache for temporary storage data
  - HTML only used browser cache
- HTML5 allows JavaScript to be run within the browser
- HTML5 supports new form controls (ex. date, times, email, number, tel, url)
- HTML5 introduces new elements like(summary, time aside, audio, command, data, and more) 
  - makes the HTML more semantic
### Pros of HTML5
- Persistent error handling
  - browsers have support to parse structurally/syntatically incorrect HTML code
- Improved semantic elements
- Mobile web made easier
  - more mobile support with HTML5
- The canvas element
  - can completely replaces Flash
- The menu element
  - semantic way of creating a menu
- Cookies
  - Local storage was added in HTML5. Before in HTML4, devs would have to use cookies
  - Local storage is an object (localStorage) that is available on the global window
### End user Advantages for HTML5
- Mobile browsers crash a lot less
- More reliable mobile websites
- The removal of Adobe Flash will now give developer the ability to create graphic-rich UX
- Ability to support native audio and video elements
  - Users will not have to download plugins to view media on a website
  
## CSS vs CSS3
- Added: Modules => which allow designing to be done in less time with more ease while updating indvidual features
  - 4 Big modules are: Color, Selector, Namespaces, and Media Queries
    - The most important is probably media queries which allow applications of certain conditions to have certain style sheets
ex.
```css
@media screen and (max-width: 600px) {
    background: #FFFFFF;
}

@media screen and (min-width: 600px) and (max-width: 900px) {
    background: #FFFFFF;
}
```
- vendor prefixes => help browsers interpret code
  - -moz- : Firefox
  - -webkit- : Webkit browsers like Apple Safari and Google Chrome
  - -o- : Opera
  - -ms- : Internet Explorer
- added pseudo-classes
- new css properties: 
  - rounded borders
    - new border properties
  - text shadow
  - adding columsn easier
  - add multiple backgrounds
## W3C Compliant Website
- HTML and CSS code that are compliant with the standards set by the World Wide Web Consortium
  - Web Design & Applications, Web of Devices, Web Architecture, Semantic Web, XML Technology, Web of Services, Browsers and Authoring Tools
- You can use a [W3C validator tool](https://validator.w3.org/) to check if your website is compliant
- W3C compliance is extremely strict and will most often throw up an error regardless if your website loads fine on the browser
  - browsers are generally flexiable and are built to handle a wide range of HTML & CSS code
- With a W3C compliant website web crawlers are able to read your website better making for better SEO. Although 100% is often difficult to achieve as long as your code is structured well 100% is not necessary for optimized SEO.
