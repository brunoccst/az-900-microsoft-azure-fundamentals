# Microsoft Azure Fundamentals - AZ-900
This repository contains the results of **my** studies and understanding regarding the *[Exam AZ-900: Microsoft Azure Fundamentals](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900)*.

# Basic concepts

## What is the cloud
*Cloud Computing* is the term used for defining on-demand availability of computer system resources.

In general, a cloud consists of the same computer system resources (hardware, infrastructure, etc.) you would need to have for hosting your computing solutions, but instead of owning each resource, you rent it from a cloud provider, usually sharing the resources with other companies.

## Benefits of Cloud Computing

### Scalability
Since the `cloud provider is the owner of all the infrastructure & hardware`, you don't need to buy new resources in order to scale your solution up. The cloud provider is prepared for scaling your solution. By centralizing the ownership of hardware and hosting, the cloud providers need to buy tons of resources and, because of it, are able to get better deals. This means the cloud providers have lots of resources available to be used by their customers.
The scalability also works the other way around - `if you're not using your resource` as much as the hardware and infrastructure can provide, `you can scale your resources down`, removing unnecessary costs.

### OpEx instead of CapEx
The expenses for buying computing resources for hosting your computing solutions are considered as *Capital Expenditure* (*CapEx*), which means expenses related to acquiring equipment and infrastructure with the objective to improve the product, service or even the company premises. By using a cloud service, you can categorize this expense as a *Operational Expenditure* (*OpEx*), which translates to expenses a business incurs in its day to day operations, such as renting equipment or requiring a service from a third party. In terms of tax income, *OpEx* are usually better than *CapEx*, because the tax deduction is smaller. 

### Cost (usually better)
With a *pay-as-you-go* model (pay for the resources you are currently using), the hosting costs usually are better than if you had your own on-premises infrastructure. It also removes you the need for an upfront huge expense of buying the necessary hardware, e.g.: instead of spending thousands beforehand for buying the necessary servers and databases, you can simply use them at the cloud and pay as you use for really small prices, such as a few cents per GB per month.

## Cloud Models
### SAAS (Software-as-a-Service)
When a software is being provided as a service.
> Example: Office 365

You don't own the software nor the code. You use an already developed and published software. You use it
through the Internet, so you don't need to install it. You can't change or configure the software - you can only use what it is provided to you. You can't change the environment where this software is published as well.

### PAAS (Platform-as-a-Service)
When a platform is provided as a service.
> Example: SQL Server

The idea is to have a whole framework being provided as a service, where you can manage and configure it. You're not only using creating a document or asking for a calculation. Instead of using a fully developed solution (as in *SaaS*), you're using a platform that allows you to create your own customized applications.

### IAAS (Infrastructure-as-a-Service)
When the infrastructure is provided as a service.
> Example: Virtual Machines

Infrastructure, in this case, means compute resources. The IaaS provides you the necessary infrastructure without the need of you buying the correspondent hardware for it. You can define, for example, on which OS will your application run or what are the network rules within your environment. The whole environment is provided by virtualization technology - this means you can't control the physical domain (e.g.: routers, CPU, graphic disks, etc).

## Serverless
On the contrary of what the name indicates, the *Serverless* model still is a server based model. It's named like that because it's meant to be dynamic: in this model you have the least configuration needed. The model automatically knows when it's needed to scale up or down (different from the other models, where you have the responsibility of configuring it). This behavior has some cons, one of the most important being the cost effectiveness: if the heavy workload at a specific period of time is always expected, having the traditional servers can be more cost effective than having a serverless solution.

## Cloud Types
### Public cloud
A cloud that anyone can sign to and start using. You share the compute resources with other customers of the cloud provider.
> Example: you sign up for Microsoft Azure and deploy your application to their cloud; the machine that hosts your application also hosts other Microsoft customers' applications.

### Private cloud
A cloud where you're the compute resources that hosts your applications are totally owned by your company or at least only leased to your company.
> Example: you bought your own servers to host your applications or you lease a server to be used only by you in Azure, in other words, no other Microsoft customer has any application hosted in this server except you.

### Hybrid cloud
A combination of both clouds, where you can define a part of your compute resources to be private and use the other part in the public cloud.
> Example: you can have your own on-premises server that hosts your database (private cloud) and host your application on the Azure servers where other Microsoft clients also have applications being hosted (public cloud).

# Azure Architectural Components

## Regions
Regions are the way Microsoft Azure organize geographical locations in the world where their servers exist. There are currently over 60 regions.
You can deploy your resource in multiple regions to, for example, have a backup if a region goes down or to improve your resource usability.
> Example: if you only have customers in the US, you can use one of the US regions. If you also have customers in Spain, the Spanish customers that access your resource are going to have latency since the information needs to travel from US to Spain. It may be better to also deploy your resource in Europe as well, so the customers can get the resource from a closer place. If the European region goes down, the customers will still be able to access your resource from US, serving as a backup for them.

### Specific rules for regions
Some regions have their own restrictions, so you may not be allowed to deploy your application on every Azure region.
> Example: you can't deploy your resource to the Azure China region because they have their own restrictions - in order to do so, you need to have a specific agreement with the Chinese company that manages Azure China.
> Example 2: you can't deploy your resources to the governmental regions unless you're an employee of that governmental organization. If you are their employee, on the other hand, you can **only** have access to the governmental regions.

### Pairs
Each region has another region that is treated as its pair. This is done so you can deploy your resource in two regions in case of a backup is needed (e.g.: the resource in one region is down, so the resource in the second region can be served as a temporary backup for it).

It's almost always found in the same geographic place, but it may happen that there's no other region to be paired with, so it it's paired with some other region that it's may not be near the same geographic place. It can also happen that one region is a pair of one or more other regions.
> Example: two European regions are the *North Europe* and *West Europe*, and they're a pair
> Example 2: Brazil only has one region, *Brazil South*, so its pair is not located near Brazil but it's in US instead, the *South Central US*
> Example 3: both *East US 2* and *Brazil South* are paired with *South Central US*, but note that each combination is a separate pair - this means that *East US 2* is **not** paired with *Brazil South*, only with *South Central US*

### Availability Zones
A group of zones inside a region. Availability zones are usually located on the same property but different buildings, having their own power, heating & cooling systems and runs on their own network. Therefore, they are completely separated physically.

The logic behind availability zones is the same as the regions: they're made so you can have backups in case any availability zone goes down. If you don't choose an availability zone for your resource, Azure will choose one of them for you.
