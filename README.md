# skript-utilities-lite

Small utility scripts for Minecraft servers. Right now it's just a clearlag-style item cleanup script.

Made for small SMP/survival servers that want something simple without installing heavy plugins.

---

## What's Included

**ClearLag Script** - Removes dropped items on a timer with warnings and manual controls.

---

## Features

**Automatic Cleanup**
- Runs every few minutes (configurable)
- Only clears dropped items from the ground
- Doesn't touch mobs, entities, or blocks

**Warnings**
- Broadcasts a 30 second warning
- Counts down from 10 with sounds
- Can be turned off if you want silent cleanup

**World Filtering**
- Only runs in worlds you specify
- Won't affect creative or lobby worlds unless you add them

**Bypass System**
- Items near players with bypass permission are protected
- Useful for staff organizing items or working on builds
- Configurable radius

**Commands**
- `/clearlag` - shows next cleanup time and commands
- `/clearlag now` - runs cleanup right away (needs permission)
- `/clearlag reload` - reloads config

---

## Permissions

| Permission | What it does |
|------------|--------------|
| `clearlag.now` | Let someone run cleanup manually |
| `clearlag.reload` | Let someone reload the config |
| `clearlag.bypass` | Protect items near this player |

---

## Requirements

- Minecraft Java Edition server
- Paper or Spigot
- Skript plugin installed

---

## Installation

1. Download the `.sk` file
2. Put it in `plugins/Skript/scripts/`
3. Run `/sk reload` or restart your server
4. Edit the options at the top of the file to configure

---

## Configuration

Open the script file and edit the options section at the top:
```skript
interval: 5           # how often cleanup runs (minutes)
warning_time: 30      # seconds before cleanup
bypass_radius: 10     # blocks around bypass players
world_1: world        # main world to clear
enable_warnings: true # turn warnings on/off
```

To add more worlds, add `world_2`, `world_3`, etc. and update the clearItems function.

---

## Limitations

This script removes items. That's all it does.

It won't fix lag from redstone, mob farms, or chunk loading. If you have serious performance issues on a larger server, you probably need a real optimization plugin.

This is meant for small servers where ground items are part of the problem, not the whole problem.

---

## License

Apache 2.0

---

## Contributing

Feel free to fork and improve it. Keep it simple though - that's the point.
