# Travlr Getaways
## CS 465 Project Software Design Document
### Version 3.0

## Table of Contents
- [Document Revision History](#document-revision-history)
- [Instructions](#instructions)
- [Executive Summary](#executive-summary)
- [Design Constraints](#design-constraints)
- [System Architecture View](#system-architecture-view)
  - [Component Diagram](#component-diagram)
  - [Sequence Diagram](#sequence-diagram)
  - [Class Diagram](#class-diagram)
  - [API Endpoints](#api-endpoints)
- [The User Interface](#the-user-interface)

## Document Revision History
| Version | Date       | Author       | Comments                                          |
|---------|------------|--------------|---------------------------------------------------|
| 1.0     | 07/16/2023 | Roy Simpson  | Updated Executive Summary, Design constraints, and Described Component Diagram |
| 2.0     | 07/30/2023 | Roy Simpson  | Updates Sequence Diagram, Class Diagram, and API Endpoints |
| 3.0     | 08/13/2023 | Roy Simpson  | Added Screenshots and provided further details to the User Interface section |


## Executive Summary
Travlr Getaways is a web application that enables users to securely book trips. This web application includes a user interface, backend, and a database. We used MEAN (MongoDB, Express, Angular, and Node) stack for the development of this web application. The benefit of using the MEAN stack is that they are all can be written in JavaScript, allowing the development process to integrate quickly and flexibly. The customer-facing side of the application will allow the users to book vacation rentals, providing them with the price and number of nights. The administrator single-page application (SPA) will allow for updating the trip availability.

## Design Constraints
Some design constraints present in this web application development process include scalability. Using the MEAN stack for a very large-scale application may not be ideal. If the web application incurs a large flow of traffic, there is a possibility of data loss when MongoDB is writing large numbers of documents. We have yet to develop a security feature to authenticate user login to allow users to access their secure travel details. Security features are necessary in a web application to ensure the users data is protected.

## System Architecture View
### Component Diagram
ComponentDiagram.jpg

The overall system architecture of the web application is demonstrated above in the component diagram. The client component consists of the user interface, where users can access the web application on a web browser component. The web browser component allows the user to access the Traveler Portfolio component. The Traveler Portfolio component contains access to the Graphic Library component and the Database Component. For this web application, the Database Component is MongoDB, the database where the information is stored for trips and alike information. The MongoDB component is also connected to the Mongoose ODM component in the Server Component. The Server Component includes the Authentication Server, which is used to authenticate the Client Session component.

### Sequence Diagram
The flow of logic in the web application is displayed in the sequence diagram. The front end is in charge of managing the user interface and user inputs, receives this request. The back end is in charge of managing the business logic and data storage for the web application. This request includes data storage such as travel search. The Actor will open the browser, access the web application, Sign In with valid credentials. The Actor will then be able to search for available trips. The Actor is inputting username and password into the front end. The front end is then requesting validation from the back end. The back end then returns authentication or not.

### Class Diagram
Based on the class diagram, Itinerary represents a travel itinerary that includes various travel components like flight, hotel, and cruise. The Itinerary Class has a start date, end date, origin, and destination for cruise, flight, and hotel info. CruiseInfo Class contains name, cabin type and price. FlightInfo Class contains name, seatclass, and price. HotelInfo Class contains name, star, location, roomrequested, and price. The TripInfo Class contains totalprice, totalmiles, and stopover from the CruiseInfo, FlightInfo, and HotelInfo Classes. HotelBooking, CruiseBooking, and FlightBooking classes handle the booking process for their respective travel components. Travel_Agent class contains BookPackage, BookFlight, BookHotel, and BookCruise. MemberAccount class contains membernumber, frequent_airline, memberstatus, and memberclub.

## API Endpoints
| Method | Purpose | URL | Notes |
|--------|---------|-----|-------|
| GET    | Retrieve list of things | /api/things | Returns all active things |
| GET    | Retrieve single thing | /api/things/:thingId | Returns single thing instance, identified by the thing ID passed on the request URL |
| POST   | Create new list of things | /api/things | Create a new list of things |
| POST   | Create a single thing | /api/things/:thingId | Create a single thing, identified by the thing ID passed on the request URL |
| PUT    | Update the full list of things | /api/things | Updates and replaces entire list of things. |
| PUT    | Update a single thing | /api/things/:thingId | Updates and replaces a single thing, identified by the thing ID passed on the request URL |
| PATCH  | Update full list of things | /api/things | Update a full list of things and modify the list of things. |
| PATCH  | Update or modify a single thing | /api/things/:thingId | Update and modify a single thing, identified by the thing ID passed on the request URL |
| DELETE | Delete a list of things | /api/things | Delete all the list of things. |
| DELETE | Delete a single thing | /api/things/:thingId | Delete a single thing, identified by the thing ID passed on the request URL |

## The User Interface
![Unique Trip](link-to-unique-trip-screenshot)
*Figure 1: Screenshot of a unique trip, added*

![Edit Screen](link-to-edit-screen-screenshot)
*Figure 2: Screenshot of the Edit screen*

![Update Screen](link-to-update-screen-screenshot)
*Figure 3: Screenshot of the Update screen*

The Angular project structure is different from that of the Express HTML customer-facing page, in terms of component-driven development. Some advantages and disadvantages of the SPA functionality include seamless user experiences, faster navigation, and reduced server load but may face SEO challenges and initial load time concerns. The process of testing to make sure the SPA is working with the API to GET and PUT data in the database include unit and integration tests, encountering CORS issues.



# Travlr Getaways - Full Stack Development
CS-465 Full Stack Development with MEAN.
### Architecture 
Through this project, I gained hands-on experience in utilizing Express HTML, JavaScript, and building a Single Page Application (SPA). The backend infrastructure relied on Node.js and Express to serve the website while establishing connectivity with a MongoDB database. Leveraging the scalability and adaptable nature of NoSQL databases, we capitalized on MongoDB's capacity to accommodate dynamic changes. Additionally, the integration of Mongoose facilitated efficient data collection and object modeling.

On the frontend, we crafted a responsive SPA using Angular. Employing a SPA architecture significantly enhanced the site's navigation speed, ensuring swift loading times for a seamless user experience.

### Functionality

Distinguishing JSON from JavaScript lies in its standardized format for object data representation, easily interpretable by JavaScript to construct literal JavaScript objects. This streamlined compatibility facilitates JavaScript's seamless transformation of data into JavaScript objects, thereby bridging the gap between frontend and backend development. JSON serves as a conduit for storing data or JavaScript objects on the backend, accessible for various purposes as requested by the frontend. This centralized data storage eliminates redundancy, allowing for versatile utilization without repetitive storage.

Regarding code refactoring in the full stack process to enhance functionality and efficiency, a significant instance involved optimizing the trip card and trip list components. Originally, maintaining two separate components rendering identical information proved inefficient. Instead, rendering each trip as a distinct element within the whole system significantly improved the site's overall functionality. Reusing UI components offers manifold benefits, reducing the application's overall size, expediting the development process, and mitigating the introduction of errors or vulnerabilities into the system, given the component's security.

### Testing

Validating request and retrieval methods involves conducting diverse API endpoint tests, often compounded by the complexities of testing within secure environments.

Preliminary testing of endpoints typically occurs prior to implementing security measures. One approach involves navigating to the local web address corresponding to the API endpoint, checking for successful data loading or identifying potential errors. Utilizing dedicated applications like Postman for testing HTTP requests is advantageous. Postman not only facilitates endpoint testing but also allows for the inclusion of security measures, ensuring thorough evaluation even within secured endpoints.

In a comprehensive full stack application, the methods deployed dictate the operational dynamics of a webpage. HTTP request methods such as GET, POST, PUT, and DELETE play a pivotal role in retrieving or modifying the database to implement functionality. On the backend, these methods are executed by employing database functions (e.g., .create, .findOne, .find, .findOneAndUpdate) to suit the client's requirements. Endpoints, observable on the admin or client side, reflect the outcomes of these methods. Rigorous testing of endpoints ensures their proper functionality, data display, and error handling.

Security constitutes an additional layer of code implementation aimed at thwarting unauthorized access or modifications to the database. For instance, protecting sensitive API endpoints, such as adding or editing trips in the database, is crucial to prevent unauthorized tampering. This added security layer ensures that only authorized and authenticated users can access and modify the database.

### Reflection

This course has been instrumental in my professional growth. It was challenging to define my post-graduation career path, including which programming languages intrigued me and whether I preferred front-end or back-end development. However, this course has provided clarity, guiding me towards a specific career direction and highlighting the additional skills essential for competitiveness in the job market. One of the most significant skills I've honed through this experience is comprehending the interconnection between different modules or components of code, understanding how they collaborate to construct a finalized product.
