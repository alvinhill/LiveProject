# LiveProject  Introduction
## Part One Style Home Page
My first assignment was to completely format and style the Home page of a theater company site.  I had to setup the page to display the production posters for the plays.  There was also a section setup to solicit donations from the patrons.   Another section was to display awards received by the productions.  Lastly a large footer was to be created to acknowledge the involvement of the local Native American tribe for their contribution.  

My first challenge was to decide which tool to use.  I found a very useful video on utube for tables that provide a method to do most of the project.  The dimensions of the tables were specific to 70% on the poster side.  I had to be able to divide spaces inside of the of a tables to place the requested items according to the example I was given.

## Home Page Code
@{
    ViewBag.Title = "Home Page";
}

<!--       Main Page Section-->

<div class="logo">

    <img src="~/Content/images/TheatreLogo.png" alt="logo" style="display: block;margin-left: auto;margin-right: auto;" />
</div>
<div class="info">

    <table align="center" border="0" width="500" height="400">
        <tr>
            <th style="width: 70%;"><p class="MOtext">SPOTLIGHT</p></th>
            <th style="width:30% ;"><p class="MOtext"> DONATIONS </p> </th>
        </tr>
        <tr>
            <td><img src=~/Content/images/DollsHouse.png alt="block" width="350" height="200"></td>
            <td>
                <input type="button" value="Click to Support" onclick="window.location.href='@Url.Action("Donate", "Home")';" />

                <table border="0" width="150" height="30">
                    <tr>
                    <td>  <p class="MOtext">SPONSORS</p>  </td>
                    </tr>
                </table>

                <table border="0" width="150" height="30">
                    <tr>
                        <td> <img src=~/Content/images/Sponsors/OCF-logo-in-white-with-tagline-lg.png alt="block" width="60" height="30"></td>
                    </tr>
                </table>
                <table border="0" width="150" height="30">
                    <tr>
                        <td> <img src=~/Content/images/Sponsors/LogoRoundColor.png alt="block" width="30" height="30"></td>
                        <td> <img src=~/Content/images/Sponsors/LogoRoundColor.png alt="block" width="30" height="30"></td>
                        <td><img src=~/Content/images/Sponsors/Ellyn-Bye-Logo.png alt="block" width="50" height="30"></td>
                    </tr>
                </table>
                <table border="0" width="150" height="30">
                    <tr>
                        <td><img src=~/Content/images/Sponsors/OCF-logo-in-white-with-tagline-lg.png alt="block" width="50" height="30"></td>
                    </tr>
                </table>
                <table border="0" width="150" height="30">
                    <tr>
                        <td><img src=~/Content/images/Sponsors/RACC.png alt="block" width="50" height="30"></td>
                    </tr>
               </table>
            </td>
        </tr>
        <tr>
            <td>
                <img src=~/Content/images/Tempest.png alt="block" width="350" height="400">
            </td>
            <td>
            </td>
            <td></td>
        </tr>
        <tr>
            <td><img src=~/Content/images/MidsummerNightDream.png alt="block" width="350" height="400"></td>
        </tr>
        <tr>
            <td><img src=~/Content/images/macbeth.png alt="block" width="350" height="400"></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
        </tr>
    </table>
</div>

<!--    Land Use Section -->

<div class="info">

    <table class="infoX" align="center" border="0" width="800" height="15" cellpadding="8">
        <tr>
            <th style="width: 70%;"><p class="LM">  Land Acknowledgment</p></th>
            <th style="width:30% ;"></th>
        </tr>
        <tr>
            <td>
                <p>
                    Theater Vertigo humbly acknowledges we live and work on the unceded, traditional
                    Tribal lands of the Multnomah, Wasco, Clackamas. Chinook bands, KathLamet, Tualatin
                    Kalapuya, Cowtitz, Mollala, Cascades, Oregan City Tumwater, Confederated Tribes of
                    The Grand Ronde and other indigenous peoples.
                </p>
                <p>
                    We are on stolen Land.

                    Theater Vertigo hac been and continues to examine our community relationships to
                    Ensure our collaborator, partners and sponsors support our regions Indigenous Nations and communities.

                    One of the ways Theater is working to act on hour commitment to being of service to the
                    Lands that we now share is to build bridges between our arts community and local Nations.
                </p>
            </td>

            <!--    Footer Section         -->

            <td>
                <p>
                    <a href="https://www.nayapdx.org/">
                    <img src="/Content/images/NAYAFamilyCenter.jpg" />
                    </a>
                </p>
            </td>
        </tr>
        <tr>
            <td></td>
            <td>
                <p>
                    Click to visit the NAYA Family Center to learn more
                    about supporting our local indigenous communities.
                </p>
            </td>
        </tr>
    </table>
</div>

## Create CRUD Database
The second Live project was to create a C.R.U.D. database.  The project was to use Entity Framework to create the database using the “code first” method.  
I was able to create the class with the appropriate properties and the correct data types.  

We were asked to not create a new dbContext class and use the current Layout file.

