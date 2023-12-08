### Asynchronous Communication - Decoupled
![[Pasted image 20231204110430.png]]

### Pub/Sub
- Reliable, scalable, fully-managed asynchronous
- Backbone for High Available and High Scalable
	- low cost
- Use cases
	- Event ingestion
	- Delivery for streaming analytics pipelines
- Support both push and pull messages

#### How doe it work?
![[Pasted image 20231204110640.png]]

- **Publisher** - Sender of a message
- **Subscriber** - Receiver of the message
	- Pull - Subscriber pulls messages when ready
	- Push - Messages are sent to subscribers
- **Very Flexible** Publisher and Subscriber Relationships

### Getting Ready with Topic and Subscriptions

Step 1 - Topic is created
Step 2 - Subscriptions are created

### Sending and Receiving a Message
- Publisher sends a message to Topic
- Message individually delivered to each and every subscription
- Subscribers send acknowledgement
- Messages are removed from subscriptions message queue

### Managing Pub/Sub
```shell
gcloud pubsub topics create TOPIC_NAME

gcloud pubsub subscriptions create SUBSCRIPTION_NAME

gcloud pubsub subscriptions pull SUBSCRIPTION_NAME

gcloud pubsub topics publish TOPIC_NAME --message="MESSAGE" --auto-ack

gcloud pubsub topics list

gcloud pubsub topics list-subscriptions TOPIC_NAME
```