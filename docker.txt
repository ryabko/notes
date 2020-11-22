Hostname to access the host from the container on MacOS
```
host.docker.internal
```

Rebuild service from docker compose
```
docker-compose --project-name projectname --file docker-compose.yml up -d --no-deps --build service-name
```

Recreate the service
```
docker-compose up --force-recreate --no-deps service-name
docker-compose up --force-recreate
```