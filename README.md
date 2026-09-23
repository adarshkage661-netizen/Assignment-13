Employee Leave – Leave Request

📌 Project Overview

Employee Leave – Leave Request is a database/software system designed to manage employee leave requests in an organization.

The system stores employee details, departments, leave types, leave requests, and approval statuses. It provides a structured process for submitting and managing leave requests and helps maintain accurate leave records.

This project is designed as a BCA / Computer Science academic project.

---

🎯 Problem Statement

Develop a system for managing employee leave requests with the following features:

1. Employee Details
2. Department
3. Leave Request
4. Leave Type
5. Approval Status

The system should allow employees to submit leave requests and enable the concerned authority or manager to review and approve or reject them.

---

✨ Features

1. Employee Details

Stores:

- Employee ID
- Employee Name
- Email
- Contact Number
- Department

2. Department

Stores:

- Department ID
- Department Name
- Description

3. Leave Request

Stores:

- Request ID
- Employee ID
- Leave Type
- Approval Status
- Start Date
- End Date
- Total Days
- Reason

4. Leave Type

Supports different leave types such as:

- Casual Leave
- Sick Leave
- Earned Leave
- Other Leave

5. Approval Status

Tracks the status of each leave request:

- Pending
- Approved
- Rejected

---

🔄 Leave Request Workflow

Start
  ↓
Enter Employee Details
  ↓
Verify Employee Details
  ↓
Valid?
 ┌───────────────┐
 │               │
No              Yes
 ↓               ↓
Display Error   Select Department
 ↓               ↓
Return          Enter Leave Details
                 ↓
              Select Leave Type
                 ↓
              Validate Request
                 ↓
              Valid?
             ┌───────┐
             │       │
            No      Yes
             ↓       ↓
        Display Error
                     ↓
              Submit Request
                     ↓
             Status = Pending
                     ↓
             Manager Reviews
                     ↓
                Approval?
              ┌─────┴─────┐
              ↓            ↓
           Approved      Rejected
              ↓            ↓
        Update Record   Update Status
              ↓            ↓
              └──────┬─────┘
                     ↓
             Display Final Status
                     ↓
                    End

---

🗃️ Database Design

The project contains the following entities:

EMPLOYEE

Attribute| Key
Employee_ID| PK
Employee_Name| 
Email| 
Phone| 
Department_ID| FK

DEPARTMENT

Attribute| Key
Department_ID| PK
Department_Name| 
Description| 

LEAVE_REQUEST

Attribute| Key
Request_ID| PK
Employee_ID| FK
Leave_Type_ID| FK
Status_ID| FK
Start_Date| 
End_Date| 
Total_Days| 
Reason| 

LEAVE_TYPE

Attribute| Key
Leave_Type_ID| PK
Leave_Type_Name| 
Description| 

APPROVAL_STATUS

Attribute| Key
Status_ID| PK
Status_Name| 
Approved_Date| 
Remarks| 

---

🔗 Entity Relationships

The database follows these relationships:

DEPARTMENT 1 ───────── M EMPLOYEE

EMPLOYEE 1 ─────────── M LEAVE_REQUEST

LEAVE_TYPE 1 ───────── M LEAVE_REQUEST

APPROVAL_STATUS 1 ──── M LEAVE_REQUEST

Relationship Explanation

- One Department can have many Employees.
- One Employee can submit many Leave Requests.
- One Leave Type can be associated with many Leave Requests.
- One Approval Status can be associated with many Leave Requests.

---

🧩 ERD

The Entity Relationship Diagram contains:

- EMPLOYEE
- DEPARTMENT
- LEAVE_REQUEST
- LEAVE_TYPE
- APPROVAL_STATUS

Primary Keys (PK) and Foreign Keys (FK) are clearly identified to show the database relationships.

---

📋 Algorithm

1. Start.
2. Enter Employee ID, Employee Name, Email, and Contact Number.
3. Verify the employee details.
4. If the details are invalid, display "Invalid Employee Details" and ask the user to enter them again.
5. If valid, identify/select the employee's department.
6. Enter Leave Start Date, Leave End Date, and Reason.
7. Select the required Leave Type.
8. Validate the leave request details.
9. If invalid, display "Invalid Leave Request" and return to leave request entry.
10. Submit the Leave Request.
11. Set Approval Status to "Pending".
12. Send the request to the concerned manager/authority.
13. Review the approval status.
14. If approved, display "Leave Request Approved".
15. If rejected, display "Leave Request Rejected".
16. If pending, display "Leave Request Pending".
17. Display the final Approval Status.
18. End.

---

🛠️ Technologies / Concepts

This project demonstrates fundamental concepts of:

- Database Management Systems (DBMS)
- Entity Relationship Diagrams (ERD)
- Primary Keys
- Foreign Keys
- Database Relationships
- Flowcharts
- Algorithms
- Data Validation
- Leave Management Systems
- CRUD Operations

---

📁 Project Structure

Employee-Leave-Leave-Request/
│
├── README.md
│
├── Algorithm/
│   └── Employee_Leave_Flowchart.png
│
├── ERD/
│   └── Employee_Leave_ERD.png
│
└── Documentation/
    └── Project_Documentation.pdf

«Update the folder and file names according to the actual files uploaded to the repository.»

---

🎓 Academic Information

Project Title: Employee Leave – Leave Request

Feature Set: Feature Set I

Course: Bachelor of Computer Applications (BCA)

Project Type: Database / Software System Design

---

👨‍💻 Project Purpose

This project is developed for academic purposes to demonstrate how a simple employee leave management system can be designed using algorithms, flowcharts, and database concepts.

---

📌 Conclusion

The Employee Leave – Leave Request system provides a structured approach to managing employee leave requests. The database design separates employee, department, leave type, request, and approval information into related entities, making the system organized and easier to manage.

The algorithm and ERD together provide a clear foundation for implementing the complete leave management application.

---

📄 License

This project is created for educational and academic purposes.
