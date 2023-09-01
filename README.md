# STEM CAPSTONE PRESENTATION SYNOPSUM WEBSITE
Prepared by Haydn Tamura


Version: 0.1.0
Date: 08-18-2023

This file contains documentation for the Stem Capstone Presentation Synopsum Website. 
 
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

    <script type='text/javascript' src="js/structure.js"></script>

```
Replace the placeholder text with the time, students; majors and minors, faculty, and posters with the information for that presentation. For multiple presentation, you can copy and paste that html section and fill in the data. 

### Physical Sciences (Phys + Chem)
### Engineering and Mathematics
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

##### Formatting
To create an into block on the website
```HTML
    <div class="info-box">
        <h4>0:00 PM - 0:00 PM </h4>
        <h1>Welcome & Introductions</h1>
        <h2>Dr. Laurie Anderson & Sonal Yadav</h2>
    </div>
    <div class="space"></div>
```
In this example, the introductions are done by Dr. Laurie Anderson and Sonal Yadav. Replace those names with the people presenting for the current capstone.

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


