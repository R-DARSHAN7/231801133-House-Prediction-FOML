```mermaid
graph TB;
    A[Student] -->|Creates profile| B[Admin Panel]
    A -->|View grades| C[Student Portal]
    B -->|Manage profiles| D[Database]
    B -->|Assign Program| E[Degree Program]
    C -->|View Academic Record| D
    D -->|Store Academic Records| F[Database]
    D -->|Store Program Data| E
    G[Evaluation Engine] -->|Evaluate CGPA & Grades| D
    G -->|Trigger Evaluation| H[Outcome Manager]
    H -->|Assign Status| D
    H -->|Trigger Actions| I[Actions (Probation, Dismissal)]
    
    subgraph Database
        D
    end
    
    subgraph System
        G[Evaluation Engine]
        H[Outcome Manager]
    end
