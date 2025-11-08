# Write-up Template

## My Analysis

### Cost Analysis
* **Azure VM**: Higher upfront cost, instances running 24/7. Additional cost of manual staff hired for VM management such as setup, patching, scaling and monitoring.
* **App SErvices**: Lower as compared to Azure VMs, cost scales with actual usage and traffic


### Scalability Analysis
* **Azure VM**:Headache of manual scaling. Autoscaling option is there, but lot of configurations are required. manual Scaling speed is always slow 
* **App SErvices**: Built in and rapid auto scaling based on Price Plan 


### Availability Analysis
* **Azure VM**: Due to manual scaling, there might be cases of downtime. Like in peak traffic, scaling took time. Manual updates, patches, monitoring is required
* **App SErvices**: Automated patching, updates, failovers, redundancy are there in App Services.

As per google,
99.95% for apps running in paid App Service plans (Basic or higher).
99.99% for zone-redundant App Service plans.


### Workflow Analysis
* **Azure VM**: Manual server setup, manual nginx setup, manual network setups, manual dependency installations, manual CICD setup, manual file transfers, then execution of custom scripts
* **App SErvices**: Integration with Github, bitbucket and gitlab. Automated deployments with git push. Automatic CICD eg. With Github-Actions, changes are deployed on the commit to main branch


## I chose Azure App Services. Why ?

For the application like CMS, where we have native support for python in App Services, it provides Automatic CICD process, automatic running python setup scripts, installing dependencies. 

Unlike Azure VMs, I dont need to setup Server like nginx configurations, uploading files manually using SCP, intalling python dependencies manually. 

Upfront cost and Time-To-Market for projects like CMS is very good in Azure App Services.



### Assess app changes that would change your decision.

* In case of high traffic, with higher CPU usage, VMs are more cost effective 
* If we want control on server level, like custom kernel modifications etc. 
* In case of ultra low latency, we might need to shift to VM 
* Because server level control is there on VMs