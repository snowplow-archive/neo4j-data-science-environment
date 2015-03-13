# Neo4j Development environment

VM with complete Neo4j environment. Setup an Neo4j development environment without any faff.

## Quickstart

Assuming git, [Vagrant] [vagrant-install] and [VirtualBox] [virtualbox-install] installed:

```
 host$ git clone https://github.com/snowplow/neo4j-dev-environment.git
 host$ cd neo4j-dev-environment
 host$ vagrant up
```

This will launch a VM, install on it [Neo4j][neo4j], and start Neo4j. You then simply navigate your host's browser to:

```
http://localhost:7474
```

[vagrant-install]: http://docs.vagrantup.com/v2/installation/index.html
[virtualbox-install]: https://www.virtualbox.org/wiki/Downloads
[neo4j]: http://neo4j.com/
