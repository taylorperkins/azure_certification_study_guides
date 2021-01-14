


# Describe the benefits and usage of Virtual Machines, Azure App Services, Azure Container Instances (ACI), Azure Kubernetes Service (AKS), and Windows Virtual Desktop

## Virtual Machines

- software emulations of physical computers
- processors, memory, storage, and networking
- host an operating system and can run software like a normal. computer
- IaaS
- Ideal when you need: 
	- total control over the OS
	- ability to run custom software
	- use custom hosting config
- Use pre-configured _images_ (template used to create a VM)
	- Already include OS and other software like dev tools or web hosting environments
- When to use VMs
	- During testing and development
	- running apps in the cloud
	- Extending datacenter to the cloud (such as sharepoint)
	- during disaster recovery


## VM Scale Sets

- manage sets of identical, load-balanced VMs
- Used to scale VM
- designed to support true autoscale
- no pre-provisioning required
- centrally manage, configure, and update a large number of VMs in minutes to provide highly available applications
- number of VM instances can automatically increase or decrease in response to demand or a defined schedule
- build large-scale services for areas such as compute, big data, and container workloads.


## Batch

- large scale parallel and high-performance computing
- when running a job, batch will:
	- start a pool of VMs for you
	- install apps and staging data
	- runs jobs with as many tasks as you have
	- identifies failures
	- re-queues work
	- scales down as pool completes


## Containers

- Used to manage and deploy containers
- Multiple instances of a container in a host machine
- What is a container?
	- virtualization environment. Containers control the OS whereas VMs control the hardware
- Generally used in microservice architecture which allows you to separate portions of your app into logical sections that can be maintained, scaled, or updated independently.



## Container Instances 

- fastest and simplest way to run a container in Azure
- PaaS


## Kubernetes

- Orchestrating is the task of automating, managing, and interacting with a large number of containers. 
- handles the orchestration of containers
- Typicallly used in a microservice architecture


## App Services

- PaaS
- Build and host web apps, background jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure. 
- Offers automatic scaling and high availability. 
- Supports Windows and Linux and enables automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.
- Host most common app service styles like: 
	- Web apps: ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python with Windows or Linux as the host operating system
	- API apps: REST-based web APIs by using your choice of language and framework. full Swagger support and the ability to package and publish your API in Azure Marketplace. HTTP- or HTTPS-based client
	- WebJobs: run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) in the same context as a web app, API app, or mobile app through a schedule or trigger
	- Mobile Apps
- handles most of the infrastructure decisions you deal with in hosting web-accessible apps:
	- Deployment and management are integrated into the platform.
	- Endpoints can be secured.
	- Sites can be scaled quickly to handle high traffic loads.
	- The built-in load balancing and traffic manager provide high availability.


## Windows Virtual Desktop

- desktop and application virtualization service that runs on the cloud. 
- Enables your users to use a cloud-hosted version of Windows from any location. 
- Windows Virtual Desktop works across devices like Windows, Mac, iOS, Android, and Linux. 
- It works with apps that you can use to access remote desktops and apps. 
- Users have the freedom to connect to Windows Virtual Desktop with any device over the internet
- Simplifies management, gives options to load balance users on a VM host pool, users can have multiple sessions


# Describe the benefits and usage of Virtual Networks, VPN Gateway, Virtual Network peering, and ExpressRoute

## VNet Peering

- enables resources in each virtual network to communicate with each other. These virtual networks can be in separate regions, which allows you to create a global interconnected network through Azure.
- UDR (user-defined Routing) is a significant update to Azure’s Virtual Networks as this allows network admins to control the routing tables between subnets within a subnet as well as between VNets thereby allowing for greater control over network traffic flow.

## Virtual Networks

- Generally provides the key networking capabilities: 
	- Isolation and segmentation
	- Internet communications
	- Communicate between Azure resources
	- Communicate with on-premises resources
	- Route network traffic
	- Filter network traffic
	- Connect virtual networks
