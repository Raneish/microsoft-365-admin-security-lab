# microsoft-365-admin-security-lab
Microsoft 365 administration lab covering Entra ID, Intune, Exchange Online, SharePoint, and Teams governance.

Microsoft 365 | Entra ID | Intune | Exchange Online | SharePoint | Teams

Date Completed: March 2026

**Project Overview**
This project involved building and administering a Microsoft 365 tenant to simulate a real-world enterprise IT environment.
The lab focused on identity and access management, endpoint security, mail flow governance, collaboration platform administration, and security policy enforcement across the Microsoft 365 ecosystem.
All configurations were documented using structured runbook-style documentation to reflect common helpdesk and IT administration procedures.

**Objectives**
This lab was designed to demonstrate practical administration of Microsoft cloud technologies, including:
Microsoft 365 tenant administration and user lifecycle management
Multi-Factor Authentication (MFA) configuration and enforcement
Conditional Access policy creation and testing
Exchange Online mail flow rule management
Shared mailbox and group administration
Microsoft Intune device enrolment and compliance management
SharePoint permission and site administration
Microsoft Teams governance and meeting policies

**Environment & Tools Used**
| Category          | Technologies                                                       |
| ----------------- | ------------------------------------------------------------------ |
| Administration    | Microsoft 365 Admin Centre, User Lifecycle Management              |
| Identity & Access | Microsoft Entra ID, Azure AD, MFA, Conditional Access              |
| Device Management | Microsoft Intune, Windows Autopilot, Compliance Policies           |
| Communication     | Exchange Online, Shared Mailboxes, Mail Flow Rules                 |
| Collaboration     | SharePoint Online, Microsoft Teams Admin Centre                    |
| Security          | Legacy Authentication Blocking, Geo-restriction, Security Policies |

**Environment Specifications**
Microsoft 365 Business Standard
Microsoft Entra ID P1 Trial
Microsoft Intune
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**TASK 01 — User Account Management**
Business Context

In a production environment, helpdesk teams manage the full user lifecycle from onboarding through offboarding. Secure identity management ensures appropriate access control, licensing allocation, and account protection.

MFA is a core security control used to reduce the risk of credential compromise.
**What I Did**
Provisioned user accounts with role-appropriate Microsoft 365 licence assignments
Created a secondary Global Administrator account to prevent a single point of failure
Configured a break-glass emergency administrator account excluded from Conditional Access MFA policies

Evidence**
**
Figure 1: Shows active Microsoft 365 users, including the configured break-glass emergency administrator account.

Figure 2: Shows MFA being enabled for selected users during testing.

Figure 3: Shows the Conditional Access policy configured to enforce MFA while excluding administrator and break-glass accounts.

Figure 4: Shows all authentication methods enabled within the tenant.

Figure 5: Shows the end-user prompt to register Multi-Factor Authentication.

Figure 6: Shows successful MFA approval using Microsoft Authenticator.

Outcome

User accounts were provisioned with appropriate licensing and access controls to reflect standard onboarding and access management practices. MFA was enforced for standard users through Conditional Access, while emergency tenant recovery access was maintained through a documented break-glass account.



**TASK 02 — Device Management & Endpoint Security (Microsoft Intune)**
Business Context

Centralised device management enables organisations to enforce security baselines, manage endpoint compliance, and control access to organisational resources.

**What I Did**
Configured Microsoft Intune for endpoint management
Established device enrolment settings
Created a Windows Autopilot enrolment profile
Configured enrolment restrictions to block personally owned devices
Evidence

Figure 7: Shows Windows Autopilot profile properties.

Figure 8: Shows enrolment restriction policies configured for device types.

Outcome

Windows devices can be enrolled through Autopilot and receive organisational settings during initial setup, helping standardise device deployment and reduce manual configuration.

**Compliance Policies**
**What I Did**
Built Windows compliance policies enforcing:
Minimum OS version
BitLocker encryption
Password requirements
Assigned compliance policies to user groups
Reviewed compliance monitoring dashboards
Evidence

Figure 9: Shows Windows 10 and later compliance policies.

Figure 10: Shows the Windows compliance monitoring dashboard.

Outcome

Only Intune-managed devices meeting defined compliance standards are eligible for access to organisational resources.


**Device Configuration Profiles**
**What I Did**
Created Intune device configuration profiles enforcing:
Screen timeout policies
USB storage restrictions
Password complexity requirements
Evidence

Figure 11: Shows steps used to create device configuration profiles.

Figure 12: Shows screen timeout profile settings.

Figure 13: Shows USB storage restrictions being configured.

Figure 14: Shows completed Windows security configuration profile.















