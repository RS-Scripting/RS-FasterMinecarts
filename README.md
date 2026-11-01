# RS-FasterMinecarts

RS-FasterMinecarts is a lightweight Paper plugin that increases the maximum travel speed of minecarts while a player is riding inside them.

The plugin only affects player-occupied minecarts. All other minecarts and entities behave normally.

## Features

- Increase player-occupied minecart speed
- Configurable speed multiplier
- Uses the minecart's existing maximum speed as the baseline
- Automatically restores the original minecart speed when the player exits
- No commands
- No permissions
- No database
- No impact on server tick rate

## How It Works

When a player enters a minecart, RS-FasterMinecarts:

1. Records the minecart's current maximum speed.
2. Reads the `max-speed` multiplier from `config.yml`.
3. Multiplies the minecart's original maximum speed by that value.
4. Applies the new maximum speed to that minecart.

When the player exits, the original maximum speed is restored.

For example, with `max-speed: 3.0`, a minecart with an original maximum speed of `0.4` will be given a maximum speed of `1.2`.

## Configuration

The default configuration is:

```yaml
max-speed: 3.0
```

### max-speed

Controls the speed multiplier applied to player-occupied minecarts.

| Value | Effect |
|---|---|
| `1.0` | Normal minecart speed |
| `2.0` | 2× normal maximum speed |
| `3.0` | 3× normal maximum speed |
| `4.0` | 4× normal maximum speed |

## What Is Affected?

### Affected

- Minecarts with a player riding inside

### Not Affected

- Empty minecarts
- Furnace minecarts
- Chest minecarts
- Hopper minecarts
- TNT minecarts
- Other minecart variants without a player riding inside
- Boats
- Horses
- Player movement
- Other entities

## Commands

None.

## Permissions

None.

## Installation

1. Download the RS-FasterMinecarts JAR.
2. Place the JAR file into your server's `plugins` folder.
3. Start or restart the server.
4. Adjust `config.yml` if desired.

## Requirements

- Paper
- Java 21 or newer

## Version

Current version: **0.1.0**

## Support

For bug reports, feature requests, and support, use the RS Scripting project issue tracker.
