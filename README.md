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


---

## Step 5 – Lab Topology

**Description:**

Built a domain-based lab environment to simulate how Cisco Duo MFA can be used to protect Windows logon authentication in an enterprise setting.

The environment includes a Windows Server Active Directory Domain Controller, an Employees OU, and a domain-joined Windows 10 Pro client workstation. The topology also demonstrates how organizations may use centralized deployment methods such as Group Policy, Microsoft Intune, Jamf, or SCCM/MECM to deploy Duo Authentication for Windows Logon to managed endpoints.

This step provides the foundation for enforcing MFA during Windows logon and validating authentication activity through Duo reporting.

<p align="center">
Active Directory + Duo MFA Deployment Topology<br/>
<img src="https://i.imgur.com/bCXFqKq.png" width="800" style="height:auto;" alt="Active Directory and Cisco Duo MFA topology for Windows Logon"/>
<br /><br />
</p>

---

# 📅 Day 2 Progress Update

Today's work focused on transitioning from basic Duo administration into a more realistic enterprise deployment scenario. Rather than only enrolling users and devices, I expanded the lab by introducing Active Directory and a domain-joined Windows endpoint to simulate how organizations deploy and manage Duo MFA for Windows logon authentication.

### Key Accomplishments

- Built an Active Directory lab environment.
- Created an Employees OU and domain-joined workstation.
- Designed a deployment topology representing enterprise deployment methods.
- Installed and configured Duo Authentication for Windows Logon.
- Integrated the Windows endpoint with the Duo Admin Portal.
- Successfully validated Duo Push authentication during Windows sign-in.

This phase moves the project beyond simple user enrollment and closer to a real-world implementation that IT and security teams may deploy to protect endpoint access.

---


# 📅 Day 3 Progress Update

Today's work focused on implementing and validating Multi-Factor Authentication (MFA) for Windows logon authentication using Cisco Duo.

After building the Active Directory environment and enrolling users and devices in previous phases, I integrated Duo Authentication for Windows Logon with a domain-joined Windows workstation. This allowed me to simulate how organizations enforce MFA at the endpoint level to strengthen identity and access security.

### Key Accomplishments

- Configured the Microsoft RDP application within the Duo Admin Portal.
- Installed and configured Duo Authentication for Windows Logon.
- Connected the workstation to Duo using the Integration Key, Secret Key, and API Hostname.
- Successfully enforced Duo Push authentication during Windows sign-in.
- Validated successful and denied authentication attempts.
- Reviewed authentication activity through Duo reporting and monitoring tools.
- Documented how authentication logs can be used for auditing, troubleshooting, and security investigations.

This phase completed the technical implementation of the project and demonstrated how organizations can use Cisco Duo to protect Windows endpoints while providing administrators with visibility into authentication activity across their environment.


---


## Step 6 – Windows Logon MFA Enforcement

**Description:**

Configured the Microsoft RDP application within Duo and installed Duo Authentication for Windows Logon on a domain-joined Windows 10 workstation.

The workstation was integrated with the Duo Admin Portal using the application's Integration Key, Secret Key, and API Hostname. Once configured, Windows logon authentication required a second factor before access was granted.

This simulates how organizations protect endpoint access by requiring Multi-Factor Authentication (MFA) before users can successfully sign into corporate devices.

<p align="center">
Duo Push Authentication During Windows Logon<br/>
<img src="https://i.imgur.com/PBwJIPm.png" width="800" style="height:auto;" alt="Duo Push authentication during Windows logon"/>
<br /><br />
</p>

---

## Step 7 – Authentication Monitoring

**Description:**

After successfully authenticating through Duo Push, authentication activity was reviewed through the Duo Administration Portal.

Authentication logs provide administrators with visibility into successful logins, denied authentication attempts, authentication methods used, timestamps, and protected applications. These logs can be used for troubleshooting, auditing, compliance reporting, and security investigations.

During testing, both successful and denied authentication attempts were generated to demonstrate how security teams can monitor and investigate authentication activity.

<p align="center">
Duo Authentication Log Monitoring<br/>
<img src="https://i.imgur.com/VEk2D36.png" width="800" style="height:auto;" alt="Duo authentication logs showing successful and denied authentication attempts"/>
<br /><br />
</p>

---

# ✅ Summary

This lab demonstrates the deployment and management of Cisco Duo Multi-Factor Authentication (MFA) for Windows Logon within an Active Directory environment.

Key concepts demonstrated:

- User onboarding and enrollment
- Device registration using Duo Mobile
- Active Directory integration concepts
- Domain-joined Windows endpoint protection
- Multi-Factor Authentication (MFA)
- Windows Logon protection
- Duo Push authentication
- Authentication monitoring and reporting
- Enterprise deployment architecture

The completed environment simulates how organizations protect Windows endpoints using Cisco Duo while maintaining centralized user and endpoint management through Active Directory and enterprise deployment platforms. ( I will make additions to this project).

---

# 🎯 Skills Demonstrated

- Identity & Access Management (IAM)
- Multi-Factor Authentication (MFA)
- Active Directory
- Endpoint Security
- Authentication Monitoring
- Security Administration
- Access Control
- Windows Security
- Security Operations
- Enterprise Authentication Workflows
