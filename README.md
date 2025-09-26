# Ivanti Secure Access Client

* [Installation](#installation)
* [User Roles and Access Control](#user-roles-and-access-control)
* [Authentication and Security Policies](#authentication-and-security-policies)
* [Single Sign-On (SSO) and Adaptive Authentication](#single-sign-on-sso-and-adaptive-authentication)

## Installation

After downloading the installation package, follow these steps to complete the setup:

* Launch the installer and proceed through the guided prompts to finalize the installation.
* Sign in with the credentials issued by your enterprise.
* Configure the VPN in accordance with your organization’s internal security policies.
* Establish a secure connection to access corporate infrastructure and resources.

For further guidance, consult your IT department or refer to the official Ivanti support documentation.

## User Roles and Access Control

### Understanding User Roles

Within ICS, user roles define permissions and access levels for various groups. Administrators have the ability to create custom roles that manage session behavior, user interface elements, and access rights.

### Role-Based Access Management

ICS differentiates between two primary categories of roles:

* **Administrator Roles:** Provide full access to all administrative functions on the ICS platform.
* **User Roles:** Specify the features and permissions available to end-users.

#### Creating a New User Role

```plaintext
1. Navigate to Users > User Roles on the admin dashboard.  
2. Click "New Role" and assign a descriptive name.  
3. Configure the relevant access controls and session policies.  
4. Save the role and link it to the appropriate authentication realms.  
```

## Authentication and Security Policies

### Authentication Methods

ICS integrates with multiple authentication systems to verify user credentials, including:

* **Local Authentication Server**
* **Active Directory (AD)**
* **LDAP**
* **RADIUS**
* **SAML-based solutions**

### Setting Up Authentication Realms

Authentication realms define how users are verified and which roles are assigned to them.

#### Configuration Steps

1. Navigate to **Users > Authentication > User Realms**.
2. Click **New Realm** and provide a unique name.
3. Select the authentication server to be used.
4. Configure user validation rules and role mapping options.
5. Save the settings and attach the realm to the intended sign-in policy.

> **[!info]**
> Enable multi-factor authentication (MFA) where possible to enhance security.

## Single Sign-On (SSO) and Adaptive Authentication

### Configuring SSO

Single Sign-On (SSO) allows users to authenticate once and access multiple services without repeated logins.

ICS supports:

* **SAML 2.0 for web-based SSO**
* **NTLM authentication**
* **Kerberos integration**

#### Enabling SSO

```plaintext
1. Navigate to Authentication > Single Sign-On.  
2. Select the desired protocol (SAML, NTLM, or Kerberos).  
3. Enter the identity provider configuration settings.  
4. Associate the SSO profile with the relevant authentication realms.  
5. Save the configuration and test to confirm proper functionality.  
```

### Adaptive Authentication

Adaptive authentication evaluates factors such as user activity, device attributes, and geographic location before granting access.

#### Implementation Steps

* Define risk parameters based on usage trends, IP addresses, and compliance requirements.
* Create rules that dynamically adjust authentication procedures according to detected risk levels.

## Host Checker and Endpoint Security

The **Host Checker** utility verifies that client devices comply with required security standards before granting access.

### Configuring Host Checker Policies

1. Navigate to **Authentication > Host Checker**.
2. Create a policy specifying compliance criteria (e.g., antivirus status, OS patch level, firewall configuration).
3. Link the policy to the applicable authentication realms.
4. Define actions for devices that fail to meet compliance requirements.

> **[!note]**
> Regularly review Host Checker policies to maintain security posture and respond to emerging threats.

## VPN Tunneling and Secure Application Manager

### VPN Tunneling

ICS utilizes **SSL-based VPN tunnels** to provide full Layer 3 access to enterprise networks.

#### Configuration Steps

* Go to **Users > User Roles** and enable **VPN Tunneling**.
* Configure routing rules and enable split tunneling if needed.
* Apply policies regarding session duration and bandwidth limits.

### Secure Application Manager (SAM)

The Secure Application Manager enables secure access to specific applications by managing traffic at the application layer.

#### Enabling SAM

* Navigate to **Users > User Roles > Secure Application Manager**.
* Specify allowed applications and define target hosts.
* Apply access rules according to user role definitions.

## Resource Policies and Access Control

Resource policies regulate user access to **internal services such as web apps, file shares, and terminal servers**.

### Creating Resource Policies

1. Navigate to **Users > Resource Policies**.
2. Select the resource type (Web, File, Terminal Services, etc.).
3. Define permitted and restricted endpoints according to access requirements.
4. Link the policy to the relevant user roles.

> **[!important]**
> Keep resource policies current to comply with security best practices.

## Logging, Monitoring, and Troubleshooting

### Logging and Event Monitoring

ICS includes **comprehensive logging and real-time event monitoring tools**.

* Enable logging under **System > Logging**.
* Integrate with external log management systems via **Syslog**.
* Use the **Admin Console diagnostic tools** to investigate active issues.

### Troubleshooting Common Issues

* **Login failures:** Verify authentication settings and network connectivity.
* **VPN connectivity problems:** Check firewall rules and VPN tunnel configurations.
* **System performance delays:** Monitor resource usage and consider load balancing solutions.

## Clustering and High Availability

### Configuring Clustering

ICS supports **clustering for high availability**, ensuring fault tolerance and balanced load distribution.

#### Setup Steps

1. Navigate to **System > Clustering**.
2. Add cluster nodes and configure synchronization parameters.
3. Select either **active/passive** or **active/active** operation modes.

## System Maintenance and Configuration Backup

### Performing System Updates

Maintaining ICS updates is critical to ensure **system stability, security, and optimal performance**.

#### Updating ICS

1. Navigate to **Maintenance > System Update**.
2. Upload the latest firmware package.
3. Reboot the device to complete the update.

### Backing Up Configuration Files

Backing up ICS configuration prevents data loss and preserves system settings.

#### Backup Process

* Go to **Maintenance > Configuration Backup**.
* Click **Export Configuration**.
* Store the backup securely in an accessible location.

> **[!note]**
> Schedule regular automated backups to ensure continuous protection.
