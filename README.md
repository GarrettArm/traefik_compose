# Connecting a traefik to docker-composes in separate folders

Following tutorial at https://github.com/DoTheEvo/Traefik-v2-examples

The author recommends Caddy as an alternative, so consider it.

## Set up the traefik

`docker network create treafik_net`

```bash
cd traefik
docker-compose up
```

See the traefik dashboard at localhost:8080

## Connect other docker-compose'd apps

```bash
cd whoami
docker-compose up
```

and

```bash
cd nginx
docker-compose up
```

This setup has benefits of:  each folder can be a different git repo.  Each folder can be anywhere on the filesystem.
