# CmdLog Help

Log command usage in a form searchable by user ID, server ID or command name.<br/><br/>The cog keeps an internal cache and everything is also logged to the bot's main logs under<br/>`red.vex.cmdlog`, level INFO.<br/><br/>The internal cache is non persistant and subsequently is lost on cog unload,<br/>including bot shutdowns. The logged data will last until Red's custom logging<br/>rotator deletes old logs.

# cmdloginfo
 - Usage: `?cmdloginfo `



# cmdlog
 - Usage: `?cmdlog `
 - Restricted to: `BOT_OWNER`
 - Aliases: `cmdlogs`

View command logs.<br/><br/>Note the cache is limited to 100 000 commands, which is approximately 50MB of RAM

## cmdlog content
 - Usage: `?cmdlog content <to_log> `

Set whether or not whole message content should be logged. Default false.

## cmdlog user
 - Usage: `?cmdlog user <user_id> `

Upload all the logs that are stored for a specific User ID in the cache.<br/><br/>**Example:**<br/>- `?cmdlog user 418078199982063626`

## cmdlog cache
 - Usage: `?cmdlog cache `

Show the size of the internal command cache.

## cmdlog server
 - Usage: `?cmdlog server <server_id> `
 - Aliases: `server`

Upload all the logs that are stored for for a specific server ID in the cache.<br/><br/>**Example:**<br/>- `?cmdlog server 527961662716772392`

## cmdlog channel
 - Usage: `?cmdlog channel <channel> `
 - Checks: `server_only`

Set the channel to send logs to, this is optional.<br/><br/>Run the comand without a channel to stop sending.<br/><br/>**Example:**<br/>- `?cmdlog channel #com-log` - set the log channel to #com-log<br/>- `?cmdlog channel` - stop sending logs

## cmdlog command
 - Usage: `?cmdlog command <command> `

Upload all the logs that are stored for a specific command in the cache.<br/><br/>This does not check it is a real command, so be careful. Do not enclose it in " if there<br/>are spaces.<br/><br/>You can search for a group command (eg `cmdlog`) or a full command (eg `cmdlog user`).<br/>As arguments are not stored, you cannot search for them.<br/><br/>**Examples:**<br/>- `?cmdlog command ping`<br/>- `?cmdlog command playlist`<br/>- `?cmdlog command playlist create`

## cmdlog full
 - Usage: `?cmdlog full `

Upload all the logs that are stored in the cache.

