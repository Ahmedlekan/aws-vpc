# Custom VPCs

- Regional Service: A VPC spans all Availability Zones (AZs) within a specific AWS region.

- Isolated Network: By default, a VPC is an isolated network. No traffic can enter or leave the VPC without explicit configuration.

- Flexible Configuration: VPCs can be configured for simple or complex multi-tier architectures.

- Hybrid Networking: VPCs support hybrid cloud setups, allowing connections to other cloud environments and on-premises data centers.

Tenancy Options:

- Default Tenancy: Resources are shared with other AWS customers.

- Dedicated Tenancy: Resources are isolated for your use only.


### VPC Sizing and IP Addressing

IPv4 Addressing

1. Primary Private IPv4 CIDR Block:

- Required for every VPC.

- Size Range: Minimum /28 (16 IP addresses) to Maximum /16 (65,536 IP addresses).

2. Secondary IPv4 CIDR Blocks:

- Optional additional CIDR blocks can be added to the VPC.

3. Public IPs:

- Public IP addresses can be assigned to instances for external communication.

### IPv6 Addressing

1. Optional IPv6 CIDR Block:

- A single /56 IPv6 CIDR block can be assigned to the VPC.

- Provides a large address space for modern applications.

### DNS in a VPC

1. DNS Services

- Provided by Route 53: AWS Route 53 provides DNS services for VPCs.

VPC DNS IP Address:

- The base IP address of the VPC plus 2 (e.g., 10.0.0.2).

### DNS Configuration Options

enableDnsHostnames:

- When enabled, instances in the VPC are assigned DNS hostnames.

- Example: ip-10-0-0-10.ec2.internal.

enableDnsSupport:

- When enabled, DNS resolution is supported within the VPC.

- Allows instances to resolve domain names to IP addresses.


## Create VPC

- Name tag

![Image](https://github.com/user-attachments/assets/f988ff37-ba8f-4665-a153-31a45019c7d7)

- IPv4 CIDR

![Image](https://github.com/user-attachments/assets/652eca1b-7763-45e9-933e-6e6604047db5)

- IPv6 CIDR block

![Image](https://github.com/user-attachments/assets/a409a8c5-2611-4120-9fe0-b843f8af3e7f)

- Tenancy

![Image](https://github.com/user-attachments/assets/a17ba613-ee33-4924-be68-3079cbdfa4b1)

- Click on create vpc


- Click on the edit vpc settings and enables DNS settings ans save.

![Image](https://github.com/user-attachments/assets/4496e099-061c-44be-b139-059cb3ac9957)


## VPC Subnets 

### Implement multi-tier VPC subnets 

1. Create subnet A

- Subnet 1 - Us-East-1a - For the Reserved A

![Image](https://github.com/user-attachments/assets/1d00f5ac-65ff-40fd-8629-e06ba598e53d)

- Subnet 2 - Us-East-1a - For the Database A

![Image](https://github.com/user-attachments/assets/b7fdfc9a-0fdc-4d86-9a6d-1261fb056e9f)

- Subnet 3 - Us-East-1a - For App A

![Image](https://github.com/user-attachments/assets/2fc436b1-73f4-4ab3-87ca-3e930f19397d)

- Subnet 4 - Us-East-1a -  For Web A

![Image](https://github.com/user-attachments/assets/72b0d203-b83a-44ce-8f71-94be05baf603)


2. Create Subnet B

- Create the same subnet process, A-Z Us-East-1b

- Make sure your IPv4 subnet CIDR are unique (e.g 10.16.80.0/20, 10.16.96.0/20)

- Make sure your IPv6 subnet CIDR are unique (2600:1f18:7bc:ca04::/64, 2600:1f18:7bc:ca05::/64)


3. Create Subnet 3

- Follow the steps above for the Us-East-1c


4. Click on each subnet, edit subnet settings and enable Auto-assign IPv6 settings. 

![Image](https://github.com/user-attachments/assets/874dd866-e13f-4f6d-9076-c037fa0ebeb3)










