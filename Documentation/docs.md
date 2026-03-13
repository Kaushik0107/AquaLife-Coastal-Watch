# AquaLife Coastal Watch – Marine Pollution Reporting System
## SDG Goal 14: Life Below Water

AquaLife Coastal Watch is a full-stack MERN web application designed to improve marine conservation through community participation. The platform allows citizens to report coastal pollution and wildlife sightings using a digital reporting system.

## ABSTRACT
## Problem Statement

Marine pollution in coastal areas is increasing due to plastic waste, oil spills, and illegal dumping. Traditional monitoring systems rely on manual surveys and government inspections.

Citizens often do not have an easy way to report environmental issues. As a result, pollution incidents may go unnoticed or be reported too late.

The lack of real-time monitoring systems makes it difficult for environmental authorities to identify pollution hotspots and respond quickly.

## Solution – AquaLife Coastal Watch System

AquaLife Coastal Watch is a community-driven web platform that allows users to:

Report marine pollution incidents

Upload geo-tagged images

Report wildlife sightings

View pollution hotspots on an interactive map

Track environmental reports

Moderators and environmental authorities can verify reports and manage environmental data using a centralized dashboard.

## Technologies Used

React.js (Frontend)

Node.js & Express.js (Backend)

MongoDB (Database)

Google Maps API (Location Tracking)

JWT (Authentication)

Cloud Storage (Image Upload)

## Outcome

The system:

Encourages community participation

Provides real-time environmental reporting

Helps identify coastal pollution hotspots

Supports faster environmental response

## CHAPTER 1: INTRODUCTION
## 1.1 Background

Marine ecosystems play a crucial role in maintaining biodiversity and ecological balance. However, coastal environments are increasingly threatened by pollution and environmental damage.

## Major threats include:

Plastic pollution

Oil spills

Industrial waste

Illegal dumping

Traditional monitoring systems rely on government inspections and environmental surveys, which are often slow and limited in coverage.

A digital platform that allows citizens to report environmental issues can significantly improve marine monitoring.

## 1.2 Problem Statement

Existing marine monitoring systems lack real-time reporting and public participation. Environmental authorities often receive delayed or incomplete information about pollution incidents.

Without proper monitoring systems, it becomes difficult to detect pollution hotspots and take immediate action.

## 1.3 Objectives

The objectives of AquaLife Coastal Watch are:

Enable citizens to report marine pollution

Collect geo-tagged environmental data

Visualize pollution hotspots on maps

Provide analytics dashboards for authorities

Promote awareness of marine conservation

## 1.4 Scope of the Project

The system includes:

Web-based citizen reporting platform

Geo-tagged image uploads

Marine pollution hotspot mapping

Wildlife sighting reporting

Administrative dashboard for verification

Environmental analytics visualization

## CHAPTER 2: LITERATURE SURVEY
## Traditional Marine Monitoring Systems

Traditional monitoring methods include:

Environmental surveys

Satellite monitoring

Laboratory water testing

These methods require specialized equipment and trained personnel, making large-scale monitoring difficult.

## IoT-Based Monitoring Systems

Some modern systems use IoT sensors to monitor water quality such as:

Temperature

pH level

Chemical contamination

However, installing IoT devices across large coastal areas is expensive.

## Citizen Science Platforms

Citizen science platforms allow the public to contribute environmental data through web or mobile applications.

## Improvement by AquaLife Coastal Watch

AquaLife improves existing systems by:

Enabling community-based reporting

Providing geo-tagged environmental data

Displaying pollution hotspots using maps

Supporting administrative verification

## CHAPTER 3: SYSTEM ANALYSIS
## 3.1 Existing System

Current monitoring systems include:

Government environmental inspections

Manual pollution reporting

Laboratory testing

Limitations

Lack of real-time monitoring

Limited geographic coverage

Slow response time

Lack of citizen participation

## 3.2 Proposed System

AquaLife Coastal Watch provides a digital reporting platform that allows community participation.

Features include:

Online pollution reporting

Centralized environmental database

Map-based pollution visualization

Moderator verification

Environmental analytics dashboard

## 3.3 Feasibility Study
Technical Feasibility

The project uses scalable and reliable technologies:

React.js

Node.js

MongoDB

Economic Feasibility

The system uses open-source technologies, reducing development costs.

Operational Feasibility

The platform has a user-friendly interface that allows users to easily submit environmental reports.

## CHAPTER 4: SYSTEM DESIGN
## 4.1 System Architecture

Architecture Overview:

Users / Moderators
↓
React Frontend
↓
Node.js + Express Backend (REST API)
↓
MongoDB Database
↓
Cloud Storage & Map Services

## 4.2 Data Flow Diagram
Level 0

Users → AquaLife Coastal Watch System → Moderators → Environmental Agencies

Level 1

Submission Phase

User submits pollution report

Data stored in database

Moderation Phase

Moderator reviews report

Approve or reject report

Approval Branch

Pollution hotspot map updated

Environmental analytics generated

Alert Branch

Authorities notified about severe pollution incidents

## 4.3 Database Design
## Users Collection

id

name

email

password

role (user/admin)

created_at

# Reports Collection

id

user_id

location

latitude

longitude

pollution_type

description

status (Pending / Approved / Rejected)

created_at

# Images Collection

id

report_id

image_url

uploaded_at

# Alerts Collection

id

report_id

message

created_at

## CHAPTER 5: IMPLEMENTATION
## 5.1 Frontend (React.js)

Components:

Login Component

Registration Component

Dashboard Component

Pollution Report Form

Map Component

Wildlife Sighting Component

Admin Dashboard

Report Verification Panel

## 5.2 Backend (Node.js + Express)

REST APIs:

POST /register-user

POST /login-user

POST /submit-report

GET /get-reports

PUT /verify-report

PUT /update-report-status

GET /heatmap-data

JWT is used for authentication.

## 5.3 Database Implementation

MongoDB with Mongoose schemas for:

Users

PollutionReports

WildlifeSightings

Notifications

## CHAPTER 6: RESULTS AND OUTPUT

The system successfully provides:

User Dashboard

Admin Dashboard

Pollution Reporting Interface

Wildlife Sighting Reporting

Map-Based Pollution Visualization

Features include:

Real-time environmental reporting

Map-based pollution hotspot visualization

Moderator verification workflow

Environmental analytics dashboard

## CHAPTER 7: CONCLUSION

AquaLife Coastal Watch demonstrates how digital technology and community participation can improve marine environmental monitoring.

The system provides an efficient platform for reporting coastal pollution and wildlife sightings, helping authorities respond quickly to environmental threats.

## CHAPTER 8: FUTURE ENHANCEMENTS

Future improvements may include:

AI-based marine pollution detection

Drone-based coastal monitoring

IoT water quality sensors

Mobile application version

Advanced environmental analytics dashboard

## AUTHOR

Project Developed By: ANSBID
Project Name: AquaLife Coastal Watch
Technology Stack: MERN Stack
SDG Goal: SDG 14 – Life Below Water
Year: 2026
