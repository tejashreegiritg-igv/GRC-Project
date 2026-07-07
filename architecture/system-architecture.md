# System Architecture

```mermaid
flowchart TD
    A[Business User] --> B[Copilot Studio Intake]
    B --> C[Power Automate Workflow]

    C --> D[Vendor Documents]
    C --> E[Business Context]
    C --> F[Integration Context]

    D --> G[OpenAI / Azure OpenAI Evidence Extraction]
    E --> H[Python Governance Engine]
    F --> H

    G --> H

    H --> I[Risk and Adoption Decision Logic]
    I --> J[Business Impact Translation]
    J --> K[Compensating Controls]
    K --> L[Executive Decision Package]

    L --> M[Human Review and Approval]
    M --> N[SharePoint / Dataverse Risk Register]