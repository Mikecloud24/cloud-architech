# Steps for User Synchronization from ADDS Microsoft Entra ID using Entra Connect tool

	1) On-Prem: To carry out the migration and synch users successfully, I spun up a VM and installed an ADDS Role...

		a. Create a VM        - Windows Server 2019
			i. Resource Group - ADVM-RG  # Resource Group that holds all related resources
			ii. VM Name       - ADVM     # provide a name for your VM
			iii. Image        - Windows Server 2019
			iv. Size          - D2sV3    # Base on requirements
			v. VM Creds:      - ""       # provide username and password
			vi. Review and Create

		b. Login and Install ADDS Role on the VM, then perform steps b - h
			i. Server Manager -> Add Roles and Features 
			ii. Server Roles -> Active Directory Domain services

		c. Configure ADDS Role - Local Domain Name - using a dcpromo
			i. New Forest
			ii. Domain Name  - mikecloud24.com  # example
			iii. Password    -""

		d. Create Users/Groups/Organizational Units: steps...

			i. Server Manager - > Tools -> Create Users and Computers
			ii. Create Users and Computers -> Users -> New -> User
			iii. User Name and Password
			iv. User Cannot change the Password, Password Never Expires
			v. Add Users to the Group 

		e. Create synchronization Users
			i. ADDS - adsyncuser - add to Enterprise Admins Group

		f. Download Microsoft Entra Connect Tool
		g. Download and Install Entra Connect Health Tool - P2 License

		h. Configure Entra Connect 
			i. Password Hash Sync/Passthrough Auth/ADFS
			ii. Filter Org Units, Group
			iii. Provide 2 Credentials
				1) Entra Id Credential - entrasyncuser 
				2) ADDS Credential - adsyncuser 
		iv. Initiate the Synchronization process
			
	2) Microsoft Entra: cloud
		a. Microsoft Entra ID - entrasyncuser - Global Admin privilege - Domain
			entrasyncuser@mikecloud24.onmicrosoft.com      
			P/w
			
		b. Synchronized Users/ Groups
		c. Additional Users and Groups

