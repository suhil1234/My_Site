Event Management Web Application Documentation


Contents
Project Overview	2
Project Structure	2
Key Features	2
Controllers	4
Views	4
Models	4
JavaScript Files	5
Home.js	5
Misc.js	5
DataTable.js	5
Middleware	5
Styling and Assets	5









Project Overview
The Event Management Web Application is designed to facilitate the management of events, participants, and locations. It provides functionalities for viewing, editing, and tracking event participation, ensuring an organized approach to event planning and execution.
Project Structure
+---Areas
¦   +---Admin
¦       ¦   _ViewImports.cshtml
¦       ¦   _ViewStart.cshtml
¦       ¦   
¦       +---Controllers
¦       ¦       AccessListController.cs
¦       ¦       ErrorController.cs
¦       ¦       EventController.cs
¦       ¦       HomeController.cs
¦       ¦       LocationController.cs
¦       ¦       ParticipantController.cs
¦       ¦       
¦       +---Views
¦           +---AccessList
¦           ¦       Edit.cshtml
¦           ¦       List.cshtml
¦           ¦       
¦           +---Error
¦           ¦       403.cshtml
¦           ¦       404.cshtml
¦           ¦       500.cshtml
¦           ¦       
¦           +---Event
¦           ¦       Edit.cshtml
¦           ¦       List.cshtml
¦           ¦       
¦           +---Home
¦           ¦       Index.cshtml
¦           ¦       
¦           +---Location
¦           ¦       Edit.cshtml
¦           ¦       List.cshtml
¦           ¦       
¦           +---Participant
¦           ¦       Edit.cshtml
¦           ¦       List.cshtml
¦           ¦       
¦           +---Shared
¦                   _Layout.cshtml
¦                          
+---BL
¦       ClsAccessList.cs
¦       CLsEvents.cs
¦       CLsLocations.cs
¦       ClsParticipants.cs
¦       ClsSummary.cs
¦       
+---Middlewares
¦       IpBlockingMiddleware.cs
¦       
+---Models
¦       EventManagementContext.cs
¦       TbAccessList.cs
¦       TbEvent.cs
¦       TbEventParticipant.cs
¦       TbLocation.cs
¦       TbParticipant.cs
¦       VwEventParticipationSummary.cs
¦       VwVenueCapacityStatus.cs
¦       
+---wwwRoot
    +---Admin
        +---css
        ¦   +---demo_1
        ¦           style.css
        ¦           style.css.map
        ¦           
        +---fonts
        ¦           
        +---images
        ¦       logo-mini.svg
        ¦       logo.svg
        ¦       
        +---js
        ¦       data-table.js
        ¦       Home.js
        ¦       misc.js
        ¦       
        +---scss
        ¦             
        +---vendors
            
Key Features
•	Event Management: Create, edit, and view events.
•	Participant Tracking: Track participants for each event.
•	Location Management: Manage venues and their capacities.
•	Responsive Design: Accessible from various devices.
•	Data Tables: Search, paginate, and order event data easily.
Controllers
The application consists of several controllers, each handling specific functionalities:
•	AccessListController: Manages access control and permissions.
•	ErrorController: Handles error pages (403, 404, 500).
•	EventController: Manages event operations.
•	HomeController: Displays the home page and event summaries.
•	LocationController: Handles location-related functionalities.
•	ParticipantController: Manages participant data.
Views
The views are organized under the Areas/Admin/Views directory, allowing for clear separation of concerns. Key views include:
•	AccessList: Edit and list access controls.
•	Event: Edit and list events.
•	Location: Edit and list locations.
•	Participant: Edit and list participants.
•	Error: Custom error pages.
•	Home: Dashboard with event participation summaries.
Models
The models represent the data structure of the application and include:
•	TbEvent: Represents event data.
•	TbParticipant: Represents participant data.
•	VwEventParticipationSummary: A view model for summarizing event participation.
•	VwVenueCapacityStatus: A view model for venue capacity tracking.
JavaScript Files
Home.js
Purpose: Handles the initialization of charts and dynamic updates based on user interactions.
Key Functions:
•	Search: Redirects to a search page based on the selected location.
•	initializeChart: Initializes a doughnut chart displaying current participants and available capacity.
Misc.js
Purpose: Manages the navigation bar's active state and sidebar functionality.
Key Functions:
•	Sets the active class on the current navigation item based on the URL.
•	Handles sidebar collapse and minimize functionality.
DataTable.js
Purpose: Enhances data tables with search, pagination, and ordering capabilities.
Key Functions:
•	Initializes the DataTable plugin with custom settings.
•	Adds placeholders for search input and adjusts form control classes for better styling.
Middleware
•	IpBlockingMiddleware: Monitors and blocks requests based on IP settings to enhance security.
Styling and Assets
The application utilizes custom CSS and third-party libraries located in the wwwRoot/Admin/css and wwwRoot/Admin/vendors directories. Ensure to maintain styles consistent with the overall design.
Usage Instructions
1.	Accessing the Application: Navigate to /admin/Home to view the dashboard.
2.	Managing Events: Use the Event section to create, edit, or list events.
3.	Tracking Participants: Access the Participant section to manage attendee information.
4.	Viewing Reports: Utilize the Home page for quick summaries of event participation.

