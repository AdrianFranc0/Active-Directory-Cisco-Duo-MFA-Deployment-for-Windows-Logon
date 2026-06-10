# Duo Authentication for Windows Logon Lab

This lab simulates an enterprise deployment of Cisco Duo Multi-Factor Authentication (MFA) for Windows Logon using a domain-joined workstation.

The environment consists of an Active Directory Domain Controller (Windows Server 2016), a Windows 10 Pro client workstation, and Cisco Duo Authentication for Windows Logon. The project demonstrates user enrollment, device registration, MFA enforcement, push-based authentication, and authentication monitoring.

In addition to validating Duo functionality, the lab was designed to mirror how organizations centrally manage users and endpoints through Active Directory while leveraging solutions such as Group Policy, Microsoft Intune, Jamf, or endpoint management platforms to deploy and manage authentication software.

---

## Technologies Used

- Active Directory Domain Services (AD DS)
- Windows Server 2016
- Windows 10 Pro
- Cisco Duo
- Duo Mobile
- Multi-Factor Authentication (MFA)
- Microsoft RDP Application
- Active Directory Organizational Units (OU)
- VirtualBox

---

## Step 1 – Duo Administration Portal

**Description:**

Created a Cisco Duo tenant and gained access to the Duo Administration Portal. This portal serves as the centralized location for managing users, enrolled devices, authentication methods, policies, protected applications, and authentication logs.

<p align="center">
<br/>
<img src=https://i.imgur.com/YyYJjnY.png width="800" style="height:auto;" alt="Cisco Duo Admin Portal dashboard"/>
<br /><br />
</p>

---

## Step 2 – User Creation

**Description:**

Created a test user within Duo to simulate onboarding a new employee. User accounts within Duo represent the identities that will later be protected by multi-factor authentication.

The account was configured with an active status and prepared for device enrollment.

<p align="center">
Duo Test User Created<br/>
<img src="https://i.imgur.com/VumKBMZ.png" width="800" style="height:auto;" alt="Test user created in Cisco Duo"/>
<br /><br />
</p>

---

## Step 3 – User Enrollment

**Description:**

Initiated the enrollment process by sending an enrollment invitation to the user. This process mirrors how employees are onboarded and register their authentication devices in production environments.

The enrollment email allows the user to securely associate a device with their Duo account.

<p align="center">
Duo Enrollment Invitation Sent<br/>
<img src="https://i.imgur.com/U42y022.png" width="800" style="height:auto;" alt="Enrollment invitation sent to Duo user"/>
<br /><br />
</p>

---

## Step 4 – Device Registration

**Description:**

Completed user enrollment through Duo Mobile and registered an iPhone as the user's authentication device.

Once enrollment was completed, the device became available for push notifications and additional authentication methods such as passcodes and phone verification.

<p align="center">
Duo Mobile Device Registered<br/>
<img src=https://i.imgur.com/WgLBEqm.png width="800" style="height:auto;" alt="User enrolled with iPhone registered in Duo"/>
<br /><br />
</p>


# Progress Update

Completed:

- Duo Administration Portal Setup
- User Creation
- Enrollment Invitation
- Device Registration

Upcoming:

- Enterprise Lab Topology
- Windows Logon MFA Enforcement
- Authentication Monitoring & Reporting
