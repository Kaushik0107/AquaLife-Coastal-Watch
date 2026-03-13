AquaLife Coastal Watch – Workflow Flowcharts

This document explains the main workflow diagrams used in the AquaLife Coastal Watch system. These flowcharts describe how different components interact within the MERN stack architecture to support marine pollution reporting and wildlife monitoring.

1. Citizen Reporting Workflow

The Citizen Reporting Workflow describes the process through which a user reports marine pollution or wildlife sightings using the AquaLife web application.

First, a citizen accesses the AquaLife platform through the web interface built with React. The user uploads a geo-tagged image or video that captures the pollution event or wildlife sighting. The user then provides additional information such as the category of pollution, description of the incident, and other relevant metadata.

After submitting the form, the frontend sends the report data to the backend using a REST API request. The Node.js and Express server receives the request and performs authentication using JWT tokens. The server validates the report details and ensures that the uploaded data meets the required format.

Once validation is completed, the report is stored in the MongoDB database. The system then sends a confirmation message back to the user indicating that the report has been successfully submitted.

2. Image Processing Pipeline

The Image Processing Pipeline explains how uploaded images are processed by the system.

When a user uploads an image, the backend receives the image through the API. The system extracts metadata from the image, including the GPS location and timestamp. This information helps identify the geographic location of the reported event.

Next, the system performs preprocessing operations on the image. These operations may include resizing the image, reducing noise, and normalizing the data to prepare it for further analysis.

After preprocessing, the image is analyzed using an AI classification module. The module detects whether the image contains pollution such as plastic waste or oil spills, or if it contains marine wildlife sightings. Based on the classification results, the processed data is stored in the MongoDB database for further analysis.

3. Report Management Workflow

The Report Management Workflow describes how submitted reports are managed within the system.

When a user submits a report, the data is transmitted through the API gateway to the backend services. The report management service processes the request and assigns an initial status to the report.

Typically, the status is set to Pending, indicating that the report requires verification. The report information, including image data, location, and description, is stored in the reports collection within MongoDB.

Once stored, the report becomes visible in the administrative dashboard where moderators can review it.

4. Admin Moderation Workflow

The Admin Moderation Workflow explains how administrators verify user-submitted reports.

Administrators log into the system using the admin dashboard. The dashboard retrieves pending reports from the MongoDB database using REST API calls. Each report includes the uploaded image, location details, and classification results.

The administrator reviews the report carefully to determine whether it is valid. Based on the review, the administrator can approve or reject the report.

If the report is approved, it becomes visible in the public analytics dashboard and contributes to pollution monitoring statistics. If the report is rejected, the system marks it as invalid and prevents it from appearing in public data visualizations.

5. Data Storage Workflow

The Data Storage Workflow describes how system data is organized in the MongoDB database.

After backend processing, the application stores data in different collections within MongoDB. The primary collections include:

• Users Collection – Stores information about registered citizens and administrators.
• Reports Collection – Stores pollution reports and wildlife sightings submitted by users.
• Admin Collection – Stores administrative user data and moderation records.

The database acts as the central storage layer that supports the reporting system, analytics engine, and administrative operations.

6. Analytics and Monitoring Workflow

The Analytics and Monitoring Workflow explains how environmental data is analyzed and visualized.

The analytics engine retrieves stored report data from the MongoDB database. This data is processed to identify patterns such as pollution hotspots and frequent wildlife sightings.

The system analyzes trends over time and generates visual insights such as maps, charts, and statistical summaries. These insights are displayed in the analytics dashboard.

Environmental agencies and conservation organizations can use this dashboard to monitor coastal conditions and take necessary action to address pollution or protect marine wildlife.

7. Complete MERN System Workflow

The Complete MERN Workflow provides an overview of the entire system operation.

The process begins when a citizen submits a report through the React frontend. The report is transmitted to the backend via REST API requests. The Node.js and Express server authenticates the user and processes the uploaded data.

The system performs image processing and classification to identify pollution or wildlife sightings. After processing, the report is stored in the MongoDB database.

Administrators review and verify the submitted reports through the admin dashboard. Once verified, the data is used by the analytics engine to generate environmental insights.

These insights are displayed through the dashboard and help environmental agencies monitor marine ecosystems and respond to pollution incidents effectively.

8. Swimlane Workflow

The Swimlane Workflow represents the complete interaction between different participants involved in the AquaLife Coastal Watch system. This diagram divides the workflow into multiple lanes to clearly show which actor performs each activity in the system.

The main participants in the swimlane diagram are:

* Citizen

* System (Frontend and Backend)

* Admin Moderator

* Analytics and Environmental Agencies

Each lane represents the responsibilities and tasks performed by that participant.

1. Citizen Lane

The process begins with the citizen. A user opens the AquaLife Coastal Watch web application through a browser. The user navigates to the reporting interface and uploads a geo-tagged image or video of coastal pollution or marine wildlife.

The citizen then provides additional information such as the description of the incident, pollution category, or wildlife details. After entering the necessary data, the user submits the report to the system.

2. System Lane (Frontend and Backend)

Once the report is submitted, the React frontend sends the data to the backend using a REST API request.

The Node.js and Express backend receives the request and performs authentication using JWT tokens to verify the user. After authentication, the system validates the submitted data to ensure it meets the required format.

Next, the system performs image processing and optional AI classification to detect whether the uploaded image contains marine pollution or wildlife sightings.

After processing the data, the system stores the report information in the MongoDB database.

3. Admin Moderator Lane

After the report is stored in the database, it becomes available in the admin dashboard for verification.

The administrator logs into the system and reviews the submitted report. The admin checks the uploaded image, location information, and classification results to determine whether the report is valid.

The admin can then either approve the report or reject it. Approved reports are included in public analytics and monitoring dashboards, while rejected reports are marked invalid and removed from further analysis.

4. Analytics and Environmental Agencies Lane

Once a report is verified, the analytics engine retrieves the validated data from the database. The system analyzes pollution patterns and wildlife sightings across coastal regions.

The analytics results are visualized through dashboards and heatmaps that show pollution hotspots and wildlife activity. Environmental agencies and marine conservation organizations use these insights to monitor coastal environments and plan appropriate response actions.

Summary

The Swimlane Workflow provides a clear overview of the responsibilities of each participant in the AquaLife Coastal Watch system. It highlights how citizens contribute data, how the system processes and stores reports, how administrators verify information, and how environmental agencies use the analytics results for marine conservation.
