# Experiment 1: Entity-Relationship (ER) Diagram
## REG NO 212222060173

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Pavithra K

## Scenario Chosen:
University / Hospital (choose one)

## ER Diagram:
![Screenshot (1)](https://github.com/user-attachments/assets/e9316f3a-ecfb-40c1-bc93-5694513f75e8)

## Entities and Attributes:
Student: Reg no, Student name, Department
Faculty: Faculty Id, Faculty name, Dept
Course: Course code, Course name, Department
ERP: Faculty name, Course details, Slots
Login: Login user, User_id, Password

## Relationships and Constraints:
### Enroll (between Student and Course)
Cardinality: Many-to-Many
Participation: Partial
Description: Students can enroll in multiple courses, and each course can have multiple students.

### Teaches (between Faculty and Student)
Cardinality: Many-to-Many
Participation: Partial
Description: A faculty member may teach multiple students; a student may be taught by multiple faculty.

### Assign (between Course and ERP)
Cardinality: One-to-One or One-to-Many
Participation: Total (for Course)
Description: Every course is assigned in ERP with specific faculty and slot info.

### Has (between Login and ERP)
Cardinality: One-to-One
Participation: Total
Description: A login account is required to access the ERP system.

## Extension (Prerequisite / Billing):
This ER model does not explicitly include prerequisite or billing information.
To model prerequisites:
Add a recursive relationship Prerequisite on the Course entity (e.g., Course —has prerequisite→ Course).
To model billing:
Create a new entity Billing with attributes like Amount, PaymentStatus, and link it to Student and Course via a relationship like PaysFor.

## Design Choices:
Separation of concerns: Distinct entities for students, faculty, courses, and logins improve clarity and manageability.
ERP as central node: Reflects real-world university systems that unify multiple academic records.
Security: Login entity ensures authentication for accessing ERP.
Flexibility: Many-to-many relationships enable realistic modeling of enrollments and teaching assignments.

## RESULT
The concepts of Entity-Relationship (ER) modeling were understood and successfully applied by creating an ER diagram for a real-world application. The diagram effectively represents entities such as Student, Faculty, Course, ERP, and Login, along with their attributes and relationships. This ER model demonstrates the structure and interactions within an academic ERP system.


