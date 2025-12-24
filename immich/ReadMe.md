# Immich
This was created following the [Docker Compose installation guide](https://docs.immich.app/install/docker-compose/).

WARNING: Does not work with docker-compose.

- Run this using docker compose manually and only use Cosmos Cloud to point a URL at it (and manage it after initial creation).
- Create the directories specified in the bind volumes *before* first-run.
- Doesn't work with env files for some reason, so that was removed. (I think Cosmos would've screwed that up potentially anyhow.)

(Paths currently set are from a test on a M4 Mac mini.)

NOTE: I highly recommend changing all admin settings before uploading anything.

## Major Version Upgrades / Breaking Changes
Check the official docs: https://docs.immich.app/install/upgrading/
