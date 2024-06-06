# STEM CAPSTONE PRESENTATION SYMPOSIUM WEBSITE
Prepared by Haydn Tamura



Version: 0.2.1
Revision 04-17-2024

This file contains documentation for the Stem Capstone Presentation Synopsum Website. 


## General 

You may need to add non-presentation blocks to the website. These will have information such as introductions and break times.

```HTML


    <div class="info-box">
        <h4>0:00 PM - 0:00 PM </h4>
        <h1>Welcome & Introductions</h1>
        <h2> text </h2>
    </div>
    <div class="space"></div>
```
You can use the above snippit for any type of introduction or spacer. Put the snippet inbetween sections for presentations or other introduction blocks.



```HTML
    <div class="info-box">
        <h4>0:00 PM - 0:00 PM </h4>
        <h1>Welcome & Introductions</h1>
        <h2> text </h2>
    </div>
    <div class="space"></div>
--------------------PRESENTATION-------------
...
..  
..
.

---------------------END-PRESENTATION--------------------
    <div class="info-box">
        <h4>0:00 PM - 0:00 PM </h4>
        <h1>Break</h1>
    </div>
    <div class="space"></div>


```


Each webpage has a header on top, containing tabs that go to the other parts of the website. 
```HTML
 <header>
        <section class="uwb-logo">
            <a href="https://www.uwb.edu/stem"><img src="images/web-white-left-school-signature-uw-bothell.png"
                    alt="UW Bothell School of STEM Logo"></a>
        </section>

        <nav class="align-center" id="dawgdrops">
            <div class="dawgdrops-inner container">
                <ul class="dawgdrops-nav" id="menu-brand-menu">

                    <li class="dawgdrops-item">
                        <a href="index.html" id="101" title="Home Page">Home Page</a>
                    </li>

                    <li class="dawgdrops-item">
                        <a class="dropdown-toggle" href="#" id="102" title="Biological Sciences">Biological Sciences</a>

                        <ul class="dawgdrops-menu dawgdrops-menu-em" id="menu-102">
                            <li>
                                <a href="./biological-sciences.html" title="BIO">Biology</a>
                            </li>
                        </ul>
                    </li>

                    <li class="dawgdrops-item">
                        <a class="dropdown-toggle" href="#" id="103" title="Computing & Software System">Computing &
                            Software Systems</a>

                        <ul class="dawgdrops-menu dawgdrops-menu-em" id="menu-104">
                            <li>
                                <a href="./csse.html" title="CSSE">Computer Science & Software Engineering</a>
                            </li>
                            <li>
                                <a href="./applied-computing.html" title="ACMPT">Applied Computing</a>
                            </li>
                        </ul>

                    </li>

                    <li class="dawgdrops-item">
                        <a class="dropdown-toggle" href="#" id="102" title="Engineering">Engineering</a>

                        <ul class="dawgdrops-menu dawgdrops-menu-em" id="menu-104">
                            <li>
                                <a href="./engineering.html" title="ENG">Engineering</a>
                            </li>
                        </ul>
                    </li>
                    <li class="dawgdrops-item">
                        <a class="dropdown-toggle" href="#" id="102" title="Mathematics">Mathematics</a>

                        <ul class="dawgdrops-menu dawgdrops-menu-em" id="menu-104">
                            <li>
                                <a href="./mathematics.html" title="MATH">Mathematics</a>
                            </li>
                        </ul>
                    </li>
                    <li class="dawgdrops-item">
                        <a class="dropdown-toggle" href="#" id="102" title="Physics">Physical Sciences</a>

                        <ul class="dawgdrops-menu dawgdrops-menu-em" id="menu-104">
                            <li>
                                <a href="./physics+chemistry.html" title="PHYS">Physics</a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
        </nav>

        <h1>**QUARTER AND YEAR** Capstone & Symposium</h1>
        <hr>
    </header>

```
This code is present on the top of all the `.html` files.

Some quarters may not have presentations for certain majors, so we will need to remove them from the header. Lets say we don't have any engineering presentations.

To remove the link to the engineering page, remove
```HTML

                    <li class="dawgdrops-item">
                        <a class="dropdown-toggle" href="#" id="102" title="Engineering">Engineering</a>

                        <ul class="dawgdrops-menu dawgdrops-menu-em" id="menu-104">
                            <li>
                                <a href="./engineering.html" title="ENG">Engineering</a>
                            </li>
                        </ul>
                    </li>

```

