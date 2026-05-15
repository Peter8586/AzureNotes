Azure Active directory - 

creating a user account - Must create a group

Enabling MFA -


Azure computing services - 
Azure VM runs windows ore linux  - most common type of compute you choose your os, memory, cpu, storage. 

azure containers instances - docker as a service 

azure kubernetes service - easy to deploy manage and scale containerized apps 

azure service fabric - tier 1 enterprise container as a service. distribute systems platforms - run azure as on premises 

azure functions 0 event driver serverless compute 

azure batch 0 plan schedule and execute your batch computer workloads across running 100 hoba in parallel use spot vms to save money 

Azure VMs - is ahighly configurable server -  



Public cloud - everything built on the cloud provider aks known as: cloud native 

Private cloud - everything build on companues datacenters known as On-premises the cloud coulf be openstakc 

Hybrid _ using both on premises and cloud service provider 

Cross - Cloud - using multiple cloude provider aka multi-cloud, hybrid-cloud

Total cost of ownership TCO 

On-premise 
Software license fees 
Implementation 
configs 
physical hardware 
IT personel 
maintenance 

Azure 
Subscription fees 
implementation 
configs 
training 


Capex vs Opex 

Capital Expenditure CAPEX 
Spending money upfront on physical infrastucure 
Server costs 
storage costs 
network costs 
backup and archive costs 
datacenter recovery 
tech personel 

Operation Expenditure OPEX 
Leasing software and costimizing features 
training employees in cloud service 
paying for cloud support 
billing based on cloud metrics 
computer usage 
storage usage 


cloud architecture terminologies 
Architect a tech org that architects a technical solution usinf multiple systems 

cloud architect 
focused  solely on architecting technical soltuions using cloud services.

a cloud architect needs to understand the following terms 

1. availability - ensure a service reamins available. 
2. Scalability - grow rapidly or unimpeded 
3. Elasticity - shrink and grot to meet the demand 
4. Fault tolerance - prevent failure 
5. Disaster - recover from a failure. 

always needs to consider 

1. security 
2. cost 


High Availability -  remain avaialable: no single point of failure 
running your work across multiple AZ ensure that if 1 or 2 Azs become unavailable your service/applications remain available. 
 
How would you distribute traffic? Azure load Balancer: A load balancer allows you to evenly distribute traffic to multiple servers in one or datacenter. if a datacetner or server is down, the load balancer will route the traffic to only available datacenters with servers. 

High Scalability: increase your capacity based on the increasing demand to traffic, memory and computing power. 

Vertical Scaling: Scaling up -> upgrade to a bigger server 
Horizontal Scaling : Scaling Out -> Add more servers of the same size 

Azure VM Scalet set: Automatically increase or descrease in response to demand or a defined schedule. 

High Elasticity - automaticallty increase or decrease your capacity based on the current demand of traffic, memory and computing power 

Horizontal scaling: scaling out adding more servers - scaling in - removing servers of the same size. 

SQL Server Stretch Database- dynamically strech warm and cold trasactional data from MS SQL server 2016  to MS Azure 
 
Fault Tolerance: No single point of failure: preventing the chance of failute: 
Fail-overs: plan to shift traffic to a redundant system in case primary system fails. 

primary database fails X -> failover to -> Sync to  secondary

secondary is on standby and only use if primary fails 


What to use in Azure to build out high fault tolerance system: 
Azure Traffic manager: DNS-based traffic balancer to fail-over from failing primary systems to a stanf-by secondary system.


High Durability: recover from disaster and prevent of loss of data. DISASTER RECOVERY (DR)
1. Do ou have a backup? 
2. How fast can you resotre that backup?
3. does your backup still work?
4. how do you ensure current live data is not corrupt?

BCP Business Continuity Plan (BCP)

BCP document that outlines how business will continue operating - during an unplanned disruption in services. 
the maximum acceptable amount of data loss after an unplanned data-loss incident , expressed as an amout of time. 
how much data are you willing to lose?

