# Cosmos Cloud
**WARNING**: A database is set up by the UI using a volume instead of a bind
mount, so this setup is ***not*** self-contained.

Host mode networking needs to be explicitly enabled in Docker Desktop on macOS.

Newer docker compose versions will complain about the `version` directive, but
it is kept for backwards compatibility.
