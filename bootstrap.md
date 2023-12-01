# Introduction/Background
Offer an overview of the project's context and significance.
	CCubed is an application that provides a quick and easy solution to groups, either professionally or leisurely, being able to find free time in their schedules. This application takes in the ability to compare calendars used in the most popular calendar applications (Microsoft and Google). This project improves and streamlines the meeting time dilemma and is an effortless solution to an often petty issue.
Define the project scope and your project management approach.
	
# Literature Review
Discuss related work and how your project aligns with or diverges from existing solutions or methodologies.
  A key Component of this application was its ability to be built over already used applications such as Microsoft's Outlook Calendar and Google Calendars. Being able to work alongside these highly used calendar applications was the basis of the idea. Their APIs connect our application by being able to focus on the implementation of our idea rather than having to find a way to convert their calendars into our own format or make it more straining for the user. 
	Our application diverges from the current application due to the fact that it can connect to the popular calendar apps and provides a real-time update for finding the availability. This distinction allows for any comparison meetings to be continuously used and recycled depending on the user's consent.
Furthermore, existing solutions like When2Meet require users to manually enter their available time slots in their website. While this provides for a simpler interface, it can create a more cumbersome experience for the user. Along with that most of the existing solutions require the user to manually update their available slots. Our solution, however, only requires the user to sign in to their respective calendar. 

# Software Technologies
Detail the technologies, tools, and frameworks used.
Justify the selection of these technologies.
JavaScript:
Node.js: This serves as the backend of our application, which makes calls to Google calendar API and Microsoft calendar API, to gather event lists. This is also where we compare calendars and calculate free time.
React.js: We used React to build the frontend of our application. This is where we implemented log in services for Google and Microsoft using firebase (mentioned below). And we also used it to display the Calendar, and once the user clicks on a date, they get a free time of that day.
npm modules: to manage the package dependencies for both the frontend and backend.
Storage:
Firebase: Used for login services, used GoogleAuth for google login and OAuth for Microsoft. And we used firebase to host our frontend.
FireStore: Served as our events and authentication database. We saved users’ email, authentication token (to make the calendar API call), calendar events and some other information about a meeting, like its status, amount of users, etc..
API:
Google Calendar API - to get an event list of the calendar when users signed in using their google account. These events were used in our calendar comparison logic.
Microsoft Calendar API - to get an event list for users signing in with Microsoft accounts. They were also used in calendar comparison logic.
Git/Github: as version control. And github pages to host this report.
Google Cloud Platform: Used to host the backend of our application.

# Project Lifecycle
Describe the stages of your project's development.
Planning Stage:
Design Stage:
Implementation Stage:
Explain the methodologies and processes implemented.

# Requirements
Document both Functional and Non-Functional Requirements.
Functional Requirements:
Authentication of user whenever they log into their specified account (Google or Microsoft)
Consistent Real-Time updates whenever the calendar undertakes any changes
Visual updates to allow users to view when their availability is open and ability to view the specified time
Access to any meeting with the code in order to compare
Non-Functional Requirements:
Update of the calendar will occur within 10 seconds of the change being made
Ability to log out of whichever account with Authentication in 20 seconds
Make sure to mention the 3 MMFs in detail here
Calendar Comparison
Displays a calendar with all days where there is mutual availability.
Pressing a specific day allows viewing of all the available times during that day.
Keeps conflict details and events private.
Popular Calendar Integration
Allow users to login to their Microsoft accounts and access their Outlook calendars.
Allow users to login to their Google accounts and access their Google calendars.
Integration with popular calendar apps prevents the tedious process of exporting and uploading calendar files manually.
Real-Time Connection
Refreshing the calendar comparison page reruns freetime comparison calculations if a user changes their calendar.
Allows users to continuously keep track of each other's openings.
Avoids the need for making new meeting sessions after every calendar update.
Discuss the process of identifying and prioritizing these requirements.

# Design
Present architectural and low-level design diagrams.
Explain your design decisions and their impact.
Design Patterns used:
Singleton Pattern:
Module Pattern:

# Testing
Elaborate on the Test Strategy, including whitebox and blackbox testing methods.
List various tools used for testing and explain their purpose.
Provide detailed test cases and their outcomes.
Discuss how testing influenced the development process and the final product.


