# Explain the difference between authentication and authorization

- Authentication
	- process of establishing identity of person or service that wants to access a resource
	- Challenges a party for legitimate credentials and provides security principal for access and control
	- Establishes whether the user is who they say they are
- Authorization
	- Establishes levels of access for an already authenticated user
	- What data they're allowed access, and what they can do with it


# Define Azure Active Directory

- provides identity services that enable your users to sign in and access both Microsoft cloud applications and cloud applications that you develop
- is for:
	- IT Admins: Control access to apps and resources based on business
	- App Devs: adding functionality to apps they build, such as sso or enabling apps to works with existing creds
	- Users: Manage identities, self-password reset
	- Online service subscribers: Microsoft 365, Office 365, Azure, etc
- It provides:
	- Authentication
	- SSO
	- App Management
	- Device Management
- can connect an AD with Azure AD using Azure AD Connect


# Describe the functionality and usage of Azure Active Directory

- provides identity services that enable your users to sign in and access both Microsoft cloud applications and cloud applications that you develop
- cloud-based identity and access management service
- you control the identity accounts, but Microsoft ensures that the service is available globally
- is for:
	- IT administrators:  can use Azure AD to control access to applications and resources based on their business requirements.
	- App developers: can use Azure AD to provide a standards-based approach for adding functionality to applications that they build, such as adding SSO functionality to an app or enabling an app to work with a user's existing credentials.
	- Users: can manage their identities. For example, self-service password reset enables users to change or reset their password with no involvement from an IT administrator or help desk.
	- Online service subscribers: Microsoft 365, Microsoft Office 365, Azure, and Microsoft Dynamics CRM Online subscribers are already using Azure AD. A tenant is a representation of an organization. A tenant is typically separated from other tenants and has its own identity. Each Microsoft 365, Office 365, Azure, and Dynamics CRM Online tenant is automatically an Azure AD tenant.
- services:
	- Authentication: includes verifying identity to access applications and resources, and providing functionality such as self-service password reset, multifactor authentication, a custom list of banned passwords, and smart lockout services.
	- Single sign-on: enables you to remember only one username and one password to access multiple applications. A single identity is tied to a user, which simplifies the security model. As users change roles or leave an organization, access modifications are tied to that identity, which greatly reduces the effort needed to change or disable accounts.
	- Application management: You can manage your cloud and on-premises apps by using Azure AD. Features like Application Proxy, SaaS apps, the My Apps portal (also called the access panel), and single-sign on provide a better user experience.
	- Device management: Along with accounts for individual people, Azure AD supports the registration of devices. Registration enables devices to be managed through tools like Microsoft Intune. It also allows for device-based conditional access policies to restrict access attempts to only those coming from known devices, regardless of the requesting user account.


# Describe the functionality and usage of Conditional Access, Multi-Factor Authentication (MFA), and Single Sign-On (SSO)

## Single Sign On (SSO)

- enables a user to sign in one time and use that credential to access multiple resources and applications from different providers.
- makes it easier for users to manage their identities and increases your security capabilities.
Multifactor Auth

- When a user is prompted for additional info at sign in
	- email address and pwd
	- Code sent to phone
	- fingerprint / face recognition
- increases identity security by limiting the impact of credential exposure


## Azure AD Multi-Factor Auth

- Comes with Azure Active Directory and Multifactor Auth for Office 365
- service that provides multifactor authentication capabilities


## Conditional Access

- tool that Azure Active Directory uses to allow (or deny) access to resources based on identity signals
- Allow or deny access based on identity signals
	- Includes who the user is, where they are coming from, and what devices they are using
- provides a more granular multifactor authentication experience for users
- Used when you need. to:
	- require MFA to access an app
	- require access to services through approved client apps
	- require users to access apps only through managed devices
	- block access from untrusted sources
- useful when you need to:
	- Require multifactor authentication to access an application.
	- Require access to services only through approved client applications.
	- Require users to access your application only from managed devices.
	- Block access from untrusted sources, such as access from unknown or unexpected locations.
