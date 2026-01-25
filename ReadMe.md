# docker-compose
These are most of the docker-compose.yml files I use (with secrets removed, of
course). Technology hates me just often enough that I have to keep multiple
backups of everything because my shit gets rocked so often. :D

See [[Table-of-Services.md]] for what each of these does, as well as seeing what
I've discarded because it sucks (or just isn't for me).

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
