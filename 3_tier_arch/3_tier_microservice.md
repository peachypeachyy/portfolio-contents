# Three Tiered Microservices Architecture.

## Description :

The aim of this architecture is to create a distributed microservice based architecture with a segregated frontend connected with a central API management layer. This allows the API's to be secured, rate limited in case of sudden spikes of traffic, authenticated and authorized from a central command plane and enables the system to monetize any external APIs if required.

![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/3_tier_arch/supporting_assets/3%20Tier%20Arch.jpg)

## Objective :

In this architecture, the business requirement was to develop a multi-tenancy solution for the client, Openshift was used on AWS in this case to host a process automation manager(PAM) application within pods managed through the Red Hat Operators on Red Hat Openshift.
The overall architecture uses 3 layers of abstraction with different namespaces for the Application workload(PAM), the API Management layer and the bespoke developed frontend dashboard monitoring usage


There are several components to this architecture

# Tenant Dashboards

# API Management

# OCP-Kubernetes Multi-tenant workloads

## Impact:

The Client was able to achieve near 100% uptime by distributing the workload across multiple pods. Using openshift they had granular observability and were able to make changes in the deployment swiftly and securely using integrated CI-CD pipelining. A single pane of glass across the PAM workloads, API Management and frontends helped IT stakeholders maintain control while having a holistic picture of the environment.  


