# TheatreCMS3
Content management system for theatre company to simply content creation for their website.
## Introduction
This project is built using ASP .NET MVC and Entity Framework. The end result is an interactive website for managing the content and productions for a theater/acting company. This content management service (aka CMS) is designed specifically for users who are not technically savvy and want to easily manage what displays on their website. It's also meant to help manage login capability for subscribers and maintain a wiki of past performances and performers.
## Dates
I worked on this project during an internship at The Tech Academy from March 20, 2023, to April 2, 2023.
## Skills
I used the following skills during the extent of my involvement in this project:
* Technical Writing
* Research
* Agile / SCRUM
* Git / Version Control
* Visual Studio
* HTML
* CSS
* JavaScript
* SQL
* Entity Framework
* C#
* .NET
## User Stories
### About Page
Create a new View in the Home View folder called About.cshtml.  The information for the about page should come from Theatre Vertigo's About page.  This about page is going to show the Mission Statement, Ensemble (including the images), Company History, and Board.  Copy the text from Theatre Vertigos about page and use the same images they are using for the Ensemble (check the Content > Images folder to see if the images are already in the project).

A UI/UX student created a mockup of the About Us page that you can recreate.  
#### Code
##### HTML
        @{
            ViewBag.Title = "About";
            Layout = "~/Views/Shared/_Layout.cshtml";



        }

        <style>
            .home-about-banner {
                width: 100vw;
                margin: 0;
                padding: 0;
                max-width: 100vw;
            }
        </style>

        <div class="home-about--page">
            <div class="home-about--title_container">

                <h1>About Us</h1>


                <div>
                    <div class="text-center">
                        <h2>Who We Are</h2>
                        <p class="home-about--mission_statement">We seek to engage audiences through compelling, ensemble-driven productions with a focus on developing new works.</p>
                    </div>
                </div>

            </div>
            <div class="home-about--company_history text-center">
                <h2>Company History</h2>
                <div class="home-about--history_text">
                    <p>
                        In 1997, Theatre Vertigo was founded by Paul Floding, Nanette Pettit, and Jeff Meyers. Since
                        then, Theatre Vertigo has performed in numerous spaces, including The Russell Street Theater,
                        The Electric Company, Theater!Theatre!, and The Shoebox Theater.
                    </p>
                    <p>
                        From 2003 to 2014, Theatre Vertigo produced Anonymous Theatre as a summer fundraiser in
                        collaboration with The Anonymous Theatre Company. Other past collaborations include
                        defunkt theatre, Stark Raving Theater, and Tears of Joy Theatre.
                    </p>
                    <p>
                        Theatre Vertigo has worked on world premieres, including <em>Faust.Us</em> by Joseph Fisher, <em>99 Ways to
                        Fuck a Swan</em> by Kim Rosenstack, and <em>The End of Sex</em> by Craig Jessen.
                    </p>
                    <p>
                        In 2016, Theatre Vertigo produced its first officially commissioned work from a playwright, <em>I Want to Destroy You</em>, by 
                        Rob Handel.
                    </p>
                </div>
            </div>
            <div class="home-about--ensemble_and_board">
                <h2>Ensemble</h2>
                <div class="home-about--ensemble_images">
                    <figure>
                        <img src="~/Content/images/Cast_Img_7.jpg" />
                        <figcaption>Tom Mounsey</figcaption>
                    </figure>
                    <figure>
                        <img src="~/Content/images/Cast_Img_1.jpg" />
                        <figcaption>Kala Maarja Hellier</figcaption>
                    </figure>
                    <figure>
                        <img src="~/Content/images/Cast_Img_3.jpg" />
                        <figcaption>Heath Hyun Houghton</figcaption>
                    </figure>
                    <figure>
                        <img src="~/Content/images/Cast_Img_4.jpg" />
                        <figcaption>Jacquelle Davis</figcaption>
                    </figure>
                    <figure>
                        <img src="~/Content/images/Cast_Img_6.jpg" />
                        <figcaption>Victoria Alvarez-Chacon</figcaption>
                    </figure>
                </div>
                <hr />
                <div class="home-about--board text-center">
                    <h2>Board</h2>
                    <div class="home-about--board_text">
                        <p>Jamie Floyd (President)</p>
                        <p>Tom Mounsey</p>
                        <p>Marcia Reyes</p>
                        <p>Lena-Liis-Kiesel</p>
                    </div>
                </div>
            </div>
        </div>
