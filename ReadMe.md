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
