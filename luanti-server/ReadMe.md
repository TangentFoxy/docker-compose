# Luanti server
Modified from [linuxserver version](https://docs.linuxserver.io/images/docker-luanti/),
because the [official version](https://docs.luanti.org/for-server-hosts/setup/containers/) doesn't support non-Linux hosts somehow?

The main config file (`LUANTI_SERVER/main-config/minetest.conf`)
may need some changes after it is generated to better support starting your server:

```
name = admin                   # Sign up as this user name to have admin rights.
secure.http_mods = digistuff   # optional feature
enable_tnt = true
```

Note that admin rights are not the same as in-game permissions,
you still need to use `/grantme all` to get all permissions,
and `/revokeme creative` if you don't want creative mode.

Worlds cannot start with a number or have spaces in their name,
and can only be selected by path for some reason.
