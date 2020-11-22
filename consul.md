Get registered services
```
http://localhost:8500/v1/catalog/service/microservice-name
```

Healthcheks
```
http://localhost:8500/v1/health/checks/microservice-name
```

Deregister service
```
curl -X PUT http://localhost:8500/v1/agent/service/deregister/microservice-name-8080-039b03582fa2685e95ce0f71c8c21ed1
```