# Identify factors that can affect costs (resource types, services, locations, ingress and egress traffic)

- Resource Type: Example with blob.. type, performance tier, access tier
- Usage Meters: similar to how you keep track of electricity or water bills (consumer-based). For example with a VM
	- Overall CPU
	- time spent with public IP
	- incoming (ingress) and outgoing (egress) network traffic
	- Disk size
- Resource Usage
- Subscription Types: May include usage allowances
- Marketplace: Billing structures are set up by the vendor
- Location can have different associated prices since it affects network traffic
- Billing zones: based on incoming and outgoing bandwidth. Typically, outgoing data transfers cost more


# Identify factors that can reduce costs (reserved instances, reserved capacity, hybrid use benefit, spot pricing)

- Understand estimated costs before deploying
- Use Azure Advisor to Monitor Usage
	- This can help identify underutilized or unused resources
- Use spending limits
- Reservations to prepay
	- Reservations will offer discounts if you prepay (up to 72 percent) compared to pay-as-you-go prices
- Choose low-cost locations and regions
- research available cost-saving offers
- Use Azure Cost Management and Billing to control spending
	- reporting
	- data enrichment
	- budgets
	- alerting
	- recommendations
- Apply tags to identify cost owners
- resize underutilized VMs
- Deallocate VM during off hours
- Delete unused resources
- Migrate from IaaS to PaaS services
- Save on licensing costs
- choose cost effective OS
- Use Azure Hybrid Benefit to repurpose software license


# Describe the functionality and usage of the Pricing calculator and the Total Cost of Ownership (TCO) calculator

- TCO helps you estimate the cost savings of operating your solution on Azure over time
- help you compare the cost of running in the datacenter versus running on Azure.
- Steps:
	- Define your workloads.
	- Adjust assumptions.
	- View the report.
- Pricing Calculator helps estimate costs for single resources (provides estimates and not actual price quotes)


# Describe the functionality and usage of Azure Cost Management

- free service that helps you understand your Azure bill, manage your account and subscriptions, monitor and control Azure spending, and optimize resource use
- Features include: 
	- reporting
	- data enrichment: categorizing resources with tags
	- budgets: monitor resource demand trends, consumption rates, and cost patterns
	- alerting: based on cost and usage budgets
	- recommendations: to eliminate idle resources and to optimize the Azure resources you provision