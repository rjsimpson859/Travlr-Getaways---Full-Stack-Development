# cs465-fullstack
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

This course has been instrumental in my professional growth. Juggling work with my studies made it challenging to define my post-graduation career path, including which programming languages intrigued me and whether I preferred front-end or back-end development. However, this course has provided clarity, guiding me towards a specific career direction and highlighting the additional skills essential for competitiveness in the job market. One of the most significant skills I've honed through this experience is comprehending the interconnection between different modules or components of code, understanding how they collaborate to construct a finalized product.
