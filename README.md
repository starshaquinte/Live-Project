# Live-Project
Code Summary of my Live Project


  '''

@model IEnumerable<TheatreCMS3.Areas.Prod.Models.CalendarEvents>

@{
    ViewBag.Title = "Index";
    Layout = "~/Views/Shared/_Layout.cshtml";
}

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
