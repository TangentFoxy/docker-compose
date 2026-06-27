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

## Schematics
Assuming WorldEdit is installed, you can move things between worlds using schematics:
1. Select corners of a volume by standing where you want them and running `//pos1` and `//pos2`.
   The selection box will be at your feet.
2. Save schematics with `//mtschemcreate SCHEMATIC_NAME`.
3. Schematics are placed in a world's `schems` directory. Copy them and rename them as necessary.
4. Use `//pos1` to select a start point, and `//mtschemplace SCHEMATIC_NAME` to place it.

## Unsafe Chainsaw
The `technic` mod's chainsaw by default protects you from destroying player-built structures,
but this also prevents several mods' trees from being cut by it. This can be changed by disabling its safety check:
`technic_safe_chainsaw = false`
