# Couchbase Community

Ran as global scale, this stack creates Couchbase nodes on each host having the specified host labels.

### Bootstrap

When running one or multiple Couchbase node(s), you must access the web interface to initialize the cluster, and link node to each others manually.

### Data persistence

Persistent data will be stored in data directory, which is mapped to specified host directory.

### Networking

Each container on each host runs with host's network. Thus, only one instance of Couchbase can run on a given host.