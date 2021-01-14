# Describe basic features of Azure Security Center, including policy compliance, security alerts, secure score, and resource hygiene

- Monitoring service that provides visibility of secure posture across all services
	- security posture means cybersecurity and controls and how to predict, prevent, and respond to threats
- Monitor security settings across workloads
- Automatically apply settings to resources as they come online
- security recommendations based on current configurations, resources, and networks
- monitor resources and perform automatic security assessments
- ML to detect and block malware from being installed on VMs
- Detect and analyze inbound attacks and investigate threats
- Provide just-in-time access control for network ports. Doing so reduces your attack surface by ensuring that the network only allows traffic that you require at the time that you need it to.
- Provides a resource security hygiene section that allows users to see the health of its resources from a security perspective. To help prioritize remediation actions, recommendations are categorized as low, medium, and high.
- Provides secure scores to measure a resource's security posture
	- Group of related security recommendations
	- Based on pct o security controls you satisfy
	- Helps protect orgs from threats
- Understand security posture
- Get security score based on security controls, groups of related security recommendations
- Cloud defense capabilities
	- Just in time: blocks traffic to specific network ports of virtual machines but allows traffic for specific time
	- Adaptive app controls: control which apps can run on it's VMs. Behind the scenes, Security Center will run ML to detect traffic and throws exceptions for resource groups that hold VMs and provides recommendations
	- Network Hardening: monitor internet traffic patterns of the VMs and compare traffic to the companies current security groups
	- file integrity monitoring: monitor changes to files that may suggest a security attack


# Describe the functionality and usage of Key Vault

- Store and manage secrets: store and tightly control access to tokens, passwords, certificates, API keys, and other secrets.
- manage encryption keys: 
- manage ssl/tls certs: provision, manage, and deploy your public and private Secure Sockets Layer / Transport Layer Security (SSL/TLS) certificates for both your Azure resources and your internal resources
- store secrets backed by security modules: can be protected either by software or by FIPS 140-2 Level 2 validated HSMs.
- centralizes secrets
- securely stores secrets and access keys
- access monitoring and control
- simplified admin of secrets: easier to enroll and renew certificates from public certificate authorities (CAs). You can also scale up and replicate content within regions and use standard certificate management tools.
- integration with other azure services


# Describe the functionality and usage of Azure Sentinel

- Collect cloud data at scale: all users, devices, applications, and infrastructure
- detect previously undetected threats: minimize false positives through Microsoft's analytics and threat intelligence
- investigate threats using AI
- Respond to incidents rapidly: built-in automation and orchestration of common tasks
- connect microsoft solutions like Microsoft Threat Protection solutions, Microsoft 365 sources (including Office 365), Azure Active Directory, and Windows Defender Firewall
- connect other services and solutions including AWS CloudTrail, Citrix Analytics (Security), Sophos XG Firewall, VMware Carbon Black Cloud, and Okta SSO.
- connect industry standard data sources that use the Common Event Format (CEF) messaging standard, Syslog, or REST API.
- Detect threats, and investigate and respond
	- allows further investigation on different incidents (or group of related alerts)
	- can review information from entities directly connected to the alert and see common exploration queries to help guide the investigation
- use Azure Monitor Workbooks  to automate responses to threats


# Describe the functionality and usage of Azure Dedicated Hosts

- Dedicated physical servers to host VM 6for Windows and Linux
- Gives visibility into and control over the server infrastructure thats running the VMs
- Helps address compliance requirements by deploying your workloads on an isolated server.
- Lets you choose the number of processors, server capabilities, VM series, and VM sizes within the same host.
- host price is based on the VM family, type (hardware size), and region.