# EditFile Help

A cog to get a file and replace it from its path from Discord!<br/><br/>⚠️ This cog can be very dangerous, since it allows direct read/write/delete of files on the bot’s machine, considering the fact that reading the wrong file can expose sensitive information like tokens and deleting the wrong file can corrupt the bot or the system entirely.

# editfile (Hybrid Command)
 - Usage: `?editfile `
 - Slash Usage: `/editfile `
 - Restricted to: `BOT_OWNER`
 - Aliases: `fileedit`

Commands group to get a file and replace it from its path.

## editfile delete (Hybrid Command)
 - Usage: `?editfile delete <path> `
 - Slash Usage: `/editfile delete <path> `
 - Aliases: `-`

Delete a file.

## editfile get (Hybrid Command)
 - Usage: `?editfile get [menu=False] [show_line=False] <path> `
 - Slash Usage: `/editfile get [menu=False] [show_line=False] <path> `

Get a file on the bot's host machine from its path.<br/>`#L10` or `#L10-L30` is supported.

## editfile listdir (Hybrid Command)
 - Usage: `?editfile listdir <path> `
 - Slash Usage: `/editfile listdir <path> `

List all files/directories of a directory from its path.

## editfile findcog (Hybrid Command)
 - Usage: `?editfile findcog <cog> `
 - Slash Usage: `/editfile findcog <cog> `

Get a cog directory on the bot's host machine from its name.

## editfile rename (Hybrid Command)
 - Usage: `?editfile rename <new_name> <path> `
 - Slash Usage: `/editfile rename <new_name> <path> `

Rename a file.

## editfile replace (Hybrid Command)
 - Usage: `?editfile replace <path> [content] `
 - Slash Usage: `/editfile replace <path> [content] `

Replace a file on the bot's host machine from its path.<br/>`#L10` or `#L10-L30` is supported.

