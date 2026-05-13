# Microsoft 365 Administration & Security Lab
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
- Microsoft 365 Business Standard
- Microsoft Entra ID P1 Trial
- Microsoft Intune
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


-----------------------------------------------------------------------------------------
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

Outcome
Security settings are applied consistently across managed devices through Intune configuration profiles.

**TASK 03 — Conditional Access Policies**
Business Context

Conditional Access acts as a policy engine at the identity layer, evaluating access requests based on user, device, location, and session conditions.

**What I Did**
Created policies to block legacy authentication protocols:
SMTP
POP
IMAP
MAPI
Enforced MFA for:
Azure Management access
Administrator roles
Restricted access to compliant managed devices only
Configured sign-in frequency controls
Evidence

Figure 16: Shows configured Conditional Access policies.

Outcome

Conditional Access policies were implemented to strengthen identity security by blocking legacy authentication, enforcing MFA for privileged access, and restricting access to compliant devices.

**TASK 04 — Exchange Online Mail Flow Management**
Business Context

Mail flow rules support secure communication, regulatory compliance, and email threat reduction.

**What I Did**
Created a disclaimer rule appending legal text and corporate signatures to outgoing mail
Configured urgent email forwarding to IT support mailbox
Blocked oversized external attachments
Blocked executable attachments (.exe, .bat, .cmd)
Evidence

Figure 15: Shows configured mail flow rules.

Figure 16: Shows disclaimer rule configuration.

Figure 17: Shows urgent email forwarding rule.

Figure 18: Shows attachment size restriction rule.

Figure 19: Shows executable attachment blocking rule.

Outcome
Mail flow rules were configured to improve email governance, route urgent support requests, and reduce exposure to malicious attachments.

**TASK 05 — Microsoft Teams Governance
Business Context**

Teams governance supports controlled communication standards and meeting security.

**What I Did**
Created messaging policies restricting:
GIFs
Memes
Message deletion permissions
Configured meeting policies restricting:
Lobby bypass
Recording permissions
Evidence

Figure 20: Shows Teams messaging policy settings.

Figure 21: Shows Teams meeting policy settings.

Outcome
Teams policies were configured to support controlled communication standards and meeting governance.

**Direct Routing Exploration**
**What I Did**
Explored Teams Direct Routing configuration for PSTN telephony integration
Evidence

Figure 22: Shows Direct Routing configuration area.

Outcome
Direct Routing functionality was explored to understand Teams telephony integration and unified communications capabilities.

**TASK 06 — Shared Mailboxes, Groups & Access Management
Business Context**

Shared mailboxes and groups improve communication efficiency and simplify access management.

What I Did
Created a shared mailbox for IT support
Created a Sales distribution list
Configured security groups for IT users and devices
Evidence

Figure 23: Shows IT support shared mailbox.

Figure 24: Shows group configuration.

Outcome
Shared mailboxes and groups were configured to support team communication and centralised access management.

**TASK 07 — SharePoint Administration**
Business Context

SharePoint enables structured collaboration, document management, and internal communication.

**What I Did**
Created:
IT Team Site
Communication Site
Configured:
Owner permissions
Member permissions
Visitor permissions
Built document libraries for IT documentation storage
Evidence

Figure 25: Shows SharePoint Team Site.

Figure 26: Shows SharePoint permissions configuration.

Outcome
SharePoint sites and permissions were configured to support collaboration, communication, and access control.

**TASK 08 — Message Trace & Email Investigation**
Business Context

Message trace supports troubleshooting, audit readiness, and email investigation.

**What I Did**
Reviewed message trace functionality to analyse:
Delivery status
Mail flow rule actions
Filtering decisions
Timestamps
Evidence

Figure 27: Shows message trace reporting.

Outcome
Message trace functionality was reviewed to understand email troubleshooting, delivery analysis, and audit support capabilities.

**Skills Demonstrated**
- Microsoft 365 Administration
- Microsoft Entra ID
- Azure AD
- Identity & Access Management
- Conditional Access
- Multi-Factor Authentication
- Exchange Online
- Mail Flow Rules
- Shared Mailboxes
- Microsoft Intune
- Windows Autopilot
- Endpoint Compliance
- SharePoint Administration
- Microsoft Teams Governance
- Security Policy Enforcement
- IT Documentation

**Key Learning Outcomes**
Through this project, I strengthened practical understanding of:
Identity and access management in Microsoft 365
Endpoint security and compliance management
Cloud administration workflows
Security policy enforcement
IT operational documentation