- Enables resources, such as VMs, web apps, and databases, to communicate to one another, with users on the internet, and with your on-prem client computers
- Provide the following capabilities:
	- Isolation and segmentation
		- Define private IP by using either private or public IP ranges
		- Further divide that range into subnets and allocate part of the defined space to each named subnet
	- Internet communications
		- VMs can connect to the internet by default
		- Enable incoming connections from the internet by defining a public IP or public load balancer
	- Communication between Azure resources
		- Virtual networks
			- Connect to other VMs as well as other resources
		- Service Endpoints
			- Connect to other resource types, such as databases and storage accounts
	- Communication with on-premises resources
		- Point-to-site virtual private networks
		- site-to-site virtual private networks
		- azure express route
			- env that need greater bandwidth and higher levels of security 
			- doesn't travel over the internet
	- Route network traffic
		- Route tables: define rules about how traffic should be directed. Create custom route tables that control how packets are routed between subnets
		- Border gateway control
	- Filter network traffic
		- Network security groups
		- network virtual appliances
	- Connect VN
		- Using virtual network peering
			- enables resources in each Vnet to communicate with each other
		- User defined routing (UDR)
			- allows network admins to control the routing tables between subnets within a subnet as well as between VNets
	- Creating Virtual Networks
		- Address space: Classless Interdomain Routing (CIDR) format
		- Network name
		- subscription
		- resource group: virtual network needs to exist in a resource group
		- location
		- subnet: you can create one or more subnets that partition the virtual network's address space. Routing between subnets will then depend on the default traffic routes. You also can define custom routes. Alternatively, you can define one subnet that encompasses all the virtual networks' address ranges.
		- DDoS protection: Basic or Standard DDoS protection
		- Service Endpoints: enable service endpoints such as Azure Cosmos DB, Azure Service Bus, Azure Key Vault, and so on
		- Network SG: enable you to filter the type of network traffic that can flow in and out of virtual network subnets and network interfaces.
		- Route table


## VPN Gateway Fundamentals

- type of private interconnected network that uses an encrypted tunnel within another network. 
- generally, they are deployed to connect two or more trusted private networks to one another over an untrusted network.
- enable the following activity:
	- Connect on-prem data centers to Vnets through site-to-site connections
	- Connect individual devices to Vnets through a point-to-site conn
	- Connect Vnets to other virtual networks through a network-to-network conn
- Policy-based VPNs
	- Specify statically the IP address of packets that should be encrypted through each tunnel
	- Supports IKEv1 only
	- Use of static routing
	- must be used in specific scenarios that require them
- Route based VPN
	- Use when you need:
		- Connections between VNets
		- Point-to-site connections
		- multisite connections
		- coexistence with an azure ExpressRoute Gateway
- Requires:
	- VNet
	- GatewaySubnet
	- Public IP
	- Localnetwork Gateway
	- Connection


## ExpressRoute

- Lets you extend on prem networks into the cloud over a private connection.
- Lets you establish connections to Microsoft cloud services, such as Azure and Microsoft 365
- Open Systems Interconnection (OSI) model:
	- Layer 2 (L2): 
		- Data Link Layer, which provides node-to-node communication between two nodes on the same network.
	- Layer 3 (L3): 
		- Network Layer, which provides addressing and routing between nodes on a multi-node network.
- features and benefits:
	- Layer 3: any IPVPN network, point-to-point ethernet, or through a virtual cross-connection
	- connectivity to cloud services across all regions and geopolitical region
	- Global conenctivity to services
		- CloudExchange colocation
		- Point-to-point Ethernet connection
		- Any-to-any connection

	- Dynamic routing 
	- redundancy
	- connection uptime SLA
	- Layer 3 (address-level) connectivity between on-prem network and cloud


# Describe the benefits and usage of Container (Blob) Storage, Disk Storage, File Storage, and storage tiers

## Disk Storage

- provides disks for VMs
- Apps and other services can access and use the disks as needed. 
- Can be SSD or HDD with varying performance tiers. 
- Tiers:
	- standard SSD for mission critical workloads
	- premium SSD for mission critical production apps
	- ultra disks for data intensive workloads such as SAP HANA, top tier db, and transaction-heavy workloads.


## Blob Storage

- Access Tiers: 
	- Hot: optimized for storing data that is accessed frequently
	- Cool : infrequently accessed data and stored for at least 30 days
	- Archive: Rarely accessed data and stored for at least 180 days, with flexible latency requirements
	- Only hot and cool tiers can be set at the account level
	- All tiers can be set at blob level, during or after upload
	- Cool tier can tolerate slightly lower availability, but still requires high durability, retrieval latency, and throughput characteristics to hot data
	- Archive stores data offline with highest cost to rehydrate and access data
