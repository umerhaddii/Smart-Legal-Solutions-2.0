# Smart-Legal-Solutions-2.0


# Legal Document Analysis Automation

This project automates the analysis of legal documents, focusing on Serbian law. It includes features for document summarization, appeal generation, legal review, lawsuit generation, and contract analysis.

## Flowchart

graph TD
    A[Input Document] --> B[Document Chunking]
    B --> C{Agent Selection}
    
    C -->|Legal Review Path| D[Legal Review Agent]
    D --> E[Create Messages with Serbian Legal Prompt]
    E --> F[Model Invocation]
    F --> G[Compile Review Parts]
    
    C -->|Appeal Path| H[Appeal Agent]
    H --> I[Create Messages]
    I --> J[Model Invocation]
    J --> K[Compile Appeal Parts]
    
    G --> L[Final Legal Review Output]
    K --> M[Final Appeal Output]
    
    subgraph Error Handling
    N[Error Logging]
    O[Error Response Generation]
    end
    
    F -.->|On Error| N
    J -.->|On Error| N
    N --> O
