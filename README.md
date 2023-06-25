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


<h4>Styling the Homepage</h4> 
The home page was pretty empty and needed some content. I added the logo under the navbar. Created two columns of content under the logo.
Created a section called Spotlight in the left column, to display upcoming events. Utilized production posters to fill this area.
Created a section called Donations with a button that says 'Click to Support' that links to the Donation page. Created a section called 
Sponsors in the right column displaying all 5 sponsors. The Land Acknowledgement section includes details about the land the theatre
sits on. The NAYA photo links to https://nayapdx.org/ on a separate tab.





'''
<h2>Index</h2>

<p>
    @Html.ActionLink("Create New", "Create", null, new { @class = "CalendarEvents--Index--CreateButton btn btn-default" })
</p>
<table class="table">
    <tr>
        <th>
            @Html.DisplayNameFor(model => model.Title)
        </th>
        <th>
            @Html.DisplayNameFor(model => model.StartDate)
        </th>
        <th>
            @Html.DisplayNameFor(model => model.EndDate)
        </th>
        <th>
            @Html.DisplayNameFor(model => model.StartTime)
        </th>
        <th>
            @Html.DisplayNameFor(model => model.EndTime)
        </th>
        <th>
            @Html.DisplayNameFor(model => model.AllDay)
        </th>
        <th>
            @Html.DisplayNameFor(model => model.TicketsAvailable)
        </th>
        <th>
            @Html.DisplayNameFor(model => model.IsProduction)
        </th>
        <th>
            @Html.DisplayNameFor(model => model.Description)
        </th>

    </tr>

    @foreach (var item in Model)
    {
        <div class="container">
            <div class="row row-striped">
                <div class="col-2 text-right">
                    <h1 class="display-4"><span class="badge badge-secondary">@item.StartDate.Day</span></h1>
                    <h2>@item.StartDate.ToString("MMMM")</h2>
                </div>
                <div class="col-10">
                    <h3 class="text-uppercase"><strong>@item.Title</strong></h3>
                    <ul class="list-inline">
                        <li class="list-inline-item"><i class="fa fa-calendar-o mr-2" aria-hidden="true"></i>@item.StartDate.DayOfWeek</li>
                        <li class="list-inline-item"><i class="fa fa-clock-o mr-2" aria-hidden="true"></i>@item.StartTime</li>
                    </ul>
                    <p>@item.Description</p>
                    <hr>
                </div>
            </div>
        </div>
        @Html.DisplayFor(modelItem => item.Title)

        <td>
            @Html.DisplayFor(modelItem => item.StartDate)
        </td>
        <td>
            @Html.DisplayFor(modelItem => item.EndDate)
        </td>
        <td>
            @Html.DisplayFor(modelItem => item.StartTime)
        </td>
        <td>
            @Html.DisplayFor(modelItem => item.EndTime)
        </td>
        <td>
            @Html.DisplayFor(modelItem => item.AllDay)
        </td>
        <td>
            @Html.DisplayFor(modelItem => item.TicketsAvailable)
        </td>
        <td>
            @Html.DisplayFor(modelItem => item.IsProduction)
        </td>
        <td>
            @Html.DisplayFor(modelItem => item.Description)
        </td>
        <td>
            @Html.ActionLink("Edit", "Edit", new { id = item.EventId }) |
            @Html.ActionLink("Details", "Details", new { id = item.EventId }) |
            @Html.ActionLink("Delete", "Delete", new { id = item.EventId })
        </td>

    }

</table>
'''