from the header. **This should be done for every .html file that has the header on the top of the file**. I recomend after removing (or adding back) tabs to the header, copy everything from `<header>` to ` </header>` , and pasting it into the other files where the html from `<header>` to ` </header>` has the old tabs.
 
## Major Sections
The following sections show how to update or change data for each Major web page.
### Biology
The biology presentations are done entirely within the `biological-sciences.html` file.
The html formatting for each presentation is:
```HTML
    <section class="presentation">
        <ul>
            <li>
                <p class="present-time">0:00 AM - 0:00 AM</p>
                <hr class="short-black-line">
                Project Title
                <div class="students-extend">
                    <h4>
                        student1<br>
                        student2<br>
                    </h4>
                    <h5 class="majors">
                        B.S. Biology<br />
                        Minor: Neuroscience<br />
                        

                    </h5>
                </div>
                <p>Faculty Advisor: </p>
            </li>

            <li>
                <img src="poster path" alt="Placeholder poster">
            </li>
        </ul>
    </section>

    <div class="space"></div>

```
Replace the placeholder text with the time, students; majors and minors, faculty, and posters with the information for that presentation. 
If you need to display multiple presentations, copy and paste everything from `<section class="presentation">` to   `<div class="space"></div>` for as many presentations as you need. For example, two presentations:
```HTML
    <section class="presentation">
        <ul>
            <li>
                <p class="present-time">12:00 PM - 1:00 PM</p>
                <hr class="short-black-line">
                Project Title
                <div class="students-extend">
                    <h4>
                        student1<br>
                        student2<br>
                        C
                    </h4>
                    <h5 class="majors">
                        B.S. Biology<br />
                        Minor: Neuroscience<br />
                        

                    </h5>
                </div>
                <p>Faculty Advisor: </p>
            </li>

            <li>
                <img src="poster path" alt="Placeholder poster">
            </li>
        </ul>
    </section>

    <div class="space"></div>
    <section class="presentation">
        <ul>
            <li>
                <p class="present-time">01:00 PM - 2:00 PM</p>
                <hr class="short-black-line">
                Project Title1
                <div class="students-extend">
                    <h4>
                        student1<br>
                        student2<br>
                        C
                    </h4>
                    <h5 class="majors">
                        B.S. Biology<br />
                        Minor: Neuroscience<br />
                        

                    </h5>
                </div>
                <p>Faculty Advisor: </p>
            </li>

            <li>
                <img src="poster path" alt="Placeholder poster">
            </li>
        </ul>
    </section>

    <div class="space"></div>

```


### Physical Sciences (Phys + Chem)
For the presentation schedule, edit the `physics+chemistry.html` file.
The presentations for Physics and Chemistry follow the same format as the Biology presentations above:

```HTML
    <section class="presentation">
        <ul>
            <li>
                <p class="present-time">0:00 AM - 0:00 AM</p>
                <hr class="short-black-line">
                <h3>Title</h3>
                <div class="students-extend">
                    <h4>
                        Student<br/>
                        <!-- <br/> -->
                    </h4>
                    <h5 class="majors">
                        Majors<br/>
                        <!-- Major<br/> -->
                    </h5>
                </div>
                <p>Faculty Advisor: </p>

                <br/>
            </li>

            <li>
                <img src="./posters/placeholder/placeholder.jpg" alt="Placeholder poster">
            </li>
        </ul>
    </section>

```

There is also a seperate .html file for the posters, `physics-poster-presentations.html`.

The format for a poster is as follows:

```HTML
    <div class="presentation-box">
        <!-- ------------------------------------ Poster 1 ------------------------------------ -->
        <section class="presentation">
            <ul>
                <li>
                    <h3>Title</h3>
                    <div class="students-extend">
                        <h4>
                            Student<br/>
                            <br>
                            Student<br/>
                        </h4>
                        <h5 class="majors">
                            Major<br/>
                            Major<br/>
                        </h5>
                    </div>
                    <p>Faculty Advisor: </p>
                </li>
        
                <li>
                    <img src="./posters/placeholder/placeholder.jpg" alt="Placeholder poster">
                </li>
            </ul>
        </section>

    </div>

    <div class="space"></div>

```
Like the previouse formatting, if you need multiple posters, copy and paste the sections for as many posters as you need.

