# Live-Project
Code Summary of my Live Project

<h3>Introduction</h3>

During my final two weeks at the Tech Academy, I collaborated with a team of peers to enhance a theater company's website using ASP .NET MVC and Entity Framework. The project had already been completed, and my task involved transforming the content into an interactive format that allowed users to manage the theater's productions.

To streamline the development process, I leveraged Bootstrap to create visually appealing and responsive webpages for the theater website. Responsive design plays a crucial role in modern web development as it ensures an optimal user experience across various devices. Throughout the project, I tackled a range of frontend and backend tasks, each with its own level of complexity.

Included below are descriptions of the specific tasks I worked on, accompanied by relevant code snippets. Additionally, this repository contains complete code files for larger functionalities that I implemented.

**Features:** Technologies used in the Live Project include C#, ASP.Net Framework, Razor syntax, HTML, CSS, JavaScript and Entity Framework

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

'''


    <div class="container CalendarEvents-create-container">
    <div class="form-horizontal CalendarEvents-create-container">
        <h3><b>CalendarEvents</b></h3>
        <hr />
        @Html.ValidationSummary(true, "", new { @class = "text-white" })
        @Html.HiddenFor(model => model.EventId)

        <div class="form-group">
            @Html.LabelFor(model => model.Title, htmlAttributes: new { @class = "control-label col-md-2" })
            <div class="col-md-10">
                @Html.EditorFor(model => model.Title, new { htmlAttributes = new { @class = "form-control CalendarEvents-Create-input" } })
                @Html.ValidationMessageFor(model => model.Title, "", new { @class = "text-danger" })
            </div>
        </div>

        <div class="form-group">
            @Html.LabelFor(model => model.StartDate, htmlAttributes: new { @class = "control-label col-md-2" })
            <div class="col-md-10">
                @Html.EditorFor(model => model.StartDate, new { htmlAttributes = new { @class = "form-control CalendarEvents-Create-input" } })
                @Html.ValidationMessageFor(model => model.StartDate, "", new { @class = "text-danger" })
            </div>
        </div>

        <div class="form-group">
            @Html.LabelFor(model => model.EndDate, htmlAttributes: new { @class = "control-label col-md-2" })
            <div class="col-md-10">
                @Html.EditorFor(model => model.EndDate, new { htmlAttributes = new { @class = "form-control CalendarEvents-Create-input"} })
                @Html.ValidationMessageFor(model => model.EndDate, "", new { @class = "text-danger" })
            </div>
        </div>

        <div class="form-group">
            @Html.LabelFor(model => model.StartTime, htmlAttributes: new { @class = "control-label col-md-2" })
            <div class="col-md-10">
                @Html.EditorFor(model => model.StartTime, new { htmlAttributes = new { @class = "form-control CalendarEvents-Create-input" } })
                @Html.ValidationMessageFor(model => model.StartTime, "", new { @class = "text-danger" })
            </div>
        </div>

        <div class="form-group">
            @Html.LabelFor(model => model.EndTime, htmlAttributes: new { @class = "control-label col-md-2" })
            <div class="col-md-10">
                @Html.EditorFor(model => model.EndTime, new { htmlAttributes = new { @class = "form-control CalendarEvents-Create-input" } })
                @Html.ValidationMessageFor(model => model.EndTime, "", new { @class = "text-danger" })
            </div>
        </div>

        <div class="form-group">
            @Html.LabelFor(model => model.AllDay, htmlAttributes: new { @class = "control-label col-md-2",  })
            <div class="col-md-10">
                <div class="checkbox">
                    @Html.EditorFor(model => model.AllDay)
                    @Html.ValidationMessageFor(model => model.AllDay, "", new { @class = "text-danger" })
                </div>
            </div>
        </div>

        <div class="form-group">
            @Html.LabelFor(model => model.TicketsAvailable, htmlAttributes: new { @class = "control-label col-md-2" })
            <div class="col-md-10">
                @Html.EditorFor(model => model.TicketsAvailable, new { htmlAttributes = new { @class = "form-control CalendarEvents-Create-input" } })
                @Html.ValidationMessageFor(model => model.TicketsAvailable, "", new { @class = "text-danger" })
            </div>
        </div>

        <div class="form-group">
            @Html.LabelFor(model => model.IsProduction, htmlAttributes: new { @class = "control-label col-md-2" })
            <div class="col-md-10">
                <div class="checkbox">
                    @Html.EditorFor(model => model.IsProduction)
                    @Html.ValidationMessageFor(model => model.IsProduction, "", new { @class = "text-danger" })
                </div>
            </div>
        </div>

        <div class="form-group">
            @Html.LabelFor(model => model.Description, htmlAttributes: new { @class = "control-label col-md-2" })
            <div class="col-md-10">
                @Html.EditorFor(model => model.Description, new { htmlAttributes = new { @class = "form-control CalendarEvents-Create-input" } })
                @Html.ValidationMessageFor(model => model.Description, "", new { @class = "text-danger" })
            </div>
        </div>

        <div class="form-group">
            <div class="col-md-offset-2 col-md-10">
                <input type="submit" value="Save" class="btn btn-default CalendarEvents-create-button" button style="background-color:#bd1a11;" />
                @Html.ActionLink("Back to List", "Index", null, new { @class = " CalendarEvents--CreateEdit--CreateButton btn btn-default" })
            </div>
            </div>
        </div>
    </div>







<h3>Back End Stories</h3>

[Model for CalendarEvent and CRUD pages](https://github.com/starshaquinte/Live-Project/blob/main/ModelforCalendarEventandCRUDpages.txt)

[Style CRUD Pages Part 2: Index Page for Calendar Event](https://github.com/starshaquinte/Live-Project/blob/main/Style%20CRUD%20Pages%20Part%202.txt)

<h4>Create entity model for CalendarEvent and CRUD pages</h4>
Created an entity model for the Calendar Event class so that productions can be saved to the database. First I created the model with
the "?" indicating that a property is nullable. After creating the model I updated the database to create a table in the database. Utilized 
SQL Server Object Explorer in Visual Studio to check that the table was created correctly. After creating the model, I was tasked with 
scaffolding the CRUD pages, CRUD follows a simple functionality: Create, Read, Update, Delete. Utilized Visual Studio and EntityFramework
to create the Index, Edit, Create, Details, and Delete pages).

<h4>Style CRUD Pages Part 2: Index Page for Calendar Event</h4>
Created a button using the 'create new' link. Styled the calendar events to be displayed more like a calendar and less like a table. The
Calendar displays the month and day of the event followed by the start time and end time. Also added a description box to include details
of the event. 

<h3>Other Skills Learned</h3>

- Gained an understanding and utilized of version control in Azure DevOps.
- Aquired skills with Git, I was able to maintain a local copy of the entire project, enabling me to work independently.
- Gained experience utilizing MVC Basics, the main functions into 3 groups: the model, the controller, and the view.
- Gained experience utilizing Agile framework, participated in Scrum, Daily standups and Code retrospective





