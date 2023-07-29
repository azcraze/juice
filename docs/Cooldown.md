# Cooldown Help

Add or remove cooldowns from/to commands<br/><br/>WARNING: Some cooldowns are meant to be in place, meaning that they should not be removed.<br/>Any contributors to this cog are not at fault if it is used improperly, and is instead at<br/>the fault of the person running the command.  By installing this cog, you agree to these terms.

# cooldown
 - Usage: `?cooldown `
 - Restricted to: `BOT_OWNER`

Group command for working with cooldowns for commands.

## cooldown remove
 - Usage: `?cooldown remove <command> `

Removes the cooldown from a command.<br/><br/>The cooldown can be one set from this cog or from inside the cog's code.<br/><br/>The command argument does not require quotes, as it consumes the rest in order to make cooldowns for subcommands easier.<br/><br/>Please do note however: some commands are meant to have cooldowns.  They may prevent something malicious from happening, or maybe your device from breaking or from being used too much.  I (Neuro Assassin <@473541068378341376>) or any other contributor to this cog take no responsibility for any complications that may result because of this.  Use at your own risk.<br/><br/>Note: Does not actually remove the command cooldown (undocumented), so instead it allows for the command to be run 100000 times every 1 second until the next boot up, where it will not be added (unless you are removing a cooldown from outside of this cog, then it will be kept after restart).

## cooldown add
 - Usage: `?cooldown add <rate> <per> <btype> <command> `

Sets a cooldown for a command, allowing a certain amount of times in a certain amount of time for a certain type.  If a cooldown already exists for the specified command, then it will be overwritten and edited.<br/><br/>The command argument does not require quotes, as it consumes the rest in order to make cooldowns for subcommands easier.<br/><br/>Example: `?cooldown add 1 5s user ping`<br/><br/>The above example will limit a user to using the `ping` command every 5 seconds.<br/><br/>Example 2: `?cooldown add 5 10m server alias add`<br/><br/>The above example (number 2) will limit people in a server to using the `alias add` command to 5 times every 10 minutes.<br/><br/>Time Types:<br/>-   S   =>  Seconds<br/>-   M   =>  Minutes<br/>-   H   =>  Hours<br/>-   D   =>  Days<br/><br/>Bucket Types:<br/>-   User<br/>-   Channel<br/>-   Guild<br/>-   Global<br/><br/>Arguments:<br/>-   Rate:      how many times<br/>-   Per:       during how long<br/>-   Type:      for what type<br/>-   Command:   for what command.  Do not use a prefix, and does not work with aliases.  Please pass the actual command for the alias if you wish.

