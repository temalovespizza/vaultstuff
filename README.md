# VAULT docker stuff

## pgsql stuff

```bash
cd psqlvault
docker-compose up -d
docker-compose down
```

- node1 http://172.26.26.6:8200
- node2 http://172.26.26.7:8200
- node3 http://172.26.26.8:8200
- balancer http://172.26.26.9:8080

## consul stuff

```bash
cd consulvault
docker-compose up -d
docker-compose down
```

CONSUL CLUSTER ACCESS

- http://127.0.0.1:8500/ui/dc1/nodes

VAULT NODES
- http://172.26.26.101:8200
- http://172.26.26.102:8200

FOR CONSUL DNS LOAD BALANCING SET DNS IN RESOLV.CONF TO:

```
nameserver 172.26.26.198
nameserver 172.26.26.199
```

AND USE THIS URL TO ACCESS VAULT
http://vault.service.dc1.consul:8200
