# Live-Project
Code Summary of my Live Project

<h5>Introduction</h5>

During my last two weeks at the tech academy, I worked on a team with peers developing using ASP .NET MVC and Entity Framework.
This project was previously completed and I was responsible for updating content to be interactive and enable its users to manage
the content and productions for a theater company.

Throughout the Live project I saved time by utilizing Bootstrap to create responsive and visually appealing webpages for the theater website.
Responsive design is an essential aspect of modern web development, as it ensures that the website can adapt and provide optimal user experience
regardless of device. I worked on several front end and back end stories of all varying degrees of difficulty.

Below are descriptions of the stories I worked on, along with code snippets. I also have some full code files in this repo for larger
funtionalities I implemented.

<h3>Front End Stories</h3>

[Styling the Homepage](https://github.com/starshaquinte/Live-Project/blob/main/StyleHomePage.html)

[Style CRUD Pages Part 1: Style the Create and Edit Pages for Calendar Event model](https://github.com/starshaquinte/Live-Project/blob/main/StyleCRUDPagesPart1.html)


<h4>Styling the Homepage</h4> 
The home page was pretty empty and needed some content. I added the logo under the navbar. Created two columns of content under the logo.
Created a section called Spotlight in the left column, to display upcoming events. Utilized production posters to fill this area.
Created a section called Donations with a button that says 'Click to Support' that links to the Donation page. Created a section called 
Sponsors in the right column displaying all 5 sponsors. The Land Acknowledgement section includes details about the land the theatre
sits on. The NAYA photo links to https://nayapdx.org/ on a separate tab.

<h4>Style CRUD Pages Part 1: Style the Create and Edit Pages for Calendar Event model</h4>
The Create and Edit pages were scaffolded but not styled. I added the header "Create Calendar Event" and styled the buttons using the website's
color theme.  I also ensured all buttons below the form were aligned. I added placeholders to all input fields and added a feature that would 
change the color when clicked. Finally, I placed the form in a centered container 


<h3>Back End Stories</h3>

[Model for CalendarEvent and CRUD pages](https://github.com/starshaquinte/Live-Project/blob/main/ModelforCalendarEventandCRUDpages.txt)

<h4>Create entity model for CalendarEvent and CRUD pages</h4>
Created an entity model for the Calendar Event class so that productions can be saved to the database. First I created the model with
the "?" indicating that a property is nullable. After creating the model I updated the database to create a table in the database. Utilized 
SQL Server Object Explorer in Visual Studio to check that the table was created correctly. After creating the model, I was tasked with 
scaffolding the CRUD pages, CRUD follows a simple functionality: Create, Read, Update, Delete. Utilized Visual Studio and EntityFramework
to create the Index, Edit, Create, Details, and Delete pages).

[Style CRUD Pages Part 2: Index Page for Calendar Event]





