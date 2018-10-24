# Unbound
This image is a Unbound server configured for DNS over TLS (DoT) to hide or circumvent DNS manipulation, tracking or blockage.

## Usage
Download docker-compose.yml & unbound.conf, tweak unbound.conf to your needs and then start the server.

### Download
```
curl -LJO https://raw.githubusercontent.com/JJTC-Docker/unbound/master/docker-compose.yml
curl -LJO https://raw.githubusercontent.com/JJTC-Docker/unbound/master/unbound.conf
```
### Pull and Up
```
docker-compose pull
docker-compose up -d
```

## Diagnostics
Change the verbosity level (1-4) and restart the service `docker-compose restart` to validate that Unbound is working.

It is possible to attach to the service and see Unbound in action with `docker-compose up`.