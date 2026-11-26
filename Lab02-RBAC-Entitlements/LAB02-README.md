# Lab02 — RBAC + Entitlements

## What I Did
Built 2 Roles from 6 Entitlements and assigned them by Department.
One Role = one lunch box. The Entitlements are the food inside.

## Roles Built
**Role-Finance-Base** — Base access for all Finance department
- Finance App Access
- Finance Group
- Finance Shared Drive

**Role-IT-Base** — Base access for all IT department
- IT App Access
- IT Group
- IT Admin Tools (Read-Only)

## Assignment Rule
- Dept = Finance → Role-Finance-Base
- Dept = IT → Role-IT-Base

## Verified
- Asha Joiner (E101, Finance) → Role-Finance-Base only
- Maya Leaver (E103, IT) → Role-IT-Base only
- Ravi Mover (E102, moved Finance → IT) → Role-IT-Base only, no Finance-Base
- Temp Contractor (E104, IT) → Role-IT-Base only, never Finance-Base

## Screenshots
- Architecture_Diagram.png
- Finance-Role.png
- IT-Role.png
- Asha-Roles.png
- Ravi-Roles.png
- Maya-Roles.png
- Temp-Roles.png

## Top 3 Key Learnings
1. Role = a bundle. Entitlement = one single access inside the bundle.
2. Assign by Department, not person-by-person. That is how real companies scale.
3. A Mover must LOSE the old Role. Ravi kept IT-Base only — that is what proves the move worked.

## Environment
Local SailPoint IIQ 2021 lab, part of TechFios IAM training.
HR-Source = HR_Feed.csv, 4 test identities. No real users.