RPO Recovery Point - defines lenght of duration 
RTO Recovery time objective - maximum amount of downtime your business can tolerate without imcurring a sugnificant financil loss. 

Disaster recovery options:

Low 
Cold 
Backup & Restore - backup your data restore to new infrastructure  (HOURS) 
Pilot light - data is replicated to another region with the minimal services running (10Min)  
Warm Standby - scaled down copy of your infrastructure running ready to scale up (Minutes) 
High 
Hot 
 Multi-site active - Scaled up copy of your infra. in another region. Real Time 


Dedicated Servers: A physical server wholly utilized by a single customer. 
you havw to guess your capacity and you'll overpay for underutilizing server. limited OS
Multiple apps can result in conflicts in resource sharing. 
but you have a guarantee of security,privacy and full utility of underlying resources. 

VM - Virtual Machines - Multiple VM on one machine. 
Hypervisor is the software layer that lets you the VMS. 
Physical seerver shared by multiple customers 
you pay for a fraction of the server 
youll over pay for underutilized VM 
you are limited by your guest operating system.
multiple apps on a single VM can result in conflic in resource sharing

Containers - Virtula mchine running in multple containers 
Docker Deamon - software layer that let your run multiple containers 
you can max the ultilize the available capacity which is more cost-effective
your container share the same underlying is so containers are more effeicient thant multiple VMs 
multiple apps run side by side without being limited to the same OS requirements and will not cause conflics during resources sharing. 

Functions - a managed Vms running managed containers. known as Serverless Compute. 
upload a piece of code choose the amount of memory and duration. 
only responsible for code and data, nothing else. 
very cost effective, only pay for the time code is running, VMs only run when there is code to be executes. 
cold starts is a side-effect to this setup.


Regions and geographies - 

a region is a grouping of multiple datacenters AZ Availability Zones 
Azrue has 58 regions accrosss 140 countries 

a geo is a discreet market of tow or more regions that preserves data residency and compliance boundaries 

Paired regions: 
each region is paired with another region 300 miles away 

only one region is updates at a time to ensure no outages 

 Some azure services rely on paired regions for Disaster recovery 

Azure geo-redundant storage replicares dsata to a secondary region automatically, ensuring that data is durable even in the event that the primary region isnt recoverable. 

Types and services - 

(not all azure cloud services are available in every region) 

recommended region - majority of services will be available - designed to support availability zone. 

alternate region - not design to support availbility zone 

general availabilty - ready to be use by everyone GA - 

Azure cloud services grouped into threee categories 
1. foundational - available immediately or in 12 months in recommended and alternate regions 
2. mainstream - when GA immediatley or in 12 month recommended region -  alternate region avaible on customer demand 
3. available in recommended or alternate region based on customer demand 

Special regions - to meet compliance or legal reasons 
1. US DoD Central 
2. US Gov Virgina 
3. US Gov Iowa 

three azure government secret locations undisclosed. 

China East - North 

Availabilty Zones: a datacenter secred building that contains hundreds of thousands of computers 

a region will generally contain 3 AZ - isolate from each otheer but will provide low latency - common practice to run workloads in atleast 3 AZs to ensure remain av. in case 1 or 2 fail. 

Az support regions - not every region has support AZ 

recommended regions are suppose to have atleast 3 Azs 

the following have 3 AZs 
1. Central US 
2. East US 2 
3. West US 2 
4. West Europe 
5. France Central 
6. North Europe 
7. South Asia 

Fault and Update Domains 
Fault domain - a group of virtual machines that share a common power source or netwrok switch 

Update domain - azure may need to apply updates to the underlying hardware and software - update domain ensures your resources do no go offline

Av. Set 
group you can use in azure to ensure that the VMs you place in the av, set are different fault/update domains to avoid downtime. 

fault domains - each virtual machine in an av. set is assigned a fault domain and update domain