I ran into a bug by getting an error when trying to generate the database.  My code was good so the instructor found that someone had left field with a conflicting primary key from the time that person worked on the project.                                                           

## Database Code
  using System;
using System.Collections.Generic;
using System.ComponentModel.DataAnnotations;
using System.Linq;
using System.Web;

namespace TheatreCMS3.Areas.Prod.Models
{
    public class CalendarEvent
    {
        [Key]
        public int EventId { get; set; }
        public string Title { get; set; }

        public DateTime StartDate { get; set; }
        public DateTime EndDate { get; set; }

        public bool AllDay { get; set; }
        public int TicketsAvailable { get; set; }
        public bool IsProduction { get; set; }
    }
}

## Format Create and Edit (shared) Layout
For my third live project assignment, I was tasked with customize the user interface based on specific written instructions.  This included styling the buttons, aligning the buttons and using placeholders.  This Create and Edit pages were initially constructed using bootstrap so that is what I used to integrate my work into project.

Placeholders were required for the input fields.  The title and the data entry boxes needed to be centered.

Mainly done with bootstrap with some css.  A limited color scheme was required and was easily implemented.  

My initial challenge was to realize that bootstrap would be the primary tool css would play a minor role.
My second challenge was to identify the correct selector for the css that I did use.  I have not seen the particular variety of code.  It was peppered with lambda, html, some C# class assignments and MVC classes.   However, was able make sense of it and complete the project.

## Format Code
@model TheatreCMS3.Areas.Prod.Models.CalendarEvent

@{
    ViewBag.Title = "";
    Layout = "~/Views/Shared/_Layout.cshtml";
}


@using (Html.BeginForm())
{
    @Html.AntiForgeryToken()
 

<div class="d-lg-flex flex-column vertical-box align-items-center bg-danger" >

   
        <h4>Create CalendarEvent</h4>
        <hr />
        @Html.ValidationSummary(true, "", new { @class = "text-danger" })

        <div class="form-group">
            @Html.LabelFor(model => model.Title, htmlAttributes: new { @class = "control-label col-md-2 mx-auto" })
            <div class="col-md-10">
                @Html.EditorFor(model => model.Title, new { htmlAttributes = new { @class = "form-control", placeholder = "Title" } })
                @Html.ValidationMessageFor(model => model.Title, "", new { @class = "text-danger" })
            </div>
        </div>
  
    <div class="form-group">
        @Html.LabelFor(model => model.StartDate, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">
            @Html.EditorFor(model => model.StartDate, new { htmlAttributes = new { @class = "form-control", placeholder = "Start Date" } })
            @Html.ValidationMessageFor(model => model.StartDate, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.EndDate, htmlAttributes: new { @class = "control-label col-md-2" })
        <div class="col-md-10">

            @Html.EditorFor(model => model.EndDate, new { htmlAttributes = new { @class = "form-control", placeholder = "End Date" } })
            @Html.ValidationMessageFor(model => model.EndDate, "", new { @class = "text-danger" })
        </div>
    </div>

    <div class="form-group">
        @Html.LabelFor(model => model.AllDay, htmlAttributes: new { @class = "control-label col-md-2" })
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
            @Html.EditorFor(model => model.TicketsAvailable, new { htmlAttributes = new { @class = "form-control", placeholder = "Tickete Available" } })
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
        <div class="col-md-offset-2 col-md-10">
            <input type="submit" value="Create" class="btn" />
        </div>
    </div>
</div>
    }

<div>
    @Html.ActionLink("Back to List", "Index")
</div>

@section Scripts {
    @Scripts.Render("~/bundles/jqueryval")
}


## Css for Layout

/* ▼ This ▼ is for you to easily reference the colors on the Site.css page */
/* Do not uncomment these color variables */

/* CSS color variables */
:root { /* Color palette for css */
--main-color: #BD1A11; /* Red */
--main-color--light: #F04D44; /* Red, a shade lighter */
--secondary-color: #D6972A; /* Yellow gold */
--light-color: #FFFBFB; /* White */
--dark-color: #000000; /* Black */
--secondary-color--dark: #9D7C39; /* Dark Gold */
--light-blue: rgb(93, 123, 244) /*Light Blue - Added color on top of original*/

--theme-color:#5ff096;

--data-color:#efdb44;
 }

h2{font-style: var(--main-color--light);

}

*-------------START STYLING OF CREATE AND EDIT PAGE ------*/

h4 {
    text-align: center;
}

.form-group {
    color: rgb(255, 255, 255);
}

.btn {
    color: #fffbfb;
    background-color: #bd1a11;
}

.form-control {
    display: flex;
    align-self: center;
    width: 200px;
    height: 20px;
    border: #e24c4c;
    text-align: left;
    background-color: #d6972a;
}

.control-label {
    align-items: center;
}
.text-danger {
    border: #f04d44 20px;
}

/*-------------END STYLING OF (shared) CREATE  AND EDIT PAGE ------*/


