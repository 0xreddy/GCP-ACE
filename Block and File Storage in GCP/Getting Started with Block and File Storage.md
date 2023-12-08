### Difference between Block and File Storage
#### Block Storage
- Hard disk attached to computer
- Used as
	- Direct attached storage (DAS)
	- Storage Area Network (SAN)
- Persistent Disks: Network Block Storage
	- Optional
		- Zonal
		- Regional
	- More durable
	- Lifecycle not tied to instance
	- Very flexible
		- Increase size whenever
		- Performance scales with size
- Local SSDs
	- Local Block Storage
		- Physically attached to the host
		- Used to hold temporary
		- Lifecycle tied to VM instance
		- Provide very high IOPS and very low latency
		- Data automatically encrypted
		- Support SCSI and NVMe interfaces
	- Choose NVMe and multi-queue SCSI images for best performance
	- Larger Local SSDs, more vCPUs => Even better performance

![[Pasted image 20231109233429.png]]

#### Persistent Disks - Standard vs Balanced vs SSD
![[Pasted image 20231109233643.png]]

#### Persistent Disks - Snapshots
- Can Schedule snapshots
- Can be multi-regional and regional
- Share snapshots across projects
- Can create new disks and instances from snapshots
- They are incremental
	- Deletes data which is not needed by snapshots
- Keep similar data together
- Avoid taking snapshots more often than once an hour
- Schedule snapshots during off-peak hours

#### Playing with Machine Images
- Machine Image is different from Image
- An image is created from the boot Persistent Disk
- Machine Image is created from a VM instance
- Recommended for disks backup, instance cloning and replication

![[Pasted image 20231111124057.png]]

```shell
gcloud compute disks [list | create | delete | resize | snapshot]
```

```shell
gcloud compute images [list | create | delete | deprecate | describe | export | import | update]
```

### Scenarios

![[Pasted image 20231111125707.png]]

#### File Storage
- Media workflows need huge shared storage for supporting processes
	- Filestore: High performance file storage

#### Cloud Filestore
- Shared file storage
	- Supports NFSv3
- Suitable for high performance
- Support HDD and SSD
- Use case: File share, media workflows and content

![[Pasted image 20231111131832.png]]

