# Database Design – AquaLife Coastal Watch

## Overview

The **AquaLife Coastal Watch** platform uses **MongoDB** as its database system as part of the MERN stack (MongoDB, Express.js, React.js, Node.js). MongoDB is a document-based NoSQL database that provides flexibility and scalability for storing user-generated environmental monitoring data.

The database design is organized into four main collections: **Users, Reports, Images, and Locations**. These collections store information related to user accounts, environmental reports, uploaded images, and geographic data associated with the reports.

The design ensures efficient storage, retrieval, and management of pollution reports and wildlife sightings submitted by citizens.

---

# Collections in the Database

## 1. Users Collection

The **Users** collection stores information about individuals who access the system. This includes both citizen users who submit environmental reports and administrators who manage and moderate the reports.

### Fields

* **userId** – Unique identifier for each user
* **name** – Name of the registered user
* **email** – Email address used for login and communication
* **password** – Encrypted password for authentication
* **role** – Defines whether the user is a *citizen* or an *admin*
* **createdAt** – Timestamp representing when the user account was created

### Purpose

This collection is responsible for managing user authentication and tracking which user submitted a report.

---

## 2. Reports Collection

The **Reports** collection is the central component of the database. It stores all pollution and wildlife sighting reports submitted by users.

### Fields

* **reportId** – Unique identifier for each report
* **userId** – Reference to the user who submitted the report
* **title** – Title describing the report
* **description** – Detailed explanation of the environmental observation
* **category** – Type of report (e.g., pollution or wildlife sighting)
* **imageId** – Reference to the uploaded image associated with the report
* **locationId** – Reference to the geographic location where the report was created
* **status** – Status of the report (pending, approved, rejected)
* **createdAt** – Timestamp indicating when the report was submitted

### Purpose

The Reports collection stores environmental incidents and enables administrators to review and moderate citizen submissions.

---

## 3. Images Collection

The **Images** collection stores information about images uploaded with environmental reports.

### Fields

* **imageId** – Unique identifier for the image
* **imageUrl** – URL or path where the image is stored
* **uploadedBy** – Reference to the user who uploaded the image
* **uploadedAt** – Timestamp indicating when the image was uploaded

### Purpose

Separating images into a dedicated collection improves system organization and allows easier management of uploaded media files.

---

## 4. Locations Collection

The **Locations** collection stores geographic coordinates associated with environmental reports.

### Fields

* **locationId** – Unique identifier for the location
* **latitude** – Latitude coordinate of the reported location
* **longitude** – Longitude coordinate of the reported location
* **placeName** – Name of the coastal area or location

### Purpose

This collection enables the system to store geo-tagged information and display reports on an interactive map for environmental monitoring.

---

# Relationships Between Collections

The collections in the AquaLife Coastal Watch database are logically connected to support the system’s functionality.

* **Users → Reports**
  A user can submit multiple environmental reports.

* **Reports → Images**
  Each report may contain an image representing the environmental issue or wildlife sighting.

* **Reports → Locations**
  Each report is associated with a geographic location where the event occurred.

* **Admins → Reports**
  Administrators review and moderate submitted reports by updating the report status.

---

# Summary

The database design for AquaLife Coastal Watch provides a structured approach for managing environmental reporting data. By organizing information into logical collections and maintaining relationships between them, the system supports efficient user management, report tracking, image storage, and geo-location mapping for environmental monitoring.
