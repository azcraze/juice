# Shell Help

Run shell commands on bot's system from Discord.

# shell
 - Usage: `?shell <command> `
 - Restricted to: `BOT_OWNER`

Run shell command.

# shellq
 - Usage: `?shellq <command> `
 - Restricted to: `BOT_OWNER`

Run shell command quietly.<br/><br/>If command's exit code is 0, `?shellq` will only send a tick reaction.<br/>Otherwise, the result will be shown as with regular `?shell` command.

# killshells
 - Usage: `?killshells `
 - Restricted to: `BOT_OWNER`

Kill all shell processes started by Shell cog.

# shellset
 - Usage: `?shellset `
 - Restricted to: `BOT_OWNER`

Manage settings of the Shell cog.

## shellset shell
 - Usage: `?shellset shell <replacement_shell> `

Set a replacement shell for the default ``/bin/sh``.<br/><br/>This needs to be a full path to the replacement shell.<br/>The input is not validated.<br/><br/>Only works on POSIX systems.

### shellset shell reset
 - Usage: `?shellset shell reset `

Reset the replacement shell back to the default.

