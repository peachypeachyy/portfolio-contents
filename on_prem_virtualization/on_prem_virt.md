# On-Prem Virtualization Architecture.

## Description :

The aim of this architecture is to create a DC-DR based on prem architecture which can run both Virtualized and Containerized workloads 

![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/on_prem_virtualization/supporting_assets/Onprem%20arch.png)

## Technologies Used :
    - Red Hat Openshift
    - Red Hat 3scale API Management
    - Red Hat JBoss Enterprise Application Platform.
    - Microsoft AD
    - Red Hat Directory servers
    - Red Hat Enterprise Linux
    - VMWare VSphere-7
    - HPE Proliant Servers

## Objective :

In this architecture, the business requirement was to develop a multi-tenancy solution for the client to expose it's billing software to different external customers. Openshift, an enterprise grade kubernetes application platform was used on AWS in this case to host a containerized process automation manager(PAM) application within pods managed through the Red Hat Operators on Red Hat Openshift.

The overall architecture uses 3 layers of abstraction with different namespaces for the Application workload(PAM), the API Management layer and the bespoke developed frontend dashboard.

As a Solutions Architect, my work involved devising this Green-field architecture, integrating & Securing the API's with the API management solution, understanding and designing the business processess which needed to be automated using low-code/no-code on the Process Automation Manager(PAM) deployed on Openshift 



## Work Performed

As a Solutions Architect, the work performed by me in detail is as follows :

    - Designed policies to Secure API's on the 3Scale API Management Layer
    - Setup Rate limiting rules for API's which were publicly exposed.
    - Devised pricing rules for API's which were monetized
    - Created the blueprint for re-usable connectors using Red Hat Fuse
    - Setup the Design for Openshift pods, nodes and namespaces
    - Designed the CI/CD Pipelines and overview of the workflows using Tekton
    - Configured the logging and monitoring on Prometheus and Grafana within Openshift for the application workloads. 

## Impact:

    - The Client was able to achieve near 100% uptime by distributing the workload across multiple pods. They were able to reduce costs by 15% in 6 months and release features faster by over 25% with the help of re-usable connectors in code and an Integrated CI/CD workflow.
    - Using openshift they had granular observability and were able to make changes in the deployment swiftly and securely using an integrated CI/CD pipeline.
    - A single pane of glass for the performance of the application workloads from Prometheus and Grafana helped IT stakeholders maintain control while having a holistic picture of the environment.
    - The Client was able to monitor and monetize the API's, observe fluctuations or anomalies and take remediary actions from the API Management plane.