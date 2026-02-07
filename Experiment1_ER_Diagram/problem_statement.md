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

<img width="1446" height="850" alt="image" src="https://github.com/user-attachments/assets/ebc1b52e-2f23-4000-93de-4d031fa9e9c6" />


### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|  Member      |           MemberID (PK), Name,MembershipType, StartDate         |   Stores gym members’ details    |
|    Program    |             ProgramID (PK), ProgramName, Type       |  Yoga, Zumba, Weight Training, etc.     |
|   Trainer     |          TrainerID (PK), Name, Specialization          |    Each trainer may handle multiple programs   |
|      Session	  |       SessionID (PK), Date, Time, TrainerID (FK), ProgramID (FK)             |  Personal training or group sessions     |
|  Payment      |            PaymentID (PK), MemberID (FK), Amount, PaymentDate, Type        |   Tracks membership & session payments    |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|   Registers (Member–Program)           |     M:N       |     Partial (not all members join all programs)          |   A member may join many programs    |
|          AssignedTo (Trainer–Program)    |     M:N       |    Total for Program           |  Programs must have at least one trainer     |
|   Attends (Member–Session)           |      M:N      |   Partial            |  Records attendance     |
|    PaysFor (Member–Payment)          |   1:M         |  Total for Payment             |  Each payment belongs to one member     |
|Covers (Payment–Session/Membership)        | 1:M      |  Optional     |  A payment can cover membership fee or personal session     |
### Assumptions

Each member must have at least one active membership.

A program may have multiple trainers, but at least one is mandatory.

Members can attend multiple sessions; attendance is recorded separately.

Personal training sessions are modeled as “Session” with specific trainer and member.

Payments can be for either membership fees or personal sessions.

### RESULT
Thus the ER Diagram for scenario A has been drawn and explained successfully.
