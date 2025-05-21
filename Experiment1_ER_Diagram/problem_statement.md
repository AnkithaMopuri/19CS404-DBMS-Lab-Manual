# Experiment 1: Entity-Relationship (ER) Diagram

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

# ER Diagram Submission - MOPURI ANKITHA
# Register Number: 212223040117

## Scenario Chosen:
University

## ER Diagram:
![ER UNIVERSITY](https://github.com/user-attachments/assets/f0200a0b-e6d6-496c-803a-058c873ea6e2)

## Entities and Attributes:
student: Name,Register Number,Year,Department

Enrollment: Timing,Course Name,Faculty,Day

Courses: Course Name,Course Type,Course Code,Credits

Faculty Details:Faculty id, Faculty Name,Faculty Department


## Relationships and Constraints:
•1.Enrollment (between Student and Enroll)
Relationship: Enrollment
Entities: Student — Enroll
Cardinality:
One student can enroll in many enrollments
One enroll entry is linked to one student
(1:N) from Student to Enroll

•2. Courses (between Enroll and Courses Offered)
Relationship: Courses
Entities: Enroll — Courses Offered
Cardinality:
One enroll instance relates to one course offered
One course offered can be part of many enrollments
(N:1) from Enroll to Courses Offered

•3.Relationship: Faculty
Entities: Enroll — Faculty Details
Cardinality:
One faculty member can appear in many enrollments
One enroll entry is managed by one faculty
(N:1) from Enroll to Faculty Details

## Extension (Prerequisite / Billing):
I modelled prerequisites using a recursive many-to-many relationship on the Courses Offered entity.
This means each course can have multiple prerequisite courses, and a course can be a prerequisite for multiple others.
The relationship is named "Prerequisite" and connects the CourseCode of one course to the CourseCode of another course within the same entity.

## Design Choices:
Student: To store personal details like registration number, name, and contact.

Courses Offered: To manage course information like code, title, credits, etc.

Faculty Details: To keep track of instructors linked to course delivery.

Enroll: Used as a bridge entity to represent student registration for courses.

Billing / Prerequisite: To track payments or course dependencies.

## RESULT
The database was designed to manage information about students, courses, faculty, and enrollments in a university.This design helps organize all the important data clearly. It shows how students are linked to courses, which faculty teaches each course, and how course schedules are managed