- Can hold any type of data
- Good for big data tasks
- Can manage thousands of simultaneous uploads, video data, constantly growing log files, etc
- Isnt limited to common file formats
	- Can hold gbs of binary streamed from scientific instrument etc
- Ideal for
	- serving images or docs to browser
	- storing files for distributed access
	- streaming 
	- backup/restore/recovery
	- analysis
	- up to 8TB for VM
	  

## Azure Files

- Fully managed file shares accessible by SMB and NFS protocols
- Can be mounted to Windows, Linux, MacOS, VMs
- Use for:
	- Migrating existing file shares to the cloud
	- Storing config files to be accessed by multiple VMs
	- Writing data to file share to be processed and analyzed later (interim)
- Can access files from anywhere in the world y using a URL that points to the file
- Can use SAS (Shared Access Signature) tokens to allow access for a specific amount of time


# Describe the benefits and usage of Cosmos DB, Azure SQL Database, Azure Database for MySQL, Azure Database for PostgreSQL, and SQL Managed Instance

## Azure Cosmos DB

- globally-distributed
- multi-model database service
- Elastically and independently scales throughput and storage across any number of azure regions
- Supports schema-less data 
- Flexible
- Atom-record-sequence format
- Supports SQL, MongoDB, Cassandra, Tables, and Gremlin


## Azure SQL DB

- Relational db based on the latest version of SQL Server
- PaaS - handles upgrading, patching, backups, and monitorin g
- 99.99% availability
- Can process both relational and non-relational structures like graphs, JSON, spatial, and XML 
- Migrate existing SQL Server db with minimal downtime

## Azure SQL Managed Instance

- Scalabled cloud data service providing the broadest SQL Server db engine compatibility with all features of PaaS
- Very similar to Azure SQL DB, but some extra features like server collation
	- Full comparison: https://docs.microsoft.com/en-us/azure/azure-sql/database/features-comparison
- Easy migration between on-prem data to the cloud. using the Database Migration Service (DMS) or native backup and restore
	- Detailed migration process: https://docs.microsoft.com/en-us/azure/azure-sql/migration-guides/managed-instance/sql-server-to-managed-instance-guide
	  

## DB for MySQL

Azure supports LAMP stack
- Relational DB based on the MySQL Community Edition DB engine (version 5.6, 5.7, and 8.0)
- 99.99% availablility
- Built-in security, fault tolerance, data protection
- Point-in-time restore
- Built-in high availability with no additional cost
- Predictable performance and inclusive, pay-as-you-go pricing
- Scale as needed, within seconds
- Ability to protect sensitive data at-rest and in-motion
- Automatic backups
- Enterprise-grade security and compliance
- Migrate existing MySQL DB with minimal downtime by using DMS


## DB for PostgreSQL

- Relational DB within the cloud
- based on community version of the open-source PostgreSQL db engine
- Built-in high availability compared to on-premises resources. There's no additional configuration, replication, or cost required to make sure your applications are always available.
- Simple and flexible pricing. You have predictable performance based on a selected pricing tier choice that includes software patching, automatic backups, monitoring, and security.
- Scale up or down as needed, within seconds. You can scale compute or storage independently as needed, to make sure you adapt your service to match usage.
- Adjustable automatic backups and point-in-time-restore for up to 35 days.
- Enterprise-grade security and compliance to protect sensitive data at-rest and in-motion. This security covers data encryption on disk and SSL encryption between client and server communication.
- Deployment options: 
	- Single Server: 
		- high-availability 
		- predictable performance and inclusive pay-as-you-go
		- vertical scale as needed
		- monitoring and alerting
		- security and compliance
		- protects sensitive data
		- automatic backups
	- Hyperscale
		- horizontally scales against multiple machines via sharding
		- parallelizes queries across these servers for a faster response time with large datasets
		- best with datasets upward of 100GB of data
		- multi-tenant applications
		- real-time operational analytics
		- high throughput transactional workloads


# Describe the benefits and usage of Azure Marketplace