##### CSS
        /* ABOUT PAGE */

        .home-about--page {
            background-color: var(--main-color--light);
        }

        .home-about--title_container {
            border-radius: 0px 0px 0px 120px;
            background: url("/Content/images/theater.jpg") no-repeat;
            background-size: 100vw;
            background-color: var(--dark-color);
            padding: 7vw 10px 40px 10px;
        }

        .home-about--title_container h1 {
            font-family: Broadway;
            text-align: center;
            padding-bottom: 500px;
        }

        .home-about--page h2 {
            text-transform: uppercase;
            text-align: center;
        }

        .home-about--page h2::after {
            content: "";
            display: block;
            width: 10vw;
            border-bottom: 2px solid var(--main-color);
            margin-left: auto;
            margin-right: auto;
        }

        .home-about--mission_statement {
            padding-left: 20vw;
            padding-right: 20vw;
        }

        .home-about--company_history {
            padding-top: 5vw;
            padding-bottom: 5vw;
            padding-left: 20vw;
            padding-right: 20vw;
        }

        .home-about--history_text {
            padding-top: 2vw;
        }

        .home-about--ensemble_and_board {
            border-radius: 0px 120px 0px 0px;
            background-color: var(--dark-color);
            background-size: 100vw;
            padding: 7vw 10px 40px 10px;
        }

        .home-contact-banner {
            background-color: var(--dark-color);
            border-radius: 0 0 0 100px;
            padding-bottom: 50px;
            padding-top: 50px;
            font-family: Broadway;
        }
        .home-about--ensemble_images {
            padding-top: 5vw;
        }

        .home-contact-btn {
            background-color: var(--main-color);
            border-color: var(--light-color);
            color: var(--light-color);
        }
        .home-about--ensemble_images img {
            border-radius: 50%;
            width: 200px;
            height: 200px;
            padding: 2vw;
        }

        .home-about--ensemble_images figure {
            text-align: center;
            text-transform: uppercase;
            display: inline-block;
        }

        /* no gray defined in their style guide. used a different color here. */

        .home-about--ensemble_and_board hr {
            border: 2px solid var(--secondary-color);
            margin-top: 2vw;
        }

        .home-about--board {
            padding-top: 5vw;
        }

        .home-about--board_text {
            padding-top: 2vw;
        }
