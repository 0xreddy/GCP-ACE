- Used to execute some code when an event happens
- Run code in response to events
	- Don't worry about scaling or servers or availability
- Pay only for what you use
	- Number of invocations
	- Compute time of the invocations
	- Memory and CPU provisioned
- Time Bound - Default 1 min and MAX 60 min
- Two versions:
	- 1st version
	- 2nd version: New version built on top of Cloud Run and Eventarc

#### **Concepts**
- Event
- Trigger
	- Trigger - The function the trigger is going to trigger
	- Functions - Action to perform after trigger
- Events triggered from 
	- Cloud Storage
	- Cloud Pub/Sub
	- HTTP/REST API
	- Firebase
	- Cloud Firestore
	- Stack driver logging

[[Google Cloud Functions/GEN 2]]