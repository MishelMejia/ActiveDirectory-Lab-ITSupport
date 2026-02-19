# Lab 03 — Active Directory User Administration

This lab documents a complete IT Support workflow performed in a Windows Server 2022 Active Directory environment.  
The objective was to simulate real-world helpdesk tasks including user creation, password policy handling, domain joining, troubleshooting, and final login validation.

Environment:

- Windows Server 2022 — Domain Controller
- Windows 11 Client VM
- VMware Workstation
- Domain: mishel.local

---

## 1️⃣ Active Directory Setup & User Creation

Active Directory Users and Computers (ADUC) was used to create organizational units and manage user accounts.

Organizational Units created:

- HR Department
- Sales Department

![ADUC Open](images/aduc-open.png)

User accounts were created following basic organizational structure.

![Users HR](images/users-list-hr.png)

![Users Sales](images/users-list-sales.png)

Example of HR user creation:

![User Created](images/user-created-hr-mlopez.png)

---

## 2️⃣ Password Policy — User Creation Scenario

While creating a new user account, a password complexity error occurred because the password did not meet the domain password policy requirements.

This represents a common IT Support scenario where administrators must comply with security standards during account provisioning.

![Password Error](images/error1.png)

Resolution:

- Reviewed password complexity rules
- Updated password using uppercase, lowercase, numbers, and symbols
- Successfully completed user creation

After provisioning, password management tasks such as resets were performed through Active Directory Users and Computers.

![Reset Password](images/reset-password-mlopez.png)

---

## 3️⃣ Windows 11 Client Configuration

The Windows 11 client virtual machine was prepared to connect to the domain.

Work or school account setup during configuration:

![Work School Setup](images/client_setup_work_school.png)

DNS settings were configured to point to the Domain Controller to allow domain discovery.

![DNS Config](images/client_dns_config.png)

---

## 4️⃣ Domain Join Process

The client machine was joined to the Active Directory domain.

System before domain join:

![Before Domain Join](images/client01_before_domain_join.png)

Domain join configuration window:

![Join Domain Window](images/client01_join_domain_window.png)

Successful domain join confirmation:

![Domain Success](images/client01_domain_success.png)

---

## 5️⃣ Troubleshooting — Connectivity Issue

A ping test initially failed, demonstrating a typical troubleshooting scenario handled by IT Support teams.
Root cause identified:

- DNS configuration mismatch between client and Domain Controller

Resolution steps:

- Verified DNS server IP address
- Confirmed VM network adapter settings
- Validated connectivity after correction

![Ping Correct](images/IMG_03_ping_domain.png)

---

## ⭐ 6️⃣ Final Validation — Domain User Login

After completing setup and troubleshooting, domain login was validated successfully.

Login using domain user:

![Session Log](images/session _log_ccalderon.png)

User session confirmation:


![Domain Login](images/client01_login_domain_user.png)

---

## 💡 Skills Demonstrated

- Active Directory user provisioning
- Organizational unit management
- Password policy handling
- Domain join configuration
- DNS troubleshooting
- Authentication validation
- Helpdesk-style issue resolution

---

## 📌 Notes

This lab reflects a realistic IT Support workflow from account creation to successful domain login validation, including password policy enforcement and troubleshooting scenarios.

