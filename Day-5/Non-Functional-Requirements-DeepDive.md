# Non-Functional Requirement

1. Monitoring
	- Observability
	- Telemetry 
	- Diagnostics
	- Instrumentation 

2. Resource Utilization
- ROI - Return on Investment
- Performance
- Security
…

# Activity Logs
- Log Analytics Workspace
- Storage Accounts - Append Logs

# Infra Resources - VM Insights
	- VM Host Logs
	- Guest OS Logs
1. PaaS resources - AKS, Storage Account, App Insights
	- Diagnostics Logs

2. NFR
	- Reliability
	- High Availability
	- E.T.C ...
	
3. VM Image  - IIS Setup/Web Application
	-) Availability Set (Multiple Instances) + Regional LB (Azure LB)

4. Install-WindowsFeature -Name Web-Server -IncludeManagementTools

	-) Availability Zone + Regional LB (Azure LB)
	-) Traffic Manager + 2 Deployments [Across Regions - VMs]
	-) Front Door + 2 Deployment [Across Regions - App Service Plans]
		a. App Service Plan/s - East US, South East Asia
		b. App Service - Respective App Service Plan
		c. App Service Plan - Auto scale Settings
		d. Front Door Service