### Engineering
Enginering is done in the engineering.html file:
```HTML
    <section class="presentation">
        <ul>
            <li>
                <p class="present-time">8:05 AM - 8:10 AM </p>
                <hr class="short-black-line">
                <h3>Title</h3>
                <div class="students">
                    <h4>
                        Students<br/>
                        <br/>
                        <br/>
                    </h4>
                    <h5 class=majors>
                        <br/>
                        <br/>
                        <br/>
                    </h5>
                </div>
                <p>Faculty Advisor: </p>
                <p>Industry Sponsor: </p>
                <p>Industry Sponsor: </p>
            </li>

            <li>
                <img src="./posters/placeholder/placeholder.jpg" alt="uav plane Poster">
            </li>
        </ul>
    </section>

```
For multiple presentations, just copy and paste for as many presentations as you need.

### Mathematics
The mathematics presentations are a little different. They are defined in the `mathematics.html` file.

```HTML
    <!-- ------------------------------------ Presentation 1 ------------------------------------ -->
    <section class="presentation">
        <ul>
            <li>
                <p class="present-time">0:00 AM - 0:00 AM </p>
                <hr class="short-black-line">
                <h3>Title</h3>
                <div class="students">
                    <h4>
                       name<br />
                        <br />
                        <br />
                        name2<br />
                        <br />
                        <br />
                       name3<br />
                        <br />
                        <br />
                    </h4>

                    <h5 class=majors>
                        BS Mathematics<br />
                        Minor: Physics<br />
                        <br />
                        BS Mathematics<br />
                        Minor:<br />
                        <br />
                        BS Mathematics<br />
                        Minor: <br />
                        <br />
                        BS Mathematics<br />
                        <br />
                        BS Mathematics<br />
                        Minor: <br />
                        <br />
                    </h5>
                </div>
                <p>Faculty Advisor: </p>
                <p>Industry Sponsor:</p>
            </li>

            <li>
                <img src="" alt="Poster">
            </li>
        </ul>
    </section>
    <!-- ------------------------------------ End Presentation 1 ------------------------------------ -->
<!-- -------------------------------------- Break 1 ------------------------------------------ -->
<div class="info-box">
    <h4>0:00 AM - 0:00 AM</h4>
    <h1> Break </h1>
</div>
```
Student names are listed in the 
```
                    <h4>
                       name<br />
                        <br />
                        <br />
                        name2<br />
                        <br />
                        <br />
                       name3<br />
                        <br />
                        <br />
                    </h4>
```
section. If you need to add more students, add the name and at least 3 `<br />`  within `<h4>` and `<\h4>`.
The same is for the Majors section,
```

                    <h5 class=majors>
                        BS Mathematics<br />
                        Minor: Physics<br />
                        <br />
                        BS Mathematics<br />
                        Minor:<br />
                        <br />
                        BS Mathematics<br />
                        Minor: <br />
                        <br />
                        BS Mathematics<br />
                        <br />
                        BS Mathematics<br />
                        Minor: <br />

```
However you don't need as many `<br />`.

For multiple presentations, copy everything starting from `  <section class="presentation">`  to the `</div>` closing the `<div class="info-box">`.

### Computing and Software Systems (CSSE + AC)
This section details documentation for the CSSE and AC web pages.
#### CSSE
The website will automatically load CSSE presentation data from files named `csseRoom*n*.json,` where *n* is the room number. There may be multiple presentation rooms, so numerous JSON files will need data and then loaded by the website.
To do so, open `structure.js` in the js directory and go around line 111. You should see the following:
```JavaScript
if (typeof document.getElementById("room-1-presentations") != "undefined") {
    loadCSSEPresentations("room-1-presentations", "js/csseRoom1.json");
    loadCSSEPresentations("room-2-presentations", "js/csseRoom2.json");
    loadCSSEPresentations("room-3-presentations", "js/csseRoom3.json");
    loadCSSEPresentations("room-4-presentations", "js/csseRoom4.json");
     loadCSSEPresentations("room-5-presentations", "js/csseRoom5.json");
    loadCSSEPresentations("room-6-presentations", "js/csseRoom6.json");
    
    loadCSSEPresentations("room-7-presentations", "js/csseRoom7.json"); 
    loadCSSEPresentations("room-8-presentations", "js/csseRoom8.json"); 
    
    loadTitleToSideNav("js/csseRoom1.json");
    loadTitleToSideNav("js/csseRoom2.json");
    loadTitleToSideNav("js/csseRoom3.json");
    loadTitleToSideNav("js/csseRoom4.json");
     loadTitleToSideNav("js/csseRoom5.json");
     loadTitleToSideNav("js/csseRoom6.json");
     loadTitleToSideNav("js/csseRoom5.json");
    loadTitleToSideNav("js/csseRoom6.json");
    loadTitleToSideNav("js/csseRoom7.json"); 
    loadTitleToSideNav("js/csseRoom8.json"); 

}
```
In this example, there are eight rooms. If there are more than eight rooms, add an extra `loadCSSEPresentations("room-n-presentations", "js/csseRoomn.json");,` where n is the number of the JSON file.