#### Screenshots
![image](https://user-images.githubusercontent.com/117326004/229182232-e9724f9d-15c9-485f-934e-e302754d07e0.png)
![image](https://user-images.githubusercontent.com/117326004/229182298-92c7f3ce-4263-496d-8fd4-9429c4e4f69b.png)
![image](https://user-images.githubusercontent.com/117326004/229182392-c892def3-cd6d-40da-8d67-857bcddc398e.png)

### Entity model for CastMembers; CRUD pages for CastMembers

We need to create an entity model for the CastMember class so that cast members can be saved to the database. There are 3 parts to this story. You will need to create a model for CastMember, an enum for positions, and finally, you will need to create CRUD functionality.  

Attached is the schema for this model. The "?" indicates that a property is nullable. Ensure that only properties with "?" in the schema below are nullable. Comment out the Photo property after creating it. You will need to create a method to handle the byte array in a later story. You can uncomment it then. All other fields are required.

![image](https://user-images.githubusercontent.com/117326004/229180219-a062e1f3-ebca-44d6-a932-011d123b8aad.png)

You will need to create a PositionEnum for the MainRole property as well.

![image](https://user-images.githubusercontent.com/117326004/229180268-a9ad1a21-5266-4fe0-8dd5-60aaea2bdcc7.png)

After creating the model, you should update-database to migrate the changes to create a table in the database. You can use SQL Server Object Explorer in Visual Studio to check that the table has been created correctly. 

After the model is created, scaffold the CRUD pages for this model (Use Visual Studio and EntityFramework to create the Index, Edit, Create, Details, and Delete pages). Make sure to add the _Layout.cshtml as a layout page when creating your scaffolding.  Ensure that each page can be reached and CastMembers can be created, edited, and deleted. 

#### Model for CastMembers
        using System;
        using System.Collections.Generic;

        namespace TheatreCMS3.Areas.Prod.Models
        {
            public class CastMember
            {
                public int CastMemberId { get; set; }
                public string Name { get; set; }
                public int? YearJoined { get; set; }
                public Position MainRole { get; set; }
                public string Bio { get; set; }
                public byte[] Photo { get; set; }
                public bool CurrentMember { get; set; }
                public string Character { get; set; }
                public int? CastYearLeft { get; set; }
                public int? DebutYear { get; set; }
            }

            public enum Position
            {
                Actor,
                Director,
                Technician,
                StageManager,
                Other
            }
        }
#### Controller for CRUD operations
        using System;
        using System.Collections.Generic;
        using System.Data;
        using System.Data.Entity;
        using System.Drawing;
        using System.IO;
        using System.Linq;
        using System.Net;
        using System.Web;
        using System.Web.Mvc;
        using TheatreCMS3.Areas.Prod.Models;
        using TheatreCMS3.Models;

        namespace TheatreCMS3.Areas.Prod.Controllers
        {
            public class CastMembersController : Controller
            {
                private ApplicationDbContext db = new ApplicationDbContext();

                // GET: Prod/CastMembers
                public ActionResult Index()
                {
                    return View(db.CastMembers.ToList());
                }

                // GET: Prod/CastMembers/Details/5
                public ActionResult Details(int? id)
                {
                    if (id == null)
                    {
                        return new HttpStatusCodeResult(HttpStatusCode.BadRequest);
                    }
                    CastMember castMember = db.CastMembers.Find(id);
                    if (castMember == null)
                    {
                        return HttpNotFound();
                    }
                    return View(castMember);
                }

                // GET: Prod/CastMembers/Create
                public ActionResult Create()
                {
                    return View();
                }

                // POST: Prod/CastMembers/Create
                // To protect from overposting attacks, enable the specific properties you want to bind to, for 
                // more details see https://go.microsoft.com/fwlink/?LinkId=317598.
                [HttpPost]
                [ValidateAntiForgeryToken]
                public ActionResult Create([Bind(Include = "CastMemberId,Name,YearJoined,MainRole,Bio,CurrentMember,Character,CastYearLeft,DebutYear,Photo")] CastMember castMember, HttpPostedFileBase postedFile)
                {
                    if (ModelState.IsValid)
                    {
                        // converts uploaded image
                        if (postedFile != null && postedFile.ContentLength > 0)
                        {
                            using (BinaryReader br = new BinaryReader(postedFile.InputStream))
                            {
                                castMember.Photo = CastPhoto(br, postedFile);
                            }
                        }

                        db.CastMembers.Add(castMember);
                        db.SaveChanges();
                        return RedirectToAction("Index");
                    }

                    return View(castMember);
                }

                // converts cast member photo from photo to byte[] for saving in the database 

                private byte[] CastPhoto (BinaryReader br, HttpPostedFileBase postedFile)
                {
                    byte[] castBytes;
                    castBytes = br.ReadBytes(postedFile.ContentLength);
                    return castBytes;
                }

                // GET: Prod/CastMembers/Edit/5
                public ActionResult Edit(int? id)
                {
                    if (id == null)
                    {
                        return new HttpStatusCodeResult(HttpStatusCode.BadRequest);
                    }
                    CastMember castMember = db.CastMembers.Find(id);
                    if (castMember == null)
                    {
                        return HttpNotFound();
                    }
                    return View(castMember);
                }

                // POST: Prod/CastMembers/Edit/5
                // To protect from overposting attacks, enable the specific properties you want to bind to, for 
                // more details see https://go.microsoft.com/fwlink/?LinkId=317598.
                [HttpPost]
                [ValidateAntiForgeryToken]
                public ActionResult Edit([Bind(Include = "CastMemberId,Name,YearJoined,MainRole,Bio,CurrentMember,Character,CastYearLeft,DebutYear, Photo")] CastMember castMember, HttpPostedFileBase postedFile)
                {
                    if (ModelState.IsValid)
                    {
                        db.Entry(castMember).State = EntityState.Modified;
                        db.SaveChanges();
                        return RedirectToAction("Index");
                    }
                    return View(castMember);
                }

                // GET: Prod/CastMembers/Delete/5
                public ActionResult Delete(int? id)
                {
                    if (id == null)
                    {
                        return new HttpStatusCodeResult(HttpStatusCode.BadRequest);
                    }
                    CastMember castMember = db.CastMembers.Find(id);
                    if (castMember == null)
                    {
                        return HttpNotFound();
                    }
                    return View(castMember);
                }

                // POST: Prod/CastMembers/Delete/5
                [HttpPost, ActionName("Delete")]
                [ValidateAntiForgeryToken]
                public ActionResult DeleteConfirmed(int id)
                {
                    CastMember castMember = db.CastMembers.Find(id);
                    db.CastMembers.Remove(castMember);
                    db.SaveChanges();
                    return RedirectToAction("Index");
                }

                protected override void Dispose(bool disposing)
                {
                    if (disposing)
                    {
                        db.Dispose();
                    }
                    base.Dispose(disposing);
                }
            }
#### HTML for Create page
        @model TheatreCMS3.Areas.Prod.Models.CastMember

        @{
            ViewBag.Title = "Create";
            Layout = "~/Views/Shared/_Layout.cshtml";
        }

        <h2 class="castmember-create_edit--heading">Create Cast Member</h2>


        @using (Html.BeginForm("Create", "CastMembers", FormMethod.Post, new { enctype = "multipart/form-data" })) 
        {
            @Html.AntiForgeryToken()

        <div class="form-horizontal castmember-create_edit--form_container">
            <h4>CastMember</h4>
            <hr />
            @Html.ValidationSummary(true, "", new { @class = "text-danger" })
            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.Name, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.Name, new { htmlAttributes = new { @class = "form-control", placeholder = "Cast member's name" } })
                    @Html.ValidationMessageFor(model => model.Name, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.YearJoined, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.YearJoined, new { htmlAttributes = new { @class = "form-control", placeholder = "Year they joined the cast" } })
                    @Html.ValidationMessageFor(model => model.YearJoined, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.MainRole, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EnumDropDownListFor(model => model.MainRole, htmlAttributes: new { @class = "form-control", placeholder = "Cast member's main role" })
                    @Html.ValidationMessageFor(model => model.MainRole, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.Bio, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.Bio, new { htmlAttributes = new { @class = "form-control", placeholder = "Enter cast member's bio" } })
                    @Html.ValidationMessageFor(model => model.Bio, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.CurrentMember, htmlAttributes: new { @class = "control-label col-md-2", })
                <div class="col-md-10">
                    <div class="checkbox">
                        @Html.EditorFor(model => model.CurrentMember)
                        @Html.ValidationMessageFor(model => model.CurrentMember, "", new { @class = "text-danger" })
                    </div>
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.Character, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.Character, new { htmlAttributes = new { @class = "form-control", placeholder = "Cast member's character" } })
                    @Html.ValidationMessageFor(model => model.Character, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.CastYearLeft, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.CastYearLeft, new { htmlAttributes = new { @class = "form-control", placeholder = "Year cast member left — leave blank if active" } })
                    @Html.ValidationMessageFor(model => model.CastYearLeft, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.DebutYear, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.DebutYear, new { htmlAttributes = new { @class = "form-control", placeholder = "The year the cast member debuted" } })
                    @Html.ValidationMessageFor(model => model.DebutYear, "", new { @class = "text-danger" })
                </div>
            </div>
            <div class="form-group">
                @Html.LabelFor(model => model.Photo, htmlAttributes: new { @class = "control-label col-md-2"})
                <div class="col-md-10">
                    <input type="file" name="postedFile" />
                    @Html.ValidationMessageFor(model => model.Photo, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group btn-toolbar castmember-create_edit--btn_group">
                <div class="col-md-offset-2 col-md-10">
                    <input type="submit" value="Create" class="btn btn-lg castmember-create_edit--create_save_btn" />
                    @Html.ActionLink("Back", "Index", "CastMembers", htmlAttributes: new { @class = "btn btn-lg ml-5 castmember-create_edit--back_btn" })
                </div>
            </div>
        </div>
        }
##### Screenshots
![image](https://user-images.githubusercontent.com/117326004/229182871-ee969ca3-3914-4c10-9d91-90950b4f187c.png)

#### HTML for Delete page
        @section Scripts {
            @Scripts.Render("~/bundles/jqueryval")
            <!-- scripts for image upload -->
            <script type="text/javascript">
                $(function () {
                    $("#dialog").dialog({
                        autoOpen: false,
                        modal: true,
                        height: 600,
                        width: 600,
                        title: "Zoomed Image"
                    });
                })
            </script>
        }


        @model TheatreCMS3.Areas.Prod.Models.CastMember

        @{
            ViewBag.Title = "Delete";
            Layout = "~/Views/Shared/_Layout.cshtml";
        }

        <h2>Delete</h2>

        <h3>Are you sure you want to delete this?</h3>
        <div>
            <h4>CastMember</h4>
            <hr />
            <dl class="dl-horizontal">
                <dt>
                    @Html.DisplayNameFor(model => model.Name)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.Name)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.YearJoined)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.YearJoined)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.MainRole)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.MainRole)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.Bio)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.Bio)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.CurrentMember)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.CurrentMember)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.Character)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.Character)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.CastYearLeft)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.CastYearLeft)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.DebutYear)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.DebutYear)
                </dd>

            </dl>

            @using (Html.BeginForm()) {
                @Html.AntiForgeryToken()

                <div class="form-actions no-color">
                    <input type="submit" value="Delete" class="btn btn-default" /> |
                    @Html.ActionLink("Back to List", "Index")
                </div>
            }
        </div>
