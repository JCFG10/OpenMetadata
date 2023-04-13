---
title: createTopic
slug: /main-concepts/metadata-standard/schemas/api/data/createtopic
---

# CreateTopicRequest

*Create a topic entity request*

## Properties

- **`name`**: Name that identifies this topic instance uniquely. Refer to *../../type/basic.json#/definitions/entityName*.
- **`displayName`** *(string)*: Display Name that identifies this topic.
- **`description`**: Description of the topic instance. What it has and how to use it. Refer to *../../type/basic.json#/definitions/markdown*.
- **`service`**: Fully qualified name of the messaging service where this topic is hosted in. Refer to *../../type/basic.json#/definitions/fullyQualifiedEntityName*.
- **`messageSchema`**: Refer to *../../type/schema.json*.
- **`partitions`** *(integer)*: Number of partitions into which the topic is divided. Minimum: `1`.
- **`cleanupPolicies`** *(array)*: Topic clean up policy. For Kafka - `cleanup.policy` configuration.
  - **Items**: Refer to *../../entity/data/topic.json#/definitions/cleanupPolicy*.
- **`replicationFactor`** *(integer)*: Replication Factor in integer (more than 1).
- **`retentionTime`** *(number)*: Retention time in milliseconds. For Kafka - `retention.ms` configuration.
- **`maximumMessageSize`** *(integer)*: Maximum message size in bytes. For Kafka - `max.message.bytes` configuration.
- **`minimumInSyncReplicas`** *(integer)*: Minimum number replicas in sync to control durability. For Kafka - `min.insync.replicas` configuration.
- **`retentionSize`** *(number)*: Maximum size of a partition in bytes before old data is discarded. For Kafka - `retention.bytes` configuration. Default: `-1`.
- **`topicConfig`**: Contains key/value pair of topic configuration. Refer to *../../entity/data/topic.json#/definitions/topicConfig*.
- **`owner`**: Owner of this topic. Refer to *../../type/entityReference.json*.
- **`tags`** *(array)*: Tags for this topic. Default: `None`.
  - **Items**: Refer to *../../type/tagLabel.json*.
- **`extension`**: Entity extension data with custom attributes added to the entity. Refer to *../../type/basic.json#/definitions/entityExtension*.


Documentation file automatically generated at 2023-04-13 23:17:03.893190.
