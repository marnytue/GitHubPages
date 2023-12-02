# Introduction/Background
  CCubed is an application that provides a quick and easy solution to groups, either professionally or leisurely, being able to find free time in their schedules. This application takes in the ability to compare calendars used in the most popular calendar applications (Microsoft and Google). This project improves and streamlines the meeting time dilemma and is an effortless solution to an often petty issue.
  
  The scope of this project is to develop an app that facilitates coordination of schedules between two users by allowing the user to login to their respective calendar provider to provide the app with direct access to their schedule, rather than having to manually enter it. The project is limited to the two most popular calendar providers: Google Calendar and Outlook. The app is also limited to two users to reduce algorithmic calculation complexity and manage database storage requirements. 
  
  The waterfall project management approach was used for this project. Due to the well-defined requirements and goals for the project, the waterfall method was most suitable. Its clear structure and reduced risk process allowed for fewer delays in executing the project.

# Literature Review
A key Component of this application was its ability to be built over already used applications such as Microsoft's Outlook Calendar and Google Calendars. Being able to work alongside these highly used calendar applications was the basis of the idea. Their APIs connect our application by being able to focus on the implementation of our idea rather than having to find a way to convert their calendars into our own format or make it more straining for the user. 

Our application diverges from the current application due to the fact that it can connect to the popular calendar apps and provides a real-time update for finding the availability. This distinction allows for any comparison meetings to be continuously used and recycled depending on the user's consent.

Furthermore, existing solutions like When2Meet require users to manually enter their available time slots in their website. While this provides for a simpler interface, it can create a more cumbersome experience for the user. Along with that most of the existing solutions require the user to manually update their available slots. Our solution, however, only requires the user to sign in to their respective calendar. 

# Software Technologies
**JavaScript:**
- Node.js: This serves as the backend of our application, which makes calls to Google calendar API and Microsoft calendar API, to gather event lists. This is also where we compare calendars and calculate free time.
- React.js: We used React to build the frontend of our application. This is where we implemented log in services for Google and Microsoft using firebase (mentioned below). And we also used it to display the Calendar, and once the user clicks on a date, they get a free time of that day.
- npm modules: to manage the package dependencies for both the frontend and backend.

**Storage:**
- Firebase: Used for login services, used GoogleAuth for google login and OAuth for Microsoft. And we used firebase to host our frontend.
- FireStore: Served as our events and authentication database. We saved users’ email, authentication token (to make the calendar API call), calendar events and some other information about a meeting, like its status, amount of users, etc..

**API:**
- Google Calendar API - to get an event list of the calendar when users signed in using their google account. These events were used in our calendar comparison logic.
- Microsoft Calendar API - to get an event list for users signing in with Microsoft accounts. They were also used in calendar comparison logic.
- Git/Github: as version control. And github pages to host this report.
- Google Cloud Platform: Used to host the backend of our application.

# Project Lifecycle
**Planning Stage:** 
We were able to begin planning shortly after the project requirements were released so that we were able to work in an efficient  manner. This stage began with us ensuring that we understood the project requirements and specifics for the deliverable. Then we began brainstorming on the project idea that could have potential for actual application while being unique. We analyzed that the selected project would satisfy all requirements while keeping a realistic scope. Once we agreed upon a project idea we broke up the team into 2 main groups: frontend & backend.

**Design Stage:**
Here we further discussed what are the key features that we needed for the project and began to create mockups of our project that would include these features. We did not stop there because we also put ourselves in the shoes of the stakeholders/users and asked “what other notable features will be nice to have”. From this, we selected additional features that we wanted to add. After all the high level thinking we began to select appropriate frameworks, architectural designs in the front & backend.  

**Implementation Stage:**
Up until this point we have been following a waterfall approach for the project and we saw fit to continue this since we knew our project requirements well. A notable thing to mention here is that at this stage we were able to have the frontend and backend be developed simultaneously. This was strongly possible with our consistent communication between the 2 teams. Each step along the way, we endured challenges as certain components in the front end were not working as properly and having authentication issues when logging in into our program in the backend but each team ensured every component worked correctly by writing test cases for the backend and simulating edge cases for the front end. As for progression of the project, we were roughly able to allocate a week for stages: requirements, design, and release. As for execution and testing, we have a little over 2 weeks and a week for each respectively. 
Methodologies and Processes.
As mentioned above, we followed the waterfall method. The first 3 stages are discussed above as for testing, information is discussed further below in the Testing section. Release is straightforward as it was just to deploy the program to the Google Cloud Platform. As for project management we kept a weekly checklist of what needed to be done that week while using Git & Github to ensure only functional and tested code was pushed to main. Required code review/approvals was implace to ensure this was the case. 

# Requirements
**Functional and Non-Functional Requirements**
- Functional Requirements:
  - Authentication of user whenever they log into their specified account (Google or Microsoft)
  - Consistent Real-Time updates whenever the calendar undertakes any changes
  - Visual updates to allow users to view when their availability is open and ability to view the specified time
  - Access to any meeting with the code in order to compare
- Non-Functional Requirements:
  - Update of the calendar will occur within 10 seconds of the change being made
  - Ability to log out of whichever account with Authentication in 20 seconds

**MMFs**
- Calendar Comparison
  - Displays a calendar with all days where there is mutual availability.
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
The process of identifying and prioritizing these requirements was based on real life experiences. Everyone in our group had used apps that were time consuming and error prone when it comes to figuring out free time. That’s why we prioritized integrating popular calendars like google and outlook calendars to calculate and provide the free times to our users. And to ensure that users see the change without having to log back in, for the convenience, we made real-time connection a requirement.
Design
Architecture Diagram

Class Diagram

Use Case Diagram

Design Patterns used:
Singleton Pattern: 
We implemented a singleton pattern for the EventParser and CalendarComparator classes.
The singleton pattern ensured we only had one instance of classes that only needed a single instance, thus providing easy access while limiting memory usage.
Module Pattern:
We implemented this specific design pattern to help keep our files small and all of their contents closely related.
This made the process of extending and implementing objects easier.
Testing
Tools:
Chai: JavaScript assertion library
Jest: JavaScript assertion library
White Box Testing:
Used Chai to certify backend interactions behave as expected.
Used Jest to certify that frontend interactions behave as expected.
Created extensive unit tests that tested all possible combinations of events for freetime array building.
Tested frontend with manual file upload before backend connections.
Black Box Testing:
Tested all implemented APIs using black box testing.
Firebase authentication endpoints tested.
Google and Outlook email login tested, along with backend calls to their APIs.
Integration Testing:
Performed extensive integration testing with manual verification.
Ensured all processes behaved as expected when frontend and backend were integrated.
Did regression testing to ensure backend-frontend integration did not produce new and unexpected behavior.
Conclusion
For this project, we adopted a test-driven development mindset and wrote unit tests for our classes before implementing them.
By doing this, we were able to ensure that we had code that could be demonstrated to work as intended.
Developing tests before our implementation saved us from discovering bugs at a point that made them prohibitively time intensive to fix.

GitHub repo link: https://github.com/SushGuha/Calendar

