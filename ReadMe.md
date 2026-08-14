# docker-compose
These are most of the docker-compose.yml files I use (with secrets removed, of
course). Technology hates me just often enough that I have to keep multiple
backups of everything because my shit gets rocked so often. :D

See [[Table-of-Services.md]] for what each of these does, as well as seeing what
I've discarded because it sucks (or just isn't for me).

Most of these are designed to be run behind a reverse proxy, and I use Cosmos
for this. As a result, I often comment out `ports` declarations. Initial setup
should probably be shielded by the reverse proxy login.

## Usage
1. Put the `docker-compose.yml` file where you want data to live.
2. Edit the file to set correct information based on the TODOs at the top.
3. **Run `docker-compose up -d` before using any form of GUI.** (If this step is skipped, volumes will *not* be set up correctly and you have to start over.)

## Named bind mounts
Managing volumes that need to be shared within a config is easier if you can use names with bind mounts:
```
volumes:
  name:
    driver: local
    driver_opts:
      type: none
      o: bind
      device: /path/on/host
```

Remember that directories must be created *before* starting containers.

## Standard reminder notes
I place these at the top of compose files for different changes that need to be made to use these files:
- `# TODO set volume directories`: Named bind mount paths must be set (near top of file).
- `# TODO change ALL_CAPS environment variables in all locations`: Environment variables for secrets (or settings) must be set.
- `# TODO set user/group IDs`: Container(s) must have a user block (`user: "USER:GROUP"`) set to the correct **numerical** permissions.
- `# TODO set timezone (TZ)`: A timezone environment variable (named `TZ`) must be set. (For me, `America/Denver`.)

## ReadMes
1. Note where I got the original compose file or documentation.
2. Add instructions.
3. End with notes about complications or issues I ran into.
