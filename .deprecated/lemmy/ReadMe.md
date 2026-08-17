# Lemmy
A federated reddit-style board.

This is like my 3rd attempt to make Lemmy do anything, but it is fundamentally
unable to run alongside other apps for no reason? I don't know.

Modified from official instructions and resources at
https://join-lemmy.org/docs/administration/install_docker.html

1. Copy all files (ReadMe.md unnecessary) to the target location.
2. Make changes in docker-compose.yml
3. Make changes in config.hjson
4. `mkdir -p volumes/pictrs volumes/lemmy-ui/extra_themes volumes/postgres`
5. `sudo chown 991:991 volumes/pictrs`
