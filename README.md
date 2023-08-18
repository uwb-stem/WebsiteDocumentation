# STEM CAPSTONE PRESENTATION SYNOPSUM WEBSITE
Prepared by Haydn Tamura
Additional Authors:

Version: 0.1.0
Date: 08-18-2023

This file contains documentation for the Stem Capstone Presentation Synopsum Website. 
 
## Major Sections
The following sections show how to update or change data for each Major web page.
### Biology
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


