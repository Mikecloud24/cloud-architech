# Designing Azure Infra Solutions

	- Architecting
		○ Architects Role:
		- 1) Solution Provider 
        - 2) Diagnosis

		○ Customer Requirements: 
			- IaaS + PaaS + SaaS
			- (FR + NFRs) Functional Requirements + Non-Functional Requirements
			- FRs
				□ UI/UX
				□ Interactions
				□ Services
				□ Business Functionality
				□ Use Cases

			- NFRs [Assumption/Obvious] <==== Cost
				□ *Abilities:
					® Scalability
					® Reliability 
					® Security
					® Accessibility
					® Manageability
					® Observability
					® Reusability

	- Architect Types:
		○ Technical Architect
		○ Solution Architect
		○ Enterprise Architect

	- Azure and AWS Proficiency
		○ CAF - Cloud Adoption Framework
		○ Well formedness Principles


# Resource Group and Tagging for effective management and cost tracking
- Example:
- Server Mgnt Team  - ServerRG/ComputeRG
- Data Mgnt Team    - DataRG
- Security Team     - SecteamRG

# Tagging:
	- Client Name:  "" 
	- Env Name:     DevTest, Staging, Prod etc
	- Project Name: ""
	- Dept Name:    Sales, Mkt, Finance