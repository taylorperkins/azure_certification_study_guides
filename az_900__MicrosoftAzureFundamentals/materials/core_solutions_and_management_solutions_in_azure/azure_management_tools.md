# Describe the functionality and usage of the Azure Portal, Azure PowerShell, Azure CLI, Cloud Shell, and Azure Mobile App

Generally, two types of tooling: Visual and code-based (Infrastructure as Code)
- IaC:
	- Imperative: Details each individual step that should be performed to achieve a desired outcome
- Visual
	- Declarative: details only a desired outcome and allows interpreter to best achieve that outcome


## Azure Portal / Mobile App

- See different resources through the GUI, not very scalable, but good for ad-hoc


## Powershell

Execute commands called cmdlets (commandlets) that call the Azure REST API to perform any command in Azure
	* Available in Windows, Mac, Linux
	

## Azure CLI

- Like boto3


# Describe the functionality and usage of Azure Advisor

- Evaluates resources and makes recommendations to help improve reliability, security, and performance
- Suggests actions to take right away, postpone, or dismiss
- Divided into five categories:
	- reliability
	- security
	- performance
	- cost
	- operational
- Analyze azure to reduce costs, improve resilience, or harden security


# Describe the functionality and usage of Azure Resource Manager (ARM) templates

- Declarative JSON format
- Verified before any code is executed
- Creates all resources in parallel


# Describe the functionality and usage of Azure Monitor

- Platform for collecting, analyzing, visualizing, or taking action based on criteria
- Monitor azure services or usage of azure
- measure custom events alongside other usage metrics
- Set up alerts for outages when autoscaling may deploy new instances
 

# Describe the functionality and usage of Azure Service Health

- Personalized view of the health of the services, regions, and resources you rely on
- Display major and minor, localized issues
- Setup alerts to help triage outages and planned maintenance