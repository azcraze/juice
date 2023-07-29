# PhenUtils Help

Various developer utilities.

# do
 - Usage: `?do <times> [sequential=True] <command> `
 - Restricted to: `BOT_OWNER`

Repeats a command a specified number of times.<br/><br/>`--sleep <int>` is an optional flag specifying how much time to wait between command invocations.

# execute
 - Usage: `?execute [sequential=False] <commands> `
 - Restricted to: `BOT_OWNER`

Execute multiple commands at once. Split them using |.

# bypass
 - Usage: `?bypass <command> `
 - Restricted to: `BOT_OWNER`

Bypass a command's checks and cooldowns.

# timing
 - Usage: `?timing <command_string> `
 - Restricted to: `BOT_OWNER`

Run a command timing execution and catching exceptions.

# schedulecmd
 - Usage: `?schedulecmd <time> <command> `
 - Restricted to: `BOT_OWNER`
 - Aliases: `taskcmd`

Schedule a command to be done later.

# reinvoke
 - Usage: `?reinvoke [message=None] `
 - Restricted to: `BOT_OWNER`

Reinvoke a command message.<br/><br/>You may reply to a message to reinvoke it or pass a message ID/link.

# loglevel
 - Usage: `?loglevel <level> `
 - Restricted to: `BOT_OWNER`

Set the log output level.