For example, here is what the code should look like if there are only 4 rooms:
```JavaScript
if (typeof document.getElementById("room-1-presentations") != "undefined") {
    loadCSSEPresentations("room-1-presentations", "js/csseRoom1.json");
    loadCSSEPresentations("room-2-presentations", "js/csseRoom2.json");
    loadCSSEPresentations("room-3-presentations", "js/csseRoom3.json");
    loadCSSEPresentations("room-4-presentations", "js/csseRoom4.json");
    // loadCSSEPresentations("room-5-presentations", "js/csseRoom5.json");
   // loadCSSEPresentations("room-6-presentations", "js/csseRoom6.json");
    
   // loadCSSEPresentations("room-7-presentations", "js/csseRoom7.json"); 
    //loadCSSEPresentations("room-8-presentations", "js/csseRoom8.json"); 
    
    loadTitleToSideNav("js/csseRoom1.json");
    loadTitleToSideNav("js/csseRoom2.json");
    loadTitleToSideNav("js/csseRoom3.json");
    loadTitleToSideNav("js/csseRoom4.json");
    // loadTitleToSideNav("js/csseRoom5.json");
   //  loadTitleToSideNav("js/csseRoom6.json");
   //  loadTitleToSideNav("js/csseRoom5.json");
   // loadTitleToSideNav("js/csseRoom6.json");
   // loadTitleToSideNav("js/csseRoom7.json"); 
   // loadTitleToSideNav("js/csseRoom8.json"); 

}
```
You will need to insert data into the correct fields to add data to the JSON files. Each JSON file has a list of csse presentations with the following data members:
```JSON
{
            "time":"",
            "projectId": "",
            "title": "",
            "studentName":"", 
            "studentMajor": "",
            "projectType":"",
            "facultyAdvisor":"", 
            "posterLink": "",
            "abstract": "",
},
```
Most of these are self-explanatory; however, `projectId` has the format csse-n-XYZ, where n is the number in the JSON file (i.e. csse-5-XYZ for csseRoom5.json), and XYZ is the starting time of the presentation (i.e. csse-5-100 for a presentation at 1:00 pm).

The website supports multiple entries for `StudentName`, `StudentMajor`, `posterLink`, and `abstract`. Each entry in these fields must be separated by "\n\n". For example:
```JSON
"time": "1:30 PM - 2:00 PM",
            "projectId": "csse-4-130",
            "title": "A Title",
            "studentName": "Bob \n\nJoe",
            "studentMajor": "CSSE\n\nCSSE",
            "projectType": "Group Project - Student Defined",
            "facultyAdvisor": "Faculty",
            "posterLink": "posters/csse/bobPoster1.png\n\nposters/csse/joePoster2.png",
            "abstract": "fdhlskfhdslkfhjdslkfjhsdlkfjds\n\ndjfshdkfhsdkfhdskfhsdkjfh"

```
The website will automatically parse the data groups in each field and format them on the website.

If the student does not have a poster, or cannot use a poster due to certain circumstances, put <<NOPOSTER>> for the poster link; The website will avoid creating a frame for an empty poster.


Additionally, you will need to navigate to `CSSE.html` and go to around line 141:
```HTML

    <section class="zoom-room-buttons">
        <button id="room-1-button" class="room-button" data-section="room-1-presentations" type="button">UW1 110</button>
        <div class="vertical-line"></div>

        <button id="room-2-button" class="room-button" data-section="room-2-presentations" type="button">UW1 120</button>
        <div class="vertical-line"></div>

        <button id="room-3-button" class="room-button" data-section="room-3-presentations" type="button">UW1 121</button>
        <div class="vertical-line"></div>
        
        <button id="room-4-button" class="room-button" data-section="room-4-presentations" type="button">UW1 202</button>
        <div class="vertical-line"></div>

        <button id="room-5-button" class="room-button" data-section="room-5-presentations" type="button">UW1 210</button>
        <div class="vertical-line"></div>

        <button id="room-6-button" class="room-button" data-section="room-6-presentations" type="button">UW1 220</button>
        <div class="vertical-line"></div>

        <button id="room-7-button" class="room-button" data-section="room-7-presentations" type="button">UW1 221</button>
    <div class = "vertical-line"></div>    
 </section>
<section id="room-1-presentations" class="room"></section>
    <section id="room-2-presentations" class="room hide"></section>
    <section id="room-3-presentations" class="room hide"></section>
    <section id="room-4-presentations" class="room hide"></section>
    <section id="room-5-presentations" class="room hide"></section>
    <section id="room-6-presentations" class="room hide"></section>
    <section id="room-7-presentations" class="room hide"></section>
```
Here, there are seven rooms. Ensure that the number of sections matches the number of rooms students will present in. So if there are eight presentations, you would add these:
```HTML
   ...
     <button id="room-8-button" class="room-button" data-section="room-8-presentations" type="button">UW1 PUT ROOM NUMBER HERE</button>
    <div class = "vertical-line"></div>
...    
 <section id="room-8-presentations" class="room hide"></section>
```


