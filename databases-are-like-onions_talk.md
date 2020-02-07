https://vimeo.com/289664676

#### Statement
The least bad way to integrate microservices is the event way.

## Events
A combination of:
- Notification
- State transfer
- Immutable

Kafka is the best event queue system.

Integrating by events facilitate a micro service ecosystem. In contrast to a RPC hierarchical service structure.

## Kafka
A streaming platform

At the heart of the system is the **event log**.

**Scaling**
- Shard data to get scalability
- Consumer groups (important)

Services interact with Kafka as a Producer or a Consumer. All other abstractions are built on Producer or Consumer APIs.


### Consumers
Consumers have a position*(in reading the log)* of their own. Consuming the message doesn't *consume* the message. Events can be stored indefinitely.

- Only have sequential access(in Kafka)


### Topics

**Single topic**
- Many producers
- Many consumers
- Many Broker machines
- NO BOTTLENECK!

### Connectors
Kafka comes with libraries for connecting Kafka to other data stores.

### Streaming
KSQL: An engine for continuous computation.

Kafka Streams: A Java API for the same

### Schema Management
- Schema registry

### Databases
At the centre of every database/database model there is a commit log. A database builds a materialized view of the log(tables, graphs, documents).

#### When you are build microservices
You are building a inside-out database