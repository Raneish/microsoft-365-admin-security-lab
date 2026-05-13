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

**Evidence**
<img width="1346" height="591" alt="Figure 1-Active users" src="https://github.com/user-attachments/assets/fb264089-4e60-42a1-b511-d22f7fa40e83" />
_Figure 1: Shows active Microsoft 365 users, including the configured break-glass emergency administrator account._

<img width="792" height="383" alt="Figure 2 Shows MFA being enabled for selected users during testing" src="https://github.com/user-attachments/assets/0726c9d1-b30b-4e6e-b118-488db646035f" />
_Figure 2: Shows MFA being enabled for selected users during testing.
_

<img width="1081" height="892" alt="Figure 3 Shows the Conditional Access policy configured to enforce MFA while excluding administrator and break-glass accounts" src="https://github.com/user-attachments/assets/7088cb9a-0a92-479e-9243-fdfc746f0799" />
_Figure 3: Shows the Conditional Access policy configured to enforce MFA while excluding administrator and break-glass accounts._

<img width="1421" height="632" alt="Figure 4 Shows all authentication methods enabled within the tenant" src="https://github.com/user-attachments/assets/69554fab-1c09-41fd-b8ed-d612141f4223" />
_Figure 4: Shows all authentication methods enabled within the tenant._

<img width="627" height="566" alt="Figure 5 Shows the end-user prompt to register Multi-Factor Authentication" src="https://github.com/user-attachments/assets/787ad604-c42a-46cb-9bf2-3f038ec4a00a" />
_Figure 5: Shows the end-user prompt to register Multi-Factor Authentication._

<img width="472" height="496" alt="Figure 6 Shows successful MFA approval using Microsoft Authenticator" src="https://github.com/user-attachments/assets/675dac7a-90b9-4ca7-b0ae-b1f389fa012f" />
_Figure 6: Shows successful MFA approval using Microsoft Authenticator._

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

**Evidence**

<img width="1113" height="895" alt="Figure 7 Shows Windows Autopilot profile properties" src="https://github.com/user-attachments/assets/f6150624-2d10-463d-ab0e-2aae28c28248" />
_Figure 7: Shows Windows Autopilot profile properties._

<img width="1165" height="499" alt="Figure 8 Shows enrolment restriction policies configured for device types" src="https://github.com/user-attachments/assets/c62224e6-74a3-478f-a0f4-5d95e922c7c0" />
_Figure 8: Shows enrolment restriction policies configured for device types._

Outcome
Windows devices can be enrolled through Autopilot and receive organisational settings during initial setup, helping standardise device deployment and reduce manual configuration.
--------------------------------------------------------------------------------------------------------------------

**Compliance Policies**
**What I Did**
- Built Windows compliance policies enforcing:
- Minimum OS version
- BitLocker encryption
- Password requirements
- Assigned compliance policies to user groups
- Reviewed compliance monitoring dashboards

**Evidence**

<img width="928" height="950" alt="Figure 9 Shows Windows 10 and later compliance policies" src="https://github.com/user-attachments/assets/93c7f034-949c-466c-ac5d-5d7a471200e2" />
_Figure 9: Shows Windows 10 and later compliance policies._

<img width="564" height="544" alt="Figure 10 Shows the Windows compliance monitoring dashboard" src="https://github.com/user-attachments/assets/fe41d6bd-742b-4938-8d39-602c7287c11d" />
_Figure 10: Shows the Windows compliance monitoring dashboard._

Outcome
Only Intune-managed devices meeting defined compliance standards are eligible for access to organisational resources.

-----------------------------------------------------------------------------------------------------------------

**Device Configuration Profiles**
**What I Did**
- Created Intune device configuration profiles enforcing:
- Screen timeout policies
- USB storage restrictions
- Password complexity requirements

**Evidence**

<img width="1138" height="581" alt="Figure 11 Shows steps used to create device configuration profiles" src="https://github.com/user-attachments/assets/1004f5a3-9374-4286-895e-9ae424e9acb6" />
_Figure 11: Shows steps used to create device configuration profiles._

<img width="1093" height="589" alt="Figure 12 Shows screen timeout profile settings" src="https://github.com/user-attachments/assets/60af26f3-6e45-4182-8e77-9ebd38084700" />
_Figure 12: Shows screen timeout profile settings._

<img width="1239" height="570" alt="Figure 13 Shows USB storage restrictions being configured" src="https://github.com/user-attachments/assets/2e8ad1bc-8bbd-45a7-bfeb-8a79ec628b5c" />
__Figure 13: Shows USB storage restrictions being configured._

<img width="743" height="833" alt="Figure 14 Shows completed Windows security configuration profile" src="https://github.com/user-attachments/assets/1b4a913c-d400-4697-9ef6-1a738e8ba34c" />
_Figure 14: Shows completed Windows security configuration profile._

Outcome
Security settings are applied consistently across managed devices through Intune configuration profiles.
---------------------------------------------------------------------------------------------------------------------

**TASK 03 — Conditional Access Policies**
Business Context

Conditional Access acts as a policy engine at the identity layer, evaluating access requests based on user, device, location, and session conditions.

**What I Did**
Created policies to block legacy authentication protocols:
- SMTP
- POP
- IMAP
- MAPI
- Enforced MFA for:
- Azure Management access
- Administrator roles
- Restricted access to compliant managed devices only
- Configured sign-in frequency controls

**Evidence**

<img width="979" height="778" alt="Figure 16 Shows configured Conditional Access policies" src="https://github.com/user-attachments/assets/2f58c99a-a35a-4e04-a720-5435ddbaff50" />
_Figure 15: Shows configured Conditional Access policies._

Outcome
Conditional Access policies were implemented to strengthen identity security by blocking legacy authentication, enforcing MFA for privileged access, and restricting access to compliant devices.
-------------------------------------------------------------------------------------------------------------------
**TASK 04 — Exchange Online Mail Flow Management**
Business Context

Mail flow rules support secure communication, regulatory compliance, and email threat reduction.

**What I Did**
- Created a disclaimer rule appending legal text and corporate signatures to outgoing mail
- Configured urgent email forwarding to IT support mailbox
- Blocked oversized external attachments
- Blocked executable attachments (.exe, .bat, .cmd)

**Evidence**

<img width="1196" height="522" alt="Figure 16 Shows configured mail flow rules" src="https://github.com/user-attachments/assets/469c2818-bdff-4cfe-835f-284059df357c" />
_Figure 16: Shows configured mail flow rules._

<img width="1608" height="818" alt="Figure 17 Shows disclaimer rule configuration" src="https://github.com/user-attachments/assets/a4034bd4-436f-4a3f-99c4-95637dd74551" />
_Figure 17: Shows disclaimer rule configuration._

<img width="1535" height="817" alt="Figure 18 Shows urgent email forwarding rule" src="https://github.com/user-attachments/assets/fa08da51-b24e-4265-9465-9688c658f961" />
_Figure 18: Shows urgent email forwarding rule._

<img width="575" height="887" alt="Figure 19 Shows attachment size restriction rule" src="https://github.com/user-attachments/assets/7f0c8364-9450-4dc0-ae3a-3a05cc4c676d" />
_Figure 19: Shows attachment size restriction rule._

<img width="1588" height="811" alt="Figure 20 Shows executable attachment blocking rule" src="https://github.com/user-attachments/assets/1307001f-01d0-435d-a7eb-0889a2cc4759" />
_Figure 20: Shows executable attachment blocking rule._

Outcome
Mail flow rules were configured to improve email governance, route urgent support requests, and reduce exposure to malicious attachments.
-----------------------------------------------------------------------------------------------------------------
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













