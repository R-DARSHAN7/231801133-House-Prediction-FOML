```mermaid
sequenceDiagram
    participant Admin
    participant System
    participant Student
    participant EvaluationEngine
    participant OutcomeManager

    Admin->>System: Create or Update Student Profile
    System->>Student: Assign Student to Degree Program

    Admin->>System: Input Academic Record (CGPA, Major CGPA, Grades)
    System->>EvaluationEngine: Trigger Evaluation for Student

    EvaluationEngine->>System: Compare Student CGPA and Grades with Criteria
    EvaluationEngine->>OutcomeManager: Assign Status based on Evaluation

    OutcomeManager->>System: Trigger Follow-up Actions (e.g., Probation, Dismissal)
    OutcomeManager->>Student: Notify Student of Status and Actions

    Admin->>System: Review and Modify Evaluation Criteria
