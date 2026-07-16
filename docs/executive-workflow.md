# VendorWise AI Executive Workflow

This workflow presents the end-to-end third-party risk lifecycle, from business need and procurement intake through vendor assessment, approval, monitoring, and reassessment.

## Component types

- **Agent:** Uses AI to perform analysis and recommendations.
- **Engine:** Applies deterministic rules and assessment logic.
- **Human:** Performs accountable review and decision-making.
- **System:** Stores records or manages workflow activities.

```mermaid
flowchart TD

A[Business Need]
    --> B[Procurement Intake]

B --> C[ISO Vendor Engagement Intake]

C --> D{Vendor Already Selected?}

D -- No --> E[AGENT: Vendor Triage and Pre-Screening]

E --> F[Business Selects Preferred Vendor]

D -- Yes --> G[ENGINE: Assessment Scoping Engine]
F --> G

G --> H[Targeted Business Questions<br/>and Vendor Evidence Submission]

H --> I[AI-Powered ISO Vendor Assessment Workflow]

I --> J[ISO Analyst Review]

J --> K{Final Decision}

K -- Approve --> L[Vendor Inventory]

K -- Approve with Conditions --> M[Vendor Inventory]

K -- Reject --> Z[Assessment Closed and Retained]

L --> N[System and Integration Inventory]
M --> N

M --> O[Risk Treatment Register]

N --> P[Assessment Repository]
O --> P

P --> Q[Ongoing Monitoring]

Q --> R{Material Change or Scheduled Review?}

R -- Yes --> G
R -- No --> Q
```

## Decision outcomes

- **Approve:** Add the vendor to the inventory, retain the assessment, and begin monitoring.
- **Approve with Conditions:** Add the vendor to the inventory and track outstanding actions in the Risk Treatment Register.
- **Reject:** Close and retain the assessment without onboarding the vendor.