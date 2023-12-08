- There are identities that need to access those resources and perform actions
- GCP Cloud Identity and Access Management (IAM)
	- Authentication
	- Authorization
- Identities can be
	- GCP User
	- Group of GCP users
	- Application running in GCP
	- Application running in your data center
	- Unauthenticated users
- Provides very granular control
	- Limit a single user
		- to perform single action 
		- on a specific cloud resource
		- from a specific cloud resource
		- during a specific time window
- Important Generic Concepts
	- Member
	- Resource
	- Action
- In Google Cloud IAM:
	- Roles - A set of permissions
		- Do not know about members
	- Policy - Used to assign a role to a member

**Step 1:** Choose a role with right permissions
**Step 2:** Create Policy binding member with role (Mapping roles)

> [!NOTE]
> IAM in AWS is very different from GCP.

##### Three types of roles:
- Basic Roles
	- Viewer - Read only
	- Editor - Viewer + Edit actions
	- Owner - Editor + Manage Roles and Permissions + Billing
- Predefined Roles - Fine grained roles predefined and managed by Google
- Custom roles - When predefined roles are not sufficient, you can create your own custom roles

#### IAM Policy
- Roles are assigned to users through IAM Policy documents
- Represented by a policy object
- Member type is identified by prefix
	- E.g. user, service account, group or domain

```shell
gcloud auth auth login
gcloud auth revoke
gcloud auth list
```

```shell
gcloud projects [get-iam-policy | add-iam-policy-binding --member=user@gmail.com --role=roles/ROLE_NAME | set-iam-policy | remove-iam-policy-binding | ] PROJECT-ID
```

```shell
gcloud iam roles [describe | create | copy --source SOURCE --destination DESTINATION --dest-project=PROJECT_NAME] roles/ROLE_NAME
```

#### Service Accounts
- Scenario: An application on a VM needs access to cloud storage (You don't want to use personal credentials to allow access)
- Service accounts help in solving the problem
- No password associated
	- Has private/public RSA key-pairs
	- Can't login via browsers or cookies
- Types
	- Default service account
	- User managed service account (fine grained access control)
	- Google-managed service account
		- Used by GCP to perform operations on user's behalf

```shell
gcloud iam service-accounts keys create
```

![[Pasted image 20231119200818.png]]

#### ACL
- Define who has access to your buckets and objects, as well as what level of access they have

> [!Remember]
> - Use IAM for common permissions to all objects in a bucket.
> - Use ACLs if you need to customize access to individual objects.

- Two types
	- Uniform - When all users should have same access
	- Fine-grained - When multiple users should have different access level

#### Signed URL
- A URL that gives permissions for limited time duration to perform specific actions
```shell
gsutil signurl
```

