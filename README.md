# Studio: Angular, Part 1



## Mission Planning Dashboard
A useful and common front end application is a dashboard. It shows a summary of information about a topic, helping users of the web app make informed decisions.

You will create a Space Mission Planning Dashboard.

### Setup
Fork the Angular Lesson 1 Studio repository.
Clone your fork to your computer.

### Create Angular Project
Open a terminal at the root of the angular-lc101-mission-planner repository you just cloned.
Create a new Angular project by running ng new mission-planning-dashboard.
When prompted about using routing, enter "N" for No.
When prompted to select the stylesheet format, select CSS.

### Update Starter Page Content
The default stater page created by Angular contains default text, images, and links. Your job is to remove the default content.

Clear out the contents of file app.component.html.
Type in the text Add components here... into app.component.html.

### Header Component
You need to create a component that shows the title, mission name, and carrier rocket.

Create a header component using ng g component header.
In the file header.component.html add HTML:

<h1>Mission Planning Dashboard</h1>
<h3>Mission Name: {{ missionName }}</h3>
<h3>Carrier Rocket: {{ rocketName }}</h3>
Add the variables missionName and rocketName to the header component in header.component.ts

Add a reference to the header component in app.component.html.
<app-header></app-header>

### Crew Component
Next you need to make a component to show a list of crew members.

Create the component by running ng g component crew.

Set the contents of crew.component.html to be:

<h3>Crew</h3>
<ul>
   <li>Jessica Watkins</li>
   <li>Raja Chari</li>
   <li>Jasmin Moghbeli</li>
</ul>
Add a reference to the header component in app.component.html.


### Equipment Component
Now you need to create a component to show a list of equipment.

Create an equipment component named equipment.

The component should display the following:

An <h3> that contains "Equipment"
A <ul> that contains <li> for: Habitat dome, Drones, Food containers, Oxygen tanks
Add the equipment component to app.component.html using the HTML below. Notice the <div> surrounding the crew and equipment components.


<app-header></app-header>
<div class="box">
   <app-crew></app-crew>
   <app-equipment></app-equipment>
</div>
Add CSS to file app.component.css to horizontally align the crew and equipment lists. Without this CSS, the equipment list will appear below the crew list.

.box {
   display: flex;
   padding: 10px;
}

### Experiments Component
Finally, add an experiments component that contains the HTML below:

<h3>Experiments</h3>
<ul>
   <li>Mars soil sample</li>
   <li>Plant growth in habitat</li>
   <li>Human bone density</li>
</ul>
Make the list of experiments show up to the right of equipment list.

### Commit Your Work
This repository will be used for the next two studios. Be sure to stage, commit, and push your changes. The next studio will start with a different branch.

Verify the branch and status of the files.
Commit your changes.
Push your commits to origin.
