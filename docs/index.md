# Work Items Gantt 

*Work Items Gantt* brings the interactive high-level project planning & scheduling to Polarion ALM. 

<div id="download-button" >
<style>
.mdc-button {	
	color:white;
    font-family: Roboto,sans-serif;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    font-size: .875rem;
    line-height: 2.25rem;
    font-weight: 500;
    letter-spacing: .0892857143em;
    text-decoration: none;
    text-transform: uppercase;
    padding: 4px 8px 0 8px;
    display: inline-flex;
    position: relative;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
    min-width: 64px;
    height: 36px;
    border: none;
    outline: none;
    line-height: inherit;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
    -webkit-appearance: none;
    overflow: hidden;
    vertical-align: middle;
    border-radius: 4px;
    background-color:  #3e91fe;
    cursor:pointer;  
}
</style>
<style>
body {font-family: Arial, Helvetica, sans-serif;}

/* The Modal (background) */
.modal {
  display: none; /* Hidden by default */
  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  padding-top: 100px; /* Location of the box */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
}

/* Modal Content */
.modal-content {
  background-color: #fefefe;
  margin: auto;
  padding: 30px;
  border: 1px solid #888;
  max-width: 650px;
}

/* The Close Button */
.close {
  color: #aaaaaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
}
.emailinput {
    border: 1px solid #89b1dc;
    padding: 10px;
    width: 60%;
    margin-top: 40px;
    margin-bottom: 40px;
    border-radius:4px;
    height:36px;
    }
</style>



<!-- The Modal -->
<div id="myModal" class="modal">
  <!-- Modal content -->
  <div class="modal-content">
    <span class="close">&times;</span>
    <h1>Download <b>Work Items Gantt</b></h1>
    Please fill in your email address to download the installation package.
    <center>
    <form onSubmit="downloadDist()">
    <input type="email"  id="email" class="emailinput" placeholder="Enter your email." />
    <input type="submit" class="mdc-button" value="Submit" />
    </form>
    <span style="font-size: 75%;color: gray;">
    By downloading the product you consent to and fully accept our <a target="_blank" href="https://gantt.nextedy.com/download/LICENSE.pdf">License Terms</a>.
    </span>
    </center>
    
  </div>
</div>

<center ><br/>
<a onClick="openDownload()">
<button class="mdc-button">&nbsp;Download Trial Now!&nbsp;</button>
</a>
</center>
<br>
</div>


Interactive drag & drop enabled Gantt chart widget provides unique capabilities to expose the standard Work Items (such as Features, Epics, Objectives, ...) as micro projects in a visually appealing way and perform various operations easily and efficiently.

<a href="https://youtu.be/9D_djgsCIac">
<center>
**Play Overview Video**
</center>
![Gantt Screenshot](img/gantt-overall.png)
</a>

## Adjust Schedule

You can easily adjust the project schedule, including re-scheduling of the subtasks when the parent project schedule is adjusted:

![Replan](img/gantt-drag-children.gif)

## Manage Dependencies

The Management of project and task dependencies is another common task. Just start a link on start item and finish it on target item:

![Dependencies](img/gantt-drag-dependency-link.gif)

## Project Types

Sometimes the task schedule should be derivered from the children, this is exactly what is covered by `project` type. (Task Script needs to be used to configure what work items are of type `project`

![Projects](img/gantt-projects.gif)

<script type="text/javascript" src="https://s3.amazonaws.com/assets.freshdesk.com/widget/freshwidget.js"></script>
<script type="text/javascript">
	FreshWidget.init("", {"queryString": "&widgetType=popup&formTitle=Nextedy+Help+%26+Support+Center&screenshot=no&captcha=yes", "utf8": "✓", "widgetType": "popup", "buttonType": "text", "buttonText": "Support", "buttonColor": "black", "buttonBg": "#2196f3", "alignment": "4", "offset": "235px", "formHeight": "500px", "screenshot": "no", "captcha": "yes", "url": "https://nextedy.freshdesk.com"} );
</script>

<script>
var modal = document.getElementById("myModal");
var span = document.getElementsByClassName("close")[0];
span.onclick = function() {
  modal.style.display = "none";
}
window.onclick = function(event) {
  if (event.target == modal) {
    modal.style.display = "none";
  }
}
function openDownload(){
  var modal = document.getElementById("myModal");
  modal.style.display = "block";
}

function downloadDist(){
    var email = document.getElementById("email").value;
    if(email==null){
    		return false;
    }
	ga('send','event','download','Gantt-Distribution',"email:"+email);
	modal.style.display = "none";	
	window.open('https://nextedy.github.io/gantt-docs/download/work_items_gantt.zip');
}
 var url = location.href;
 if(url.indexOf("downloadNow")!=-1){
    var modal = document.getElementById("myModal");
    modal.style.display = "block";
 }
 
</script>
