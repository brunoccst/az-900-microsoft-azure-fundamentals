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
- SAAS (Software as a service) is when a software is being provided as a service,
usually with a signature involved, e.g.: Office 365. You don't own the software
nor the code. You use an already developed and published software. You use it
through the Internet, so you don't need to install it. You use it as a service.
You can't change or configurate the software - you can only use what it provides you.
You can't change the virtualized environment where this software is at as well.

- PAAS (Platform as a service) is when a platform is provided as a service.
A platform can also be a software, but you have a type of "environment" around it
which you can manipulate and manage.
It's not only creating a document or asking for a calculation.
You're managing the environment, making operations e.g. to make big calculations
across different documents. You still don't have the power to control the OS or
the virtualized environment where the platform is at.
E.g.: SQL Server

- IAAS (Infrastructure as a service) is when the infrastructure is provided as a service.
You can configurate the base of all your application. You can define its OS,
its firewall, etc. You can configure the virtual infrastructure where your 
softwares or platforms will be hosted at.
E.g.: Virtual Machines and Operational System.
You can't control the physical domain (e.g.: routers, CPU, graphic disks, etc).

- Serverless is still a server based model, but it's named that way because it's 
meant to be dynamic. You don't need to scale manually like on PAAS - the serverless
model will do that for you. You don't need to specify which model are you using,
which price plan you need, etc. The serverless model manages everything for you.

## Cloud Types
- Public cloud
A cloud that anyone can sign to and start using.
You share the resources with other customers of the cloud provider,
e.g.: the hardware hosting your cloud and another cloud is the same.

- Private cloud
The hardware is owned or leased by a single company, or at least only used by this company.

- Hybrid cloud
Combination of both clouds. You can configure only the infrastructure to the private cloud
and keep all the rest (apps, platforms, etc.) in the public cloud. 

## Azure Subscriptions
