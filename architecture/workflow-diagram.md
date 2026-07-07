# VendorWise AI Workflow

```mermaid
flowchart TD
    A[Start Vendor Adoption Request] --> B{Does business already have a vendor?}

    B -->|No| C[Vendor Selection Guidance]
    B -->|Yes| D[Selected Vendor Assessment]

    C --> E[Compare Vendor Options]
    E --> F[Recommend Preferred Vendor or Safer Option]

    D --> G[Collect Vendor Documents]
    G --> H[Assess Security Controls]
    H --> I[Assess Privacy and Data Risk]
    I --> J[Assess AI Governance Risk]
    J --> K[Assess Integration Security]

    K --> L[Apply Governance Scoring Logic]
    L --> M[Translate Technical Risk to Business Impact]
    M --> N[Recommend Compensating Controls]
    N --> O[Generate Adoption Decision]

    O --> P{Decision}
    P -->|Approve| Q[Proceed with Standard Onboarding]
    P -->|Approve with Conditions| R[Track Required Controls]
    P -->|Pilot Only| S[Limit Scope and Monitor]
    P -->|Reject| T[Document Rationale]