#### AC
The applied computing section is done entirly within the `applied-computing.html` file.




For the presentations, group each project into a div with the class "acContent". Within this div, you can create multiple presentation cards within divs with `col#` ids, and the presentation cards themselves with divs with the class `student-box`. The following is a template:
``` HTML
<div class="acContent_Block">
        <div class="acContent">
            <!--  Student column 1  -->

            <div id="col2" class="acspan-12">
                <div class="gray-box"><!---->
                    <h3>0:00 PM - 0:00 PM</h3>
                    <h1><b>Panel Discussion:</b>..</h1>
                    <div class="gray-box-text">
                        <b>Host:</b> Host name  |
                        <b>Assistants:</b> Assistants <br><br>
                    </div>
                </div>

                <div class="student-box">
                    <img src="./posters/applied-computing/kim.png" width="384" height="216" alt="Rat-a-Tat-Cat!" style="cursor:pointer"
                    onclick="onClick(this)" class="w3-hover-opacity">
                    <h3>Title</h3>
                    <div class="students">
                        <h4>
                           Studnet<br/>
                        </h4>
                        <h5 class="majors">
                            Applied Computing,<br/>
                            Second discipline:
                        </h5>
                    </div>
                    <p>Faculty Advisor:  </p>
                </div>

                <div class="student-box">
                    <img src="./posters/applied-computing/timbol.png" width="384" height="216" alt="Exerlog" style="cursor:pointer"
                    onclick="onClick(this)" class="w3-hover-opacity">
                    <h3>Title</h3>
                    <div class="students">
                        <h4>
                            student<br/>
                        </h4>
                        <h5 class="majors">
                            Applied Computing,<br/>
                            Second discipline:
                        </h5>
                    </div>
                    <p>Faculty Advisor:  </p>
                </div>



            </div>
            <!-- column 1 END -->

            <!--  Student column 2  -->
            <div id="col3" class="acspan-6 ">
                <div class="empty-box"></div>
                <br/><br/><br/>


                <div class="student-box">
                    <img src="./posters/applied-computing/tran_brandon.jpg" width="384" height="216" alt="Exerlog" style="cursor:pointer"
                    onclick="onClick(this)" class="w3-hover-opacity">
                    <h3>Project Title</h3>
                    <div class="students">
                        <h4>
                            Student Name<br/>
                        </h4>
                        <h5 class="majors">
                            Applied Computing,<br/>
                            Second discipline: ... <br/>...
                        </h5>
                    </div>
                    <p>Faculty Advisor: ...  </p>
                </div>                <div class="student-box">
                    <img src="./posters/applied-computing/tran_brandon.jpg" width="384" height="216" alt="Exerlog" style="cursor:pointer"
                    onclick="onClick(this)" class="w3-hover-opacity">
                    <h3>Project Title</h3>
                    <div class="students">
                        <h4>
                            Student Name<br/>
                        </h4>
                        <h5 class="majors">
                            Applied Computing,<br/>
                            Second discipline: ... <br/>...
                        </h5>
                    </div>
                    <p>Faculty Advisor: ...  </p>
                </div>
                <div class="student-box">
                    <img src="./posters/applied-computing/tran_brandon.jpg" width="384" height="216" alt="Exerlog" style="cursor:pointer"
                    onclick="onClick(this)" class="w3-hover-opacity">
                    <h3>Project Title</h3>
                    <div class="students">
                        <h4>
                            Student Name<br/>
                        </h4>
                        <h5 class="majors">
                            Applied Computing,<br/>
                            Second discipline: ... <br/>...
                        </h5>
                    </div>
                    <p>Faculty Advisor: ...  </p>
                </div>

            </div>
            <!-- column 2 END -->
        </div>
    </div>

```


