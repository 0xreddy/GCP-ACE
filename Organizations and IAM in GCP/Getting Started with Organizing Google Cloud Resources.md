### Resources Hierarchy
- **Resources** are created in projects
- A **Folder** can contain multiple projects
- **Organization** can contain multiple folders
![[Pasted image 20231207113256.png]]
#### Recommendations for Enterprises
- Create separate projects for different environments
	- Complete isolation between test and production environments
- Create separate folders for each department
	- Isolation production applications of one department from another
	- Can create shared folders for shared resources
- One project per application per environment

### Billing Accounts
- Billing Account is mandatory for creating resources in a project
- Associated with on or more projects
- Can have multiple billing accounts in an Organization
- Create Billing Accounts representing your organization structure
- Two Types:
	- Self Serve - Billed directly to Credit Card or Bank Account
	- Invoiced - Generate invoices

#### Managing Billing - Budget, Alerts and Exports
- Setup a Cloud Billing Budget to avoid surprises
	- Configure Alerts
- Billing data can be exported
	- Big Query(for information and visualization)
	- Cloud Storage(for history/archiving)

### IAM Best Practices
- **Principle of Least Privilege** - Give least possible privilege needed for a role
	- Basic Roles are Not recommended
	- Use Service Accounts with minimum privileges
- **Separation of Duties** - Involve at least 2 people in sensitive task
- **Constant Monitoring** - Review Cloud Audit Logs to audit changes to IAM policies and access to Service Account keys
- Use Groups when possible
	- Makes it easy to manage users and permissions

### User Identity Management in Google Cloud
- **Super Admin** => Email used to create Gcloud Account
	- Access to everything
- However not recommended for enterprises
- **OPTION 1** - Your Enterprise is using Google Workspace
- **OPTION 2** - Your Enterprise uses an Identity Provider of its own
	- Federate Google Cloud with your Identity Provider

#### Corporate Directory Federation
- Federate Cloud Identity or Google Workspace with your external identity provider such as Active Directory or Azure AD
- Enable Single Sign On
	- Users are redirected to an external Idp to authenticate
	- When users are authenticated, SAML assertion is sent to Google Sign-In

### IAM Members/Identities
- **Google Account** - Represent a person (an email address)
- **Service Account** - Represents an application account (Not person)
- **Google group** - Collection - Google & Service Accounts
	- Has an unique email address
	- Helps to apply access policy to a group
- **Google Workspace domain** - Google Workspace provides collaboration services for enterprises
	- Tools like Gmail, Calendar, Meet, Chat, Drive, Docs etc are included
- **Cloud Identity domain** - Cloud Identity is an Identity as a Service (IDaaS) solution that centrally manages users and groups

#### Use Cases

![[Pasted image 20231207115846.png]]

### Organization Policy Service
- To have centralized constraints on all resources created in an Organization
	- Configure Organization Policy
	- Disable creation of Service Accounts
	- Allow/Deny creation of resources in specific regions
- Needs a Role - Organization Policy Administrator
- IAM focuses on **Who**
- Organization policy focuses on **What**

### Resource Hierarchy & IAM Policy

![[Pasted image 20231207120521.png]]

- IAM Policy can be set at any level of the hierarchy
- Resources inherit the policies of All parents
- The effective policy for a resource is the union of the policy on that resource and its parents
- Policy inheritance is transitive
- You can't restrict policy at lower level if permission is given at an higher level

[[Organizations and IAM in GCP/Exploring IAM Predefined Roles]]
