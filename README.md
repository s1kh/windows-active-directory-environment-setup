# windows-active-directory-environment-setup

# Windows Active Directory Environment Setup

## Overview
Deployment of a secure, enterprise-style Windows Active Directory environment,
including a domain controller, departmental organizational units, and Group
Policy-based access control enforced and validated through live testing.

## My Contribution
Individual project. I built the full environment and designed, implemented, and
tested all access control policies.

## Objectives
- Simulate a small organizational network with role-based access control
- Deploy core Windows Server infrastructure roles
- Enforce access restrictions aligned with departmental security requirements

## Environment
| Component | Details |
|---|---|
| Domain Controller | Windows Server 2022 |
| Client | Windows 10 Pro |
| Domain | khateeb.com |
| Roles installed | AD DS, DNS, DHCP, IIS |

## Work Performed
- Installed and configured AD DS, DNS, DHCP, and IIS roles; promoted the server to a
  Domain Controller and created the domain
- Joined a Windows 10 client to the domain
- Created Organizational Units (HR, Technical) and assigned users to each
- Hosted a sample website via IIS
- Configured Group Policy Objects:
  - HR-specific GPO disabling CMD/PowerShell and blocking website access
  - Domain-wide GPO disabling Control Panel and USB/removable storage access
  - Logon-hour restrictions (8 AM–5 PM) on a user account
- Validated every policy through live testing (e.g., confirming CMD was blocked for
  HR, the website was reachable only for Technical, and logon outside permitted
  hours was denied)

## Results
- All configured policies were verified working as intended through direct testing
- Demonstrated a structured, least-privilege access model suitable for an
  enterprise network

## Documentation
See [`docs/`](./docs) for the full written report and supporting screenshots of each
configuration and validation step.

## Disclaimer
Built entirely in an isolated lab (VirtualBox) for educational purposes. No real
organizational data or infrastructure was used.
