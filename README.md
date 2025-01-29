# Smart-Legal-Solutions-2.0


# Legal Document Analysis Automation

This project automates the analysis of legal documents, focusing on Serbian law. It includes features for document summarization, appeal generation, legal review, lawsuit generation, and contract analysis.

## Flowchart

The following flowchart visualizes the document analysis process from input through various assessment stages to final output:

```mermaid
flowchart TD
    classDef pink fill:#FFB6C1,stroke:#333
    classDef blue fill:#ADD8E6,stroke:#333
    classDef green fill:#90EE90,stroke:#333
    classDef purple fill:#DDA0DD,stroke:#333
    classDef red fill:#FF6B6B,stroke:#333
    classDef yellow fill:#FFD700,stroke:#333

    %% Input Processing
    A[Document Upload]:::pink
    B[PDF Text Extraction]:::pink
    C[Document Chunking]:::pink

    %% Analysis Selection
    D[Document Type Detection]:::blue
    E[Analysis Type Selection]:::blue
    F[Route Determination]:::blue

    %% Legal Agents
    G[Summary Generation]:::green
    H[Appeal Creation]:::green
    I[Legal Review]:::green
    J[Lawsuit Generation]:::green
    K[Defense Response]:::green
    L[Contract Analysis]:::green
    M[Chat Support]:::green

    %% AI Processing
    N[GPT-4 Processing]:::purple
    O[Context Management]:::purple
    P[Legal Compliance Check]:::purple

    %% Output Handling
    Q[PDF Generation]:::red
    R[Web Display]:::red
    S[Chat Interface]:::red

    %% Final Delivery
    T[Document Downloads]:::yellow
    U[Web Interface]:::yellow
    V[Result Storage]:::yellow

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
