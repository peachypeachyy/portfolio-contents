# Consolidation of IT assets and Automating from Single Platform.

## Description
Owing to increasing number of IT assets for a Major Oil and Gas Client, there was a need to consolidate and Automate IT tasks from a single pane of glass.

## Challenges / Pain Points

- Growing number of IT assets
- No central source of truth to manage the lifecycle of assets
- Increasing manual efforts for routine IT tasks performed by different teams in silo's.

## Existing Setup
- Heterogenous Scripts in different languages to automate certain tasks.

## Solution Approach

- Consolidation of IT assets under a single platform to manage their lifecycle
- Automate routine tasks to improve IT productivity
- Deliver consistent and reliable state of the IT infrastructure

## Steps Taken

1. Convert Heterogenous scripts to Ansible YAML
    1. First step of transition is to convert the Different scripts such as Bash scripts, Powershell scripts, Perl scripts to Ansible YAML.
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/consolidation_IT_automation/supporting_assets/BP-1.png)
2. Setup Ansible Automation Platform with Active-Passive mode capable to handle disaster recovery situations
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/consolidation_IT_automation/supporting_assets/BP-2.png)
3. Make Infrastructure Changes to Support the Ansible communication over SSH.
    1. Make changes to Network and Storage, setup Network links, open WAF ports and configure SAN Storage Zoning
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/consolidation_IT_automation/supporting_assets/BP-3.png)

## Impact

- Centralized Manageability and Observability.
- Automated most L1-L2 Tasks, reduced time to patch and manage IT environment, improved IT productivity by 40%.
- Provided Consistent and repeatable state of infrastructure with Audit logs.



