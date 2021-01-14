# Describe the concept of defense in depth

- to protect information and prevent it from being stolen by those who aren't authorized to access it.
- uses a series of mechanisms to slow the advance of an attack that aims at acquiring unauthorized access to data.
- Physical security layer is the first line of defense to protect computing hardware in the datacenter
	- buildings/access to computing hardware
- Identity and access layer controls access to infrastructure and change control
	- control access to infrastructure and change control
	- sso
	- audit events and changes
- perimeter layer uses distributed denial of service (DDoS) protection to filter large-scale attacks before they can cause a denial of service to users
	- DDoS to filter large-scale attacks before they can affect the availability of systems to users
	- firewalls
- network layer limits communication between resources via segmentation and access controls
	- limit communication between resources
	- deny by default
	- restrict inbound internet access and limit outbound access
	- implement secure connectivity
- compute layer secures access to VMs
	- secure access to VMs
	- endpoint protection and keep systems patched and current
- application layer helps ensure apps are secure and free of security vulnerabilities
	- ensure secure and free of vulnerabilities
	- store sensitive app secrets in a secure storage medium
	- security a design requirement
- data layer controls access to the business and customers data need to protect (generally attackers try to get this)
	- stored in db
	- stored in disk
	- stored in SaaS
	- managed through cloud
	

# Describe the functionality and usage of Network Security Groups (NSG)

- enables you to filter network traffic to and from Azure resources within an Azure virtual network
- like an internal firewall
- can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, port, and protocol.


# Describe the functionality and usage of Azure Firewall

- managed, cloud-based network security service that helps protect resources in your Azure virtual networks
- stateful: analyzes the complete context of a network connection, not just an individual packet of network traffic
- static (unchanging) public IP address for your virtual network resources, which enables outside firewalls to identify traffic coming from your virtual network
- high availability and unrestricted cloud scalability.
- Unrestricted cloud scalability.
- Inbound and outbound filtering rules.
- Inbound Destination Network Address Translation (DNAT) support.
- Azure Monitor logging.


# Describe the functionality and usage of Azure DDoS protection

- helps protect your Azure resources from DDoS attacks
	- DDoS attacks: attempts to overwhelm and exhaust an application's resources, making the application slow or unresponsive to legitimate users. DDoS attacks can target any resource that's publicly reachable through the internet, including websites.
- identifies the attacker's attempt to overwhelm the network and blocks further traffic from them, ensuring that traffic never reaches Azure resources
- Tiers:
	- Basic: automatically enabled for free as part of your Azure subscription. Always-on traffic monitoring and real-time mitigation of common network-level attacks provide the same defenses that Microsoft's online services use. The Basic service tier ensures that Azure infrastructure itself is not affected during a large-scale DDoS attack. The Azure global network is used to distribute and mitigate attack traffic across Azure regions.
	- Standard: additional mitigation capabilities that are tuned specifically to Azure Virtual Network resources. always-on traffic monitoring and real-time mitigation of common network-level attacks.
- Helps prevent:
	- Volumetric attacks: flood network layer with a substantial amount of seemingly legitimate traffic.
	- Protocol attacks: These attacks render a target inaccessible by exploiting a weakness in the layer 3 and layer 4 protocol stack.
	- Resource-layer (application-layer) attacks (only with web application firewall): These attacks target web application packets to disrupt the transmission of data between hosts. You need a web application firewall (WAF) to protect against L7 attacks. DDoS Protection Standard protects the WAF from volumetric and protocol attacks.