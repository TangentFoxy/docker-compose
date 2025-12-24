# PeerTube
Modified from official instructions: https://docs.joinpeertube.org/install/docker

1. Edit `docker-compose.yml`
2. Generate `PEERTUBE_SECRET` using `openssl rand -hex 32`.
3. Create the volume directories needed: config, data, opendkim, postgres, redis
4. Launch from CLI docker compose.
5. Search logs for "User password" (near the end) to find the generated password for the root account.
