# Business Requirements Document  
Optimize the online classroom booking system at a university by integrating IoT sensors (for detecting room availability and temperature) and the student database for user authentication. The project aims to reduce booking conflicts, increase room utilization rates, and enhance the user experience.


---

## 1. System Components and Design
### Purpose  

The client is the university facilities management team – the system should enable efficient room booking for students and lecturers, integrating IoT sensor data (occupancy, temperature) to suggest optimal rooms and reduce booking conflicts.  
The system should provide a web-based interface for booking, support user authentication via the student database, and allow offline data access for admins.  
The system should track room usage analytics to optimize facility management.  

### System Background  

- **Problem** – high booking conflicts (10% of bookings) and low room utilization (50% of rooms underused) due to manual processes and lack of real-time data.  
- **Database** – stores user information, room bookings, IoT sensor data (occupancy, temperature), and system logs.  
- **Frontend** – web interface for students/lecturers to book rooms, view IoT-based suggestions, and access schedules; admin interface for managing bookings and analytics.  
- **Backend** – processes IoT data, integrates with student database for authentication, and supports offline data access for admins.  
- **IoT Integration** – collects real-time data from sensors to inform booking decisions.  


## 2. Objectives and Goals  

- Reduce booking conflicts to under 5% by validating room availability with IoT data.  
- Increase room utilization by 30% through IoT-based room suggestions.  
- Reduce average booking time to 2 minutes via an intuitive web interface.  
- Authenticate 100% of users via the student database.  
- Provide admins with offline access to booking data and online editing capabilities.  
- Track changes made by admins and manage multiple user roles (student, lecturer, admin).  
- Notify admins of IoT sensor malfunctions or maintenance needs.  
- Offer a web interface for users to view schedules and analytics dashboards for admins.  


## 3. Requirements  

### 3.1. Nonfunctional Requirements  

#### Performance Requirements  

- System should be web-based, accessible via desktop and mobile browsers.  
- Page load times should not exceed 1.5 seconds for 90% of users.  
- IoT data should refresh every 5 minutes to ensure real-time accuracy.  
- System updates should occur quarterly or as needed, with downtime not exceeding 1 hour.  

#### Platform Constraints  

- Web frontend should run on major browsers (Chrome, Firefox, Safari, Edge) and adapt to mobile devices.  
- Backend requires a relational database (e.g., MySQL) to store user, booking, and IoT data.  
- IoT integration requires an API to communicate with sensor hardware.  
- Offline access requires local caching for admin devices.  

#### Accuracy and Precision  

- System uses session tokens to distinguish users after login.  
- Passwords are case-sensitive; other inputs (e.g., room type) are not.  
- Admins receive immediate notifications for critical errors (e.g., sensor failure, database outage).  
- Daily reports summarize non-critical errors (e.g., failed login attempts).  

#### Adaptability   

- User management (add/remove/modify) is handled via the admin interface without code changes.  
- Web app adapts to browser updates via regular maintenance.  
- IT admin requires full database access and server access for system updates.  
- IoT API should support backward compatibility for sensor firmware updates.  

#### Security  

- Users require a username and password for login, validated against the student database.  
- HTTPS secures data exchange between client and server.  
- Accounts lock after 5 failed login attempts; admins are notified of potential brute force attacks.  
- Forgotten passwords trigger an email with a temporary password and a reset link.  
- Optional 2FA via email for enhanced security.  


### 3.1. Functional Requirements  

- The system shall validate user credentials against the student database during login.  
- The system shall display real-time room availability based on IoT sensor data (occupancy, temperature).  
- The system shall suggest optimal rooms based on user preferences and IoT data.  
- The system shall prevent booking conflicts by cross-checking IoT data and existing bookings.  
- The system shall allow users to book rooms via a web interface.  
- The system shall allow admins to manage bookings (add/remove/modify) online.  
- The system shall provide offline access to booking data for admins.  
- The system shall track changes made by admins and log user roles.  
- The system shall notify admins of IoT sensor malfunctions via email.  
- The system shall generate analytics dashboards for room usage using Power BI.  


## 4. User Interface  

**What are the needs of the interface? Who are the different users for this interface? What will each user need to be able to do through the interface? How will the user interact with the interface?**  

- The UI is web-based, adaptive for desktop and mobile browsers.  
- **Users:** Students, lecturers, admins, and facilities management.  
  - **Students/Lecturers:** Book rooms, view schedules, receive IoT-based room suggestions, and manage account details.  
  - **Admins:** Manage bookings, view analytics dashboards, and override conflicts.  
  - **Facilities Management:** Access room usage reports and IoT sensor status.  
- Interaction via browser with intuitive navigation (e.g., filters for room type, time slot).  


## 5. Assumptions  


- Users have access to modern web browsers and university login credentials.  
- IoT sensors provide accurate occupancy and temperature data.  
- The student database is up-to-date and accessible via API.  
- The university IT team handles server maintenance and backups.  


## 6. Limitations  

- Project timeline limited to 12 weeks for BA deliverables.  
- Dependency on third-party IoT sensor reliability.  
- Inability to predict browser updates that may affect compatibility.  
- Limited budget for advanced IoT hardware testing.  
- Limited resources for extensive user training.  


## 7. Gantt Chart  

**Please include a screenshot of the GANTT chart that you created with Lucidchart.**  

> [Gantt Chart Placeholder: A Lucidchart Gantt chart will be created to outline the 12-week project timeline, including tasks such as requirement gathering (2 weeks), process modeling (1 week), data mapping (1 week), prototyping (2 weeks), data analysis (2 weeks), UAT planning (1 week), and stakeholder communication (ongoing). Due to text-based response limitations, a screenshot cannot be included here. I can guide you to create this in Lucidchart if needed.]
