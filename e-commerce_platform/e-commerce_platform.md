## Description

Client acquired a basic ruby on rails application from another vendor. The need was to setup a fault tolerant, highly available and scalable platform to accomodate load from millions of site visitors and customers.


## Pain-Points / Challenges

- Scalability: Need a solution which can meet high traffic demand.
- Uptime of website should be minimum of 99.95%
- Automated builds with modern DevOps practices.
- Have a clear Visibility on User interactions and Performance metrics.


## Existing Setup

- Ruby on Rails MVC application was pre-written by an agency.
- Greenfield deployment, all newly setup for a new business.


## Solution Approach

- Deployment of scalable platform on AWS
- Setup CI/CD to install and run the application on AWS
- Setup the Data Pipeline enabling analytics for User Interactions and Performance Metrics.

## Steps

1. Setup different components of Architecture:
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/e-commerce_platform/supporting_assets/wo-2.png)
    1. Setup the EKS Nodes in the public subnet.
    2. Setup the Cache and ElasticSearch in the public subnet.
    3. Setup Static assets of the website into S3 Bucket and cloudfront to deliver static assets.
    4. Setup the Database in private subnet, configure VPC peering and security groups.
    5. Setup DNS for website within cloudflare, configure Bot protection levels and IP access rules.
    6. Configure Load balancer.
    7. Create Kubernetes Manifest files.
2. Setup Workflow for CI/CD to facilitate builds for the application.
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/e-commerce_platform/supporting_assets/wo-1.png)
    1. Create the config file defining workflows pertaining to application code and kubernetes manifest files.
    2. Grant access to CircleCI from AWS to deploy infrastructure on AWS.
3. Setup the Data pipelines to gain granular data insights.
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/e-commerce_platform/supporting_assets/wo-3.png)
    1. Setup required permissions to pull data from RDS.
    2. Write Glue scripts to transform data and load into S3.
    3. Visualize on Quicksight.


## Impact

- Platform handles roughly 1 million requests per day.
- CI/CD pipeline delivers consistent secure deployments into production.
- Data Pipelines gives granular insights into metrics such as Time Spent on page or sales metrics such as MRR.


