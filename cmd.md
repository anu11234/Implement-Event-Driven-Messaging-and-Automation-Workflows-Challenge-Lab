# Implement Event-Driven Messaging and Automation Workflows: Challenge Lab || **ARC113**

**Command:**

```bash
# Task 1: Create subscription 'pubsub-subscription-message' and publish 'Hello World'
gcloud pubsub subscriptions create pubsub-subscription-message --topic=gcloud-pubsub-topic
gcloud pubsub topics publish gcloud-pubsub-topic --message="Hello World"

# Task 2: Pull the message to verify
gcloud pubsub subscriptions pull pubsub-subscription-message --limit 5 --auto-ack

# Task 3: Create the snapshot 'pubsub-snapshot' from 'gcloud-pubsub-subscription'
gcloud pubsub snapshots create pubsub-snapshot --subscription=gcloud-pubsub-subscription
