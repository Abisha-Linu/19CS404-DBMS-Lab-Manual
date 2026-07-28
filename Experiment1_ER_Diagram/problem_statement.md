
# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:

<img width="1351" height="551" alt="image" src="https://github.com/user-attachments/assets/3cc10edf-18b4-43af-8a2a-b8a8790acfc7" />


### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|---------------------|-------|
| Member | Member_ID (PK), Name, Membership_Type, Start_Date | Stores details of gym members. |
| Program | Program_ID (PK), Program_Name, Category, Duration | Stores information about fitness programs such as Yoga, Zumba, and Weight Training. |
| Trainer | Trainer_ID (PK), Name, Qualification, Phone | Stores trainer information and specialization. |
| Personal_Session | Session_ID (PK), Session_Date, Session_Time, Member_ID (FK), Trainer_ID (FK) | Records personal training sessions booked by members. |
| Attendance | Attendance_ID (PK), Session_ID (FK), Member_ID (FK), Status | Records attendance for each personal training session. |
| Payment | Payment_ID (PK), Payment_Date, Amount, Payment_Method, Member_ID (FK) | Stores membership and personal session payment details. |
### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|-------------|----------------|-------|
| Member JOINS Program | M:N | Total – Partial | A member can join multiple programs, and a program can have many members. |
| Trainer ASSIGNED TO Program | M:N | Total – Total | A trainer can teach multiple programs, and a program can have multiple trainers. |
| Member BOOKS Personal Session | 1:N | Partial – Total | One member can book many personal training sessions; every session belongs to one member. |
| Trainer CONDUCTS Personal Session | 1:N | Partial – Total | One trainer can conduct many sessions; each session is conducted by one trainer. |
| Personal Session HAS Attendance | 1:N | Total – Total | Attendance is recorded for each session. |
| Member MAKES Payment | 1:N | Partial – Total | A member can make multiple payments; every payment belongs to one member. |

### Assumptions
1.	Every Member has a unique Member_ID. 
2.	Every Trainer has a unique Trainer_ID. 
3.	Every Program has a unique Program_ID. 
4.	A member may enroll in multiple programs. 
5.	A trainer may be assigned to multiple programs. 
6.	Each personal training session is conducted by one trainer for one member. 
7.	Attendance is recorded for each personal session. 
8.	Payments may be for either membership fees or personal training sessions.

---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_library.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_restaurant.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
