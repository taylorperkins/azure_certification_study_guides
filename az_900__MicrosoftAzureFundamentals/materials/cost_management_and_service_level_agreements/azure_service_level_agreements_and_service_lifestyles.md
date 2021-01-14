# Describe the purpose of an Azure Service Level Agreement (SLA)

- formal agreement between a service company and the customer
- defines the performance standards that Microsoft commits to for you, the customer
- https://azure.microsoft.com/support/legal/sla/
- Broken down into sections:
	- Intro: explains what to expect in the SLA, including its scope and how subscription renewals can affect the terms.
	- General terms: contains terms that are used throughout the SLA so that both parties (you and Microsoft) have a consistent vocabulary. For example, this section might define what's meant by downtime, incidents, and error codes.
	- Details: specific guarantees for the service. Performance commitments are commonly measured as a percentage. That percentage typically ranges from 99.9 percent ("three nines") to 99.99 percent ("four nines"). The primary performance commitment typically focuses on uptime, but can also focus on latency.
- Downtime refers to the time duration that the service is unavailable.
- Free products typically don't have an SLA.
- Outages/resource statuses can be found here: https://status.azure.com/status


# Identify actions that can impact an SLA (i.e. Availability Zones)

- Workloads
	- Multiply together all SLA for resources in a workload to get the composite SLA for those set of services
- Disks: Example being VM standard HDD Managed disk, Standard SSD Managed Disk, Premium SSD or Ultra Disk
- Tiers: Between Free and Standard Tiers
- Avoid having any single points of failure
	- deploy more instances of VMs across different availability zones in the same Azure region to ensure availability if one datacenter goes down
	- An availability zone is a unique physical location within an Azure region
- ensure redundancy within every part of the application (including the application itself) by duplicating components across regions


# Describe the service lifecycle in Azure (Public Preview and General Availability)

- service lifecycle defines how every Azure service is released for public use
- general availability is when a new Azure service is validated and tested, and released to all customers as a production-ready service
- Access new features through Public Preview
- Don't put these in prod, only dev