# Smart-Legal-Solutions-2.0


# Legal Document Analysis Automation

This project automates the analysis of legal documents, focusing on Serbian law. It includes features for document summarization, appeal generation, legal review, lawsuit generation, and contract analysis.

## Flowchart

The following flowchart visualizes the document analysis process from input through various assessment stages to final output:

```mermaid
flowchart TD
    %% Style definitions
    classDef primary fill:#4A90E2,stroke:#2171C7,color:#fff,font-size:14px
    classDef secondary fill:#34495E,stroke:#2C3E50,color:#fff,font-size:14px
    classDef success fill:#2ECC71,stroke:#27AE60,color:#fff,font-size:14px
    classDef info fill:#3498DB,stroke:#2980B9,color:#fff,font-size:14px
    classDef warning fill:#F1C40F,stroke:#F39C12,color:#fff,font-size:14px
    classDef danger fill:#E74C3C,stroke:#C0392B,color:#fff,font-size:14px

    %% Input Processing
    A[Document Upload]:::primary
    B[PDF Text Extraction]:::primary
    C[Document Chunking]:::primary

    %% Analysis Selection
    D[Document Type Detection]:::secondary
    E[Analysis Type Selection]:::secondary
    F[Route Determination]:::secondary

    %% Legal Agents
    G[Summary Generation]:::success
    H[Appeal Creation]:::success
    I[Legal Review]:::success
    J[Lawsuit Generation]:::success
    K[Defense Response]:::success
    L[Contract Analysis]:::success
    M[Chat Support]:::success

    %% AI Processing
    N[GPT-4 Processing]:::info
    O[Context Management]:::info
    P[Legal Compliance Check]:::info

    %% Output Handling
    Q[PDF Generation]:::danger
    R[Web Display]:::danger
    S[Chat Interface]:::danger

    %% Final Delivery
    T[Document Downloads]:::warning
    U[Web Interface]:::warning
    V[Result Storage]:::warning

    %% Flow connections
    A --> B --> C
    C --> D --> E --> F
    F --> |Summary|G
    F --> |Appeal|H
    F --> |Review|I
    F --> |Lawsuit|J
    F --> |Defense|K
    F --> |Contract|L
    F --> |Chat|M
    
    G & H & I & J & K & L & M --> N
    N --> O --> P
    
    P --> Q
    P --> R
    P --> S
    
    Q --> T
    R --> U
    S --> U
    Q & R & S --> V
