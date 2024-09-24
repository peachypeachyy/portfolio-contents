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

- Setup different components of Architecture:
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/e-commerce_platform/supporting_assets/wo-2.png)
- Setup Workflow for CI/CD to facilitate builds for the application.
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/e-commerce_platform/supporting_assets/wo-1.png)
- Setup the Data pipelines to gain granular data insights.
    ![My Image](https://github.com/peachypeachyy/portfolio-contents/blob/main/e-commerce_platform/supporting_assets/wo-3.png)


## Impact

- Platform handles roughly 1 million requests per day.
- CI/CD pipeline delivers consistent secure deployments into production.
- Data Pipelines gives granular insights into metrics such as Time Spent on page or sales metrics such as MRR.


