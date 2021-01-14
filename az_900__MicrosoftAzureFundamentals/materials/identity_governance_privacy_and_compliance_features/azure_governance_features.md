# Describe the functionality and usage of Role-Based Access Control (RBAC)

- Permissions that get assigned to roles, that are then assigned to users
- Azure provides built-in roles that describe common access rules for cloud resources
- can also define your own roles
- Role-based access control is applied to a scope, including:
	- A management group (a collection of multiple subscriptions).
	- A single subscription.
	- A resource group.
	- A single resource.
- Owner roles at the management group scope can manage everything in all subscriptions within the management group
- Reader roles at the subscription scope allow the member to view every resource group and resource within the subscription
- Contributor roles to an application at the resource group scope allow the user to manage resources of all types within that resource group, but no other resource groups within the subscription
- Use when you need to:
	- Allow one user to manage VMs in a subscription and another user to manage virtual networks.
	- Allow a database administrator group to manage SQL databases in a subscription.
	- Allow a user to manage all resources in a resource group, such as virtual machines, websites, and subnets.
	- Allow an application to access all resources in a resource group.
- Uses an allow model


# Describe the functionality and usage of resource locks

- warning system that reminds you that a resource should not be deleted or changed.
- prevents resources from being changed or deleted
	- CannotDelete
	- ReadOnly
- Can combine this with Azure Blueprints to make it more robust


# Describe the functionality and usage of tags

- Using tags is useful for:
	- Resource management: enable you to locate and act on resources that are associated with specific workloads, environments, business units, and owners
	- Cost management optimization: enable you to group resources so that you can report on costs, allocate internal cost centers, track budgets, and forecast estimated cost.
	- Operations management: enable you to group resources according to how critical their availability is to your business. This grouping helps you formulate service-level agreements (SLAs). An SLA is an uptime or performance guarantee between you and your users.
	- Security: enable you to classify data by its security level, such as public or confidential.
	- Governance and regulatory compliance: enable you to identify resources that align with governance or regulatory compliance requirements, such as ISO 27001.
	- Workload Optimization and automation: help you visualize all of the resources that participate in complex deployments


# Describe the functionality and usage of Azure Policy

- service in Azure that enables you to create, assign, and manage policies that control or audit your resources
- enforce different rules and effects over your resource configurations so that those configurations stay compliant with corporate standards
- enables you to define both individual policies and groups of related policies, known as initiatives
- evaluates your resources and highlights resources that aren't compliant with the policies you've created. 
- can also prevent noncompliant resources from being created.
- Policy initiative is a way of grouping related policies into one set
- assigned at the scope level


# Describe the functionality and usage of Azure Blueprints

- can define a repeatable set of governance tools and standard Azure resources that your organization requires
- orchestrates the deployment of various resource templates and other artifacts, such as:
	- Role assignments
	- Policy assignments
	- Azure Resource Manager templates
	- Resource groups
- component in the blueprint definition is known as an artifact.


# Describe the Cloud Adoption Framework for Azure

- Consists of tools, docs, and proven best-practices
- helps you create and implement the business and technology strategies needed to succeed in the cloud.
- Stages:
	- Define strategy
		- Define and doc motivations
		- doc business outcomes
		- develop business case
		- Choose the right first project
	- make a plan
		- Digital estate (inventory existing digital assets)
		- initial org alignment
		- skills readiness plan
		- cloud adoption plan
	- ready the org
		- Azure setup guide
		- landing zone
		- expand landing zone
		- best practices
	- adopt the cloud
		- migrate first workload
		- migration scenarios
		- best practices
		- process improvements
	- Innovate
		- Business value consensus
		- innovation guide
		- best practices
		- feedback loops
	- govern and manage environments
		- methodology
		- benchmark
		- initial governance foundation
		- improve foundation
	- manage
		- establish management baseline
		- business commitments
		- expand baseline
		- advanced operations and design principles