#### HTML for Details page
        @model TheatreCMS3.Areas.Prod.Models.CastMember

        @{
            ViewBag.Title = "Details";
            Layout = "~/Views/Shared/_Layout.cshtml";
        }

        <h2>Details</h2>

        <div>
            <h4>CastMember</h4>
            <hr />
            <dl class="dl-horizontal">
                <dt>
                    @Html.DisplayNameFor(model => model.Name)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.Name)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.YearJoined)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.YearJoined)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.MainRole)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.MainRole)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.Bio)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.Bio)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.CurrentMember)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.CurrentMember)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.Character)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.Character)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.CastYearLeft)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.CastYearLeft)
                </dd>

                <dt>
                    @Html.DisplayNameFor(model => model.DebutYear)
                </dt>

                <dd>
                    @Html.DisplayFor(model => model.DebutYear)
                </dd>

            </dl>
        </div>
        <p>
            @Html.ActionLink("Edit", "Edit", new { id = Model.CastMemberId }) |
            @Html.ActionLink("Back to List", "Index")
        </p>
#### HTML for Edit page
        @model TheatreCMS3.Areas.Prod.Models.CastMember

        @{
            ViewBag.Title = "Edit";
            Layout = "~/Views/Shared/_Layout.cshtml";
        }

        <h2 class="castmember-create_edit--heading">Edit Cast Member</h2>


        @using (Html.BeginForm())
        {
            @Html.AntiForgeryToken()

        <div class="form-horizontal castmember-create_edit--form_container">
            <h4>CastMember</h4>
            <hr />
            @Html.ValidationSummary(true, "", new { @class = "text-danger" })
            @Html.HiddenFor(model => model.CastMemberId)

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.Name, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.Name, new { htmlAttributes = new { @class = "form-control" } })
                    @Html.ValidationMessageFor(model => model.Name, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.YearJoined, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.YearJoined, new { htmlAttributes = new { @class = "form-control" } })
                    @Html.ValidationMessageFor(model => model.YearJoined, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.MainRole, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EnumDropDownListFor(model => model.MainRole, htmlAttributes: new { @class = "form-control" })
                    @Html.ValidationMessageFor(model => model.MainRole, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.Bio, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.Bio, new { htmlAttributes = new { @class = "form-control" } })
                    @Html.ValidationMessageFor(model => model.Bio, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.CurrentMember, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    <div class="checkbox">
                        @Html.EditorFor(model => model.CurrentMember)
                        @Html.ValidationMessageFor(model => model.CurrentMember, "", new { @class = "text-danger" })
                    </div>
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.Character, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.Character, new { htmlAttributes = new { @class = "form-control" } })
                    @Html.ValidationMessageFor(model => model.Character, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.CastYearLeft, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.CastYearLeft, new { htmlAttributes = new { @class = "form-control" } })
                    @Html.ValidationMessageFor(model => model.CastYearLeft, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group castmember-create_edit--form_input">
                @Html.LabelFor(model => model.DebutYear, htmlAttributes: new { @class = "control-label col-md-2" })
                <div class="col-md-10">
                    @Html.EditorFor(model => model.DebutYear, new { htmlAttributes = new { @class = "form-control" } })
                    @Html.ValidationMessageFor(model => model.DebutYear, "", new { @class = "text-danger" })
                </div>
            </div>

            <div class="form-group btn-toolbar castmember-create_edit--btn_group">
                <div class="col-md-offset-2 col-md-10">
                    <input type="submit" value="Save" class="btn btn-lg castmember-create_edit--create_save_btn" />
                    @Html.ActionLink("Back", "Index", "CastMembers", htmlAttributes: new { @class = "btn btn-lg ml-5 castmember-create_edit--back_btn" })
                </div>
            </div>
        </div>
        }

        @section Scripts {
            @Scripts.Render("~/bundles/jqueryval")
        }
##### Screenshots
![image](https://user-images.githubusercontent.com/117326004/229183034-080b846f-c1e5-4eb2-acd6-3504531bb1f5.png)

#### HTML for Index page
        @model IEnumerable<TheatreCMS3.Areas.Prod.Models.CastMember>

        @{
            ViewBag.Title = "Index";
            Layout = "~/Views/Shared/_Layout.cshtml";
        }

        <h2>Index</h2>

        <p>
            @Html.ActionLink("Create New", "Create")
        </p>
        <table class="table">
            <tr>
                <th>
                    @Html.DisplayNameFor(model => model.Name)
                </th>
                <th>
                    @Html.DisplayNameFor(model => model.YearJoined)
                </th>
                <th>
                    @Html.DisplayNameFor(model => model.MainRole)
                </th>
                <th>
                    @Html.DisplayNameFor(model => model.Bio)
                </th>
                <th>
                    @Html.DisplayNameFor(model => model.CurrentMember)
                </th>
                <th>
                    @Html.DisplayNameFor(model => model.Character)
                </th>
                <th>
                    @Html.DisplayNameFor(model => model.CastYearLeft)
                </th>
                <th>
                    @Html.DisplayNameFor(model => model.DebutYear)
                </th>
                <th>
                    @Html.DisplayNameFor(model => model.Photo)
                </th>
            </tr>

        @foreach (var item in Model) {
            <tr>
                <td>
                    @Html.DisplayFor(modelItem => item.Name)
                </td>
                <td>
                    @Html.DisplayFor(modelItem => item.YearJoined)
                </td>
                <td>
                    @Html.DisplayFor(modelItem => item.MainRole)
                </td>
                <td>
                    @Html.DisplayFor(modelItem => item.Bio)
                </td>
                <td>
                    @Html.DisplayFor(modelItem => item.CurrentMember)
                </td>
                <td>
                    @Html.DisplayFor(modelItem => item.Character)
                </td>
                <td>
                    @Html.DisplayFor(modelItem => item.CastYearLeft)
                </td>
                <td>
                    @Html.DisplayFor(modelItem => item.DebutYear)
                </td>
                <td>
                    @if (item.Photo != null)
                    {
                        <img src="data:image;base64,@System.Convert.ToBase64String(item.Photo)" width="80" height="80" />
                    }
                </td>
                <td>
                    @Html.ActionLink("Edit", "Edit", new { id=item.CastMemberId }) |
                    @Html.ActionLink("Details", "Details", new { id=item.CastMemberId }) |
                    @Html.ActionLink("Delete", "Delete", new { id=item.CastMemberId })
                </td>
            </tr>
        }

        </table>
#### CSS for CRUD pages
        /* Styling for Cast Member CRUD pages*/

        .castmember-create_edit--heading {
            padding: 5vw;
            text-align: center;
        }

        .castmember-create_edit--back_btn {
            background-color: var(--secondary-color);
            padding: 1vw;
            width: 15vw;
            border-radius: 7px;
            border: 1px solid var(--secondary-color);
            transition: .3s;
        }

        .castmember-create_edit--back_btn:hover {
            box-shadow: 5px 5px var(--secondary-color--dark);
            transition: .3s;
        }

        .castmember-create_edit--create_save_btn {
            background-color: var(--secondary-color--dark);
            padding: 1vw;
            width: 15vw;
            border-radius: 7px;
            border: 1px solid var(--secondary-color--dark);
            transition: .3s;
        }

        .castmember-create_edit--create_save_btn:hover {
            box-shadow: 5px 5px var(--secondary-color);
            transition: .3s;
        }

        .castmember-create_edit--btn_group {
            padding: 2vw;
            display: block;
            align-content: center;
            text-align: center;
        }

        .castmember-create_edit--form_container {
            background-color: var(--main-color);
            padding: 2vw;
        }

        .castmember-create_edit--form_input input, option, option:checked {
            background-color: var(--secondary-color);
            border: 0px solid;
        }


        .castmember-create_edit--form_input input:focus {
            background-color: white;
            border: 0px solid;
            outline: 3px solid var(--secondary-color);
        }
