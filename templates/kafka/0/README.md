# Apache Kafka

Ran as global scale, this stack creates Kafka nodes on each host having the specified host labels.

## Configuration

Each node is automatically configured to advertise its host hostname, which will be written into given Zookeeper path.
The broker id of each instance is defined using a host label: _instore.digital.kafka.brokerid_

Labels on correctly configured Kafka hosts:
```
instore.digital.kafka.enable=true
instore.digital.kafka.brokerid=1
```
```
instore.digital.kafka.enable=true
instore.digital.kafka.brokerid=2
```
```
instore.digital.kafka.enable=true
instore.digital.kafka.brokerid=3
```

Default configuration options set:
```
controlled.shutdown.enable=true
auto.leader.rebalance.enable=true
auto.create.topics.enable=false
default.replication.factor=1
delete.topic.enable=true
zookeeper.connection.timeout.ms=10000
zookeeper.session.timeout.ms=10000
```

## Networking

Each container on each host runs with host's network. Thus, only one instance of Kafka can run on a given host.