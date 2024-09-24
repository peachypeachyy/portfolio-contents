# Brownfield augmentation of an Insurance Pricing system.

## Description

Rearchitecting a Brownfield deployment of an Insurance Client based on requirements. Client uses BRMS system to compute insurance pricing. A inhouse business team configures appropriate rules in excel and uploads to BRMS system which is then picked up by the Quotation engine for pricing.

## Pain Points / Challenges

- Scalability: Due to recent regulation change, anticipated traffic to the servers performing pricing were to increase by 4-5 times.
- Performance: Resource contention due to growth of system, latency observed for a round trip request.
- Manageability: Duplicate entries in excel while uploading in BRMS.

## Existing Setup

Following was the original setup (Baseline state)

![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/BRMS_Augmentation/supporting_assets/Lib-1.png)

Following is the step-by-step approach taken to address challenges

## Solution Approach:

- Bring Webservices and Rules engine closer together on the same node enabling faster rules based calculations
- Decompose application into smaller modules to scale and manage better.
- Bring in CI checks to ensure validity of excel before being fed into BRMS

## Steps:

1. Refactor webservices and BRMS to deploy as side-by-side containers
    1. Breakdown existing web services code from a giant single project structure to multiple projects
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/BRMS_Augmentation/supporting_assets/Lib-2.png)
    2. Deploy Red Hat Decision Manager as containers
    3. Create docker files for web-services
    4. Create daemonsets to have deployment of decision manager and web-services on single node.
2. Create the Target Setup
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/BRMS_Augmentation/supporting_assets/Lib-3.png)
    1. Setup nexus repository
    2. Configure webhooks and CI process:
    3. Setup the Openshift environment and load the files created in previous step
    4. Setup Redis Cache, request re-read from web-services when page fault occurs.
3. Perform Blue-Green Migration from existing setup to target setup
    1. Copy sanitized existing content into target nexus repository
    2. Slowly divert network traffic to new setup and observe pricing

## Impact
- Independent scaling based on products made the system more modular, containerization facilitated accomodation of higher traffic.
- Round trip of request accomodated under 1 second.
- No more duplicate entries in the excel sheets.


