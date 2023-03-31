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
