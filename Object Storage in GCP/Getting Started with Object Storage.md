- Most popular, very flexible & inexpensive storage service
- Store large objects using a key-value approach
	- Treats entire object as an unit, also called Object storage
- Provides REST API to access and modify objects
- Store all file types
- Bucket names are globally unique
	- 3-63 characters
	- can't start with 'goog' prefix
- Max object size is 5TB

#### Storage Class
![[Pasted image 20231111185307.png]]

#### Uploading and Downloading Objects
![[Pasted image 20231111185739.png]]

#### Object Versioning
- Prevents accidental deletion & provide history
	- Enabled at bucket level
	- Live version is the latest version
		- If delete live object, it becomes non current object version
		- If delete nun current object version, it is deleted
	- Older versions are uniquely identified
	- Reduced costs by deleting older ones

#### Object Lifecycle Management
- Files are frequently accessed when they are created
- Identify objects using conditions based on
	- Age, CreatedBefore. IsLive, MatchesStorageClass, NumberOfNewerVersions, etc.
- Two kind of actions:
	- SetStorageClass actions - change from one storage class to another
	- Deletion actions - delete objects
- Allowed Transitions:
- (Standard or Multi-Regional or Regional) to (Nearline or Coldline or Archive)
- Nearline to (Coldline or Archive)
- Coldline to Archive

```shell
gsutil [mb | ls | cp | mv | rewrite] gs://BUCKET_NAME

gsutil versioning set on/off gs://BUCKET_NAME
gsutil uniformbucketlevelaccess set on/off gs://BUCKET_NAME
gsutil acl ch [-u | -g | -p]
gsutil iam ch
```