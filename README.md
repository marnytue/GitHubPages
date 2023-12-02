# Group3_Project2_Report

## Introduction/Background

CCubed is an application that provides a quick and easy solution to groups, either professionally or leisurely, being able to find free time in their schedules. This application takes in the ability to compare calendars used in the most popular calendar applications (Microsoft and Google). This project improves and streamlines the meeting time dilemma and is an effortless solution to an often petty issue.

The scope of this project is to develop an app that facilitates coordination of schedules between two users by allowing the user to login to their respective calendar provider to provide the app with direct access to their schedule, rather than having to manually enter it. The project is limited to the two most popular calendar providers: Google Calendar and Outlook. The app is also limited to two users to reduce algorithmic calculation complexity and manage database storage requirements.

The waterfall project management approach was used for this project. Due to the well-defined requirements and goals for the project, the waterfall method was most suitable. Its clear structure and reduced risk process allowed for fewer delays in executing the project.

## Literature Review

A key Component of this application was its ability to be built over already used applications such as Microsoft's Outlook Calendar and Google Calendars. Being able to work alongside these highly used calendar applications was the basis of the idea. Their APIs connect our application by being able to focus on the implementation of our idea rather than having to find a way to convert their calendars into our own format or make it more straining for the user.

Our application diverges from the current application due to the fact that it can connect to the popular calendar apps and provides a real-time update for finding the availability. This distinction allows for any comparison meetings to be continuously used and recycled depending on the user's consent.

Furthermore, existing solutions like When2Meet require users to manually enter their available time slots in their website. While this provides for a simpler interface, it can create a more cumbersome experience for the user. Along with that most of the existing solutions require the user to manually update their available slots. Our solution, however, only requires the user to sign in to their respective calendar.

## Software Technologies

### JavaScript:
- **Node.js:** Backend for making calls to Google calendar API and Microsoft calendar API, to gather event lists and compare calendars for free time calculation.
- **React.js:** Frontend implementation for login services, displaying the Calendar, and showing free time upon clicking a date.

### Storage:
- **Firebase:** Used for login services, hosting the frontend, and authentication database.
- **Firestore:** Database for storing users’ email, authentication token, calendar events, and meeting information.

### API:
- **Google Calendar API:** Retrieve event lists for calendar comparison logic.
- **Microsoft Calendar API:** Retrieve event lists for calendar comparison logic.

### Other Tools:
- **Git/Github:** Version control and hosting the report.
- **Google Cloud Platform:** Used to host the backend of the application.

## Project Lifecycle

### Planning Stage:
- Understanding project requirements and defining the project idea.
- Breaking the team into frontend & backend groups.

### Design Stage:
- Identifying key features, creating mockups, and selecting frameworks.
- Choosing additional features for implementation.

### Implementation Stage:
- Developing frontend and backend simultaneously.
- Overcoming challenges in development and ensuring functionality through testing.

## Methodologies and Processes

### Waterfall Method:
- Sequential stages: requirements, design, release, execution, and testing.
- Weekly checklist for project management, using Git & Github for version control and code review.

### Requirements

#### Functional Requirements:
- Authentication of users upon login.
- Real-time updates on calendar changes.
- Visual representation of availability.
- Access to meetings for comparison.

#### Non-Functional Requirements:
- Calendar update within 10 seconds.
- Log out with authentication within 20 seconds.

#### MMFs (Minimal Marketable Features)
- Calendar Comparison: Displays mutual availability, specific day view, and keeps events private.
- Popular Calendar Integration: Allows login and access to Microsoft and Google calendars.
- Real-Time Connection: Refreshes comparisons on calendar change, enables continuous tracking of openings, and avoids the need for new meeting sessions.

## Design

### Architecture Diagram

### Class Diagram

### Use Case Diagram

#### Design Patterns used:
- **Singleton Pattern:** Implemented for EventParser and CalendarComparator classes for memory efficiency.
- **Module Pattern:** To organize files and contents for easier extension and implementation.

## Testing

### Tools:
- **Chai:** JavaScript assertion library for backend.
- **Jest:** JavaScript assertion library for frontend.

### White Box Testing:
- Certification of backend and frontend interactions.
- Extensive unit tests for freetime array building.

### Black Box Testing:
- Testing implemented APIs and Firebase authentication endpoints.

### Integration Testing:
- Verification of frontend-backend integration.
- Regression testing to ensure expected behavior post-integration.

## Conclusion

For this project, a test-driven development mindset was adopted, writing unit tests before implementation. This approach ensured code demonstration aligned with intended functionality, saving time in bug discovery and fixing.

[GitHub repo link](https://github.com/SushGuha/Calendar)
