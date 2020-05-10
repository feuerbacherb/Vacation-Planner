# Vacation-Planner
National Park Weather and Things To Do App

## Description of Project
The requirements of the project are as follows
* Use a CSS framework other than Bootstrap
* Be deployed to GitHub Pages
* Be interactive (ie, accept and respond to user input)
* Use at least two server-side APIs
* Does not use alerts, confirms, or prompts (use modals)
* Use client-side storage to store persistent data
* Be responsive
* Have a polished UI
* Have a clean repository that meets quality coding standards (file structure, naming conventions, follows best practices for class/id naming conventions, indentation, quality comments, etc)
* Have a quality README (with unique name, description, technologies used, screenshot, and link to deployed application)
* Add your project to the portfolio you created in module 2

## Elevator story
You and your family are coming up to a three day weekend where everybody is off.  Somebody says that they want to get away and go camping.  Normally you would need to first find a park or place to go, then check out the weather, then go somewhere else to find a campground that meets your needs.  It's really a pain.
We have created a new application called Vacation Planner to help in the decision making process.  We have combined a number of resources to do data mining of information so you don't have to.
Want to go to a different state and see what parks they offer?  We have that.
Want to see what the weather is going to be over the next couple of days?  Yep, it's there.
Want to read about the campgrounds at the park?  We also provide that.
Are you interested in seeing what activities the parks support and offer?  Because we give you that information as well.
Vacation Planner will give you a well-informed decision making tool that will allow you to maximize your activities and get right to the fun!

## Description of the Working Program
1. Click on "Find Your Park"
2. A modal opens with all the states and U.S. territories that contain national parks.
3. Choose a state you are interested in visiting.
4. A second modal opens up giving you a list of the different parks located in that state.
5. Choose a park.
6. The choice of park fires off two different server APIs simultaneously: one for the weather and one for the park.
  * OpenWeather API
  * NPS API
7. With confirmation that the information is retrievable, we proceed to make multiple calls to retrieve other information, including weather, park information, campgrounds, alerts, and things to do, and we even change the background to provide a picture of how the park looks or wants to be seen
8. We provide a clean interface which the user can scroll up through for the different sections, allowing the user to take less time in making their decision
9. We provide a phone number and a button with access directly to the park's web site
10.  We provide today's park weather, and a forecast for the next three days
11.  The information about the park is stored in localStorage
  * The next time the user visits the page, as long as they do not delete their cache, when the user clicks on the "Find Your Park" button, a list of the last two previous parks will be provided for quick access
  * The list is in reverse order so that the newest chosen park is first.

## Risks and Milestones
* The NPS API can be very slow, depending on the data being downloaded
  * The amount of time to download a single state's park information took as long as 30 seconds at times
    * This was avoided by converting the park information in to an array of objects for each park
      * Risks:  If a new park is added, we would need to run a routine to manually update the localdata.js
      * Milestone: By doing it this was, we were able to decrease the responsiveness of the site exponentially, from 10-30 seconds for a list of parks down to milliseconds
* The NPS API tends to have missing information 
  * The amount inconsitent data gaps gave us trouble, especially on data that we tried to use with the OpenWeather API, which included zip code, latitude and longitude information
    * In order to compensate for the missing information, as special function was created to see if the information was populated
      * Risks:  Based on the number of parks that existed in multiple states, many of the latitude and longitude pieces of information were completely missing
      * Milestone:  We used the physical address of the main park visitor's center as a point of reference and passed its zip code to the OpenWeather API
* The COVID-19 pandemic has closed many of the National Parks
  * Because of this, events that we would like to have provided information for were canceled for safety reasons
    * Because of the lack of information, we were unable to provide a piece information we wanted to let the users see
      * Risks: The lack of information would normally not be noticed, but could be provided on the Park's web site
      * Milestone: We decided to change Events to Activities and were awarded with a large list of things that visitors could do at each park

## Technologies Used
* Foundation CSS
* OpenWeather API
* NPS API
* HTML
* CSS

## Websites
* [Portfolio](https://feuerbacherb.github.io/)
* [Vacation Planner Live](https://feuerbacherb.github.io/Vacation-Planner/)
* [Vacation Planner Repo](https://github.com/feuerbacherb/Vacation-Planner)

## Picture of Site
![Vacation Planner](https://feuerbacherb.github.io/Vacation-Planner/assets/images/VacationPlanner.jpg)