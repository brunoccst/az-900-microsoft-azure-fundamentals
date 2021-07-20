# Microsoft Azure Fundamentals - AZ-900
This repository contains the results of **my** studies and understanding regarding the *[Exam AZ-900: Microsoft Azure Fundamentals](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900)*.

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
