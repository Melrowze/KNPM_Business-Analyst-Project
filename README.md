## KNPM Product Development Project: Building a Simple Project Management Tool"
![daria-nepriakhina-zoCDWPuiRuA-unsplash](https://github.com/Melrowze/KNPM/assets/44920093/2805f5a3-ba7c-4d71-8e59-a9c5f7d6d66e)
### Overview
---
Welcome to the presentation of our Project Management Tool project! In this project, we aimed to develop a comprehensive tool that enables efficient project management, similar to popular platforms like JIRA, Trello, Asana, or Monday. Our tool is designed to streamline project planning, tracking, and collaboration, ultimately enhancing productivity and success.

### Key Components
---
### Requirements Identification
---
We began by conducting thorough research and engaging with stakeholders to identify the key requirements for our project management tool. These requirements encompassed various aspects such as task management, team collaboration, progress tracking, and reporting.

### User Stories
---
Based on the identified requirements, we crafted detailed user stories that describe the desired functionality and features of our tool from the perspective of end users. These user stories served as a roadmap for development, guiding the design and implementation process.

[KNPM User_Stories.pdf](https://github.com/Melrowze/KNPM/files/15128195/KNPM.User_Stories.pdf)

### Database Design
---
To support the functionality of our project management tool, we designed a robust database using Entity-Relationship (ER) diagrams. The database schema was carefully crafted to efficiently store and retrieve project-related data, ensuring data integrity and scalability.

![KNPM_Database](https://github.com/Melrowze/KNPM/assets/44920093/362bc068-7240-4260-b2d4-2850a2e3b5e7)

### UML Activity Diagram
---
In addition to database design, we created UML activity diagrams to visualize the flow of activities and processes within our project management tool. These diagrams provided insights into how users interact with the system and navigate through different functionalities.

![Activity Diagram](https://github.com/Melrowze/KNPM/assets/44920093/218c45fc-9d32-4e25-ae87-9a1ee6cbe9c5)

### SQL Queries
---
To demonstrate the functionality of our database and its interaction with the project management tool, we developed a set of SQL queries for various entities such as tasks, projects, users, and teams. These queries enable data manipulation, retrieval, and reporting, facilitating seamless integration with the tool.

```sql

Sql queries for identified entities

User
CREATE TABLE "User" (
    "ID" integer  NOT NULL,
    "First_Name" varchar(64)  NOT NULL,
    "Last_Name" varchar(64)  NOT NULL,
    "Email" varchar(255)  NOT NULL,
    "Password" varchar(64)  NOT NULL,
    "Role_Name" varchar(64)  NOT NULL,
     PRIMARY KEY ("ID")
) ;

Role
CREATE TABLE "Role" (
    "ID" integer  NOT NULL,
    "Role_Name" varchar(64)  NOT NULL,
     PRIMARY KEY ("ID")
) ;


Team
CREATE TABLE "Team" (
    "ID" int  NOT NULL,
    "Team_Name" varchar(64)  NOT NULL,
     PRIMARY KEY ("ID")
) ;


Team member
CREATE TABLE "Team_Member" (
    "ID" integer  NOT NULL,
    "Team_ID" integer  NOT NULL,
    "User_ID" integer  NOT NULL,
    "Role_ID" integer  NOT NULL,
     PRIMARY KEY ("ID")
) ;

Project
CREATE TABLE "Project" (
    "ID" integer  NOT NULL,
    "Project_Name" varchar(128)  NOT NULL,
    "Project_Description" varchar(255)  NOT NULL,
    "User_ID" integer  NOT NULL,
     PRIMARY KEY ("ID")
) ;

Issue
CREATE TABLE "Issue" (
    "ID" integer  NOT NULL,
    "Project_ID" integer  NOT NULL,
    "Issue_Type" varchar(64)  NOT NULL,
    "Issue_Name" varchar(128)  NOT NULL,
    "Issue_Description" varchar(255)  NOT NULL,
    "Priority" varchar(64)  NOT NULL,
    "Start_Date" date  NOT NULL,
    "Due_Date" date  NOT NULL,
    "Status" varchar(64)  NOT NULL,
    "Assignment_ID" integer  NOT NULL,
     PRIMARY KEY ("ID")
) ;

Assignment
CREATE TABLE "Assignment" (
    "ID" integer  NOT NULL,
    "Role_ID" integer  NOT NULL,
    "User_ID" integer  NOT NULL,
     PRIMARY KEY ("ID")
) ;


```

## Conclusion
---
Our Project Management Tool project represents a comprehensive effort to develop a versatile and user-friendly platform for effective project management. By leveraging requirements analysis, user-centric design, database modeling, and SQL query development, we have created a solution that empowers teams to collaborate efficiently and achieve their project goals.

Thank you for your attention, and we look forward to showcasing our tool in action!
