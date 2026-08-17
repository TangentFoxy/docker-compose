# Cosmos Cloud
**WARNING**: A database is set up by the UI using a volume instead of a bind
mount, so this setup is ***not*** self-contained.

Newer docker compose versions will complain about the `version` directive, but
it is kept for backwards compatibility.

## Setup
Host mode networking needs to be explicitly enabled in Docker Desktop on macOS before attempting to run this.
