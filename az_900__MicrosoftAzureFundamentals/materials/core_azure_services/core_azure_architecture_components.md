# Describe the benefits and usage of Regions and Region Pairs

-  region is a geographical area on the planet that contains at least one but potentially multiple data centers that are nearby and networked together with a low-latency network
- Azure has more global regions than any other cloud provider
- They also preserve data residency for your services
- Specialized regions for compliance or legal purposes
	- US DoD Central, US Gov Virginia, US Gov Iowa and more: These regions are physical and logical network-isolated instances of Azure for U.S. government agencies and partners. These data centers are operated by screened U.S. personnel and include additional compliance certifications.
	- China East, China North, and more: These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft doesn't directly maintain the data centers.
- Each Azure region is always paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away to allow for the replication of resources (such as VM storage) across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect both regions at once
- Advantages of region pairs:
	- If an extensive Azure outage occurs, one region out of every pair is prioritized to make sure at least one is restored as quickly as possible for applications hosted in that region pair.
	- Planned Azure updates are rolled out to paired regions one region at a time to minimize downtime and risk of application outage.
	- Data continues to reside within the same geography as its pair (except for Brazil South) for tax- and law-enforcement jurisdiction purposes.


# Describe the benefits and usage of Availability Zones

- Availability zones are physically separate data centers within an Azure region
- Azure can help make your app highly available through availability zones by ensuring your services and data are redundant so you can protect your information in case of failure
- Each availability zone is made up of one or more data centers equipped with independent power, cooling, and networking
- Set up to be an isolation boundary. If one zone goes down, the other continues working. 
- Connected through high-speed, private fiber-optic networks
- Not every region has support for availability zones. For an updated list, see Regions that support availability zones in Azure 
- Apps that use AZ fall into 2 categories
	- Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses)
	- Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database)


# Describe the benefits and usage of Subscriptions

- Groups together user accounts and resources those users have created
- Defines limits or quotas around the amount of resources you can create and use
- Manages costs and resources created within
- Provides users with authenticated and authorized access to products and services
- Allows you to provision resources
- Define boundaries around products, services and resources
	- Billing boundary: determines how an Azure account is billed for using Azure. Azure generates separate billing reports and invoices for each subscription so that you can organize and manage costs
	- Access control boundary: Azure applies access-management policies at the subscription level, and you can create separate subscriptions to reflect different organizational structures. An example is that within a business, you have different departments to which you apply distinct Azure subscription policies. This billing model allows you to manage and control access to the resources that users provision with specific subscriptions.
- Can create subscription for resource  or billing management purposes. For example, they can help separate:
	- Environments such as dev, test, security
	- Org structures such as IT vs lower-cost resources
	- Billing to manage and track costs
- Some limitations: Azure ExpressRoute circuits per subscription is 10


# Describe the benefits and usage of Management Groups

- Help manage access, policy, and compliance for multiple subscriptions
- All subscriptions inherit conditions applied to the parent management group
- You can apply policies to a management group that limits the regions available for VM creation
- 10,000 management groups can be supported in a single directory
- A management group tree can support up to six levels of depth. This limit doesn't include the root level or the subscription level
- Each management group and subscription can support only one parent
- Each management group can have many children
- All subscriptions and management groups are within a single hierarchy in each directory


# Explain Azure Resources

- instances of services you create
- examples: Virtual Machines, storage, or SQL DBs


# Describe the benefits and usage of Resource Groups

- Resources combined into resource groups, serving as a logical container into which resources are deployed and managed
- Can't be nested
- Resources must be placed in resource groups
- Deleting a resource group also deletes children resources living inside
- Scope for applying role-based access control (RBAC) permisions


# Describe the benefits and usage of Azure Resource Manager

- Deployment and management service for Azure
- Enables creation, updating, and deleting resources within an account
- Features such as access control, locks, and tags
- Manage your infrastructure through declarative templates rather than scripts. A Resource Manager template is a JSON file that defines what you want to deploy to Azure.
- Deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.
- Redeploy your solution throughout the development life cycle and have confidence your resources are deployed in a consistent state.
- Define the dependencies between resources so they're deployed in the correct order.
- Apply access control to all services because RBAC is natively integrated into the management platform.
- Apply tags to resources to logically organize all the resources in your subscription.
- Clarify your organization's billing by viewing costs for a group of resources that share the same tag.