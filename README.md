Cockroach
==========

A Scalable, Geo-Replicated, Transactional Datastore

Cockroach is a distributed key:value which supports ACID
transactional semantics and versioned values as first-class
features. The primary design goal is global consistency and 
survivability, hence the name. Cockroach aims to toerate disk,
machine, rack or even datacenter failure with minimal latency
disruption and no manual intervention. Cockroach nodes are symmetric;
a design goal is one binary with minimal configuration and no required
auxiliary services

Cockroach implements a single, monolithic sorted map from key to value
where both keys and values are byte strings (not unicode). Cockroach 
scales linearly (theoritically up to 4 exabytes (4E) of logical data).
The map is composed of one or more ranges and each range is backed by data stored in leveldb and replicated to up to a tota of three or more cockroach servers. 