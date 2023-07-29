# Rift Help

Communicate with other servers/channels.

# send
 - Usage: `?send <rifts> `

Send a message to the specified destinations.<br/><br/>Editing or deleting the message you send will still forward<br/>to the bot's reposts, as in normal rifts.

# rift
 - Usage: `?rift `

Communicate with other channels through Red.

## rift notify
 - Usage: `?rift notify [notify] `
 - Restricted to: `BOT_OWNER`

Toggle whether the bot notifies the destination of an open rift.<br/><br/>The notification is only disabled for bot owners, and<br/>will still notify channels the bot owner doesn't have direct access to.

## rift open
 - Usage: `?rift open [one_way=None] <rifts> `

Opens a rift to the specified destination(s).<br/><br/>Only your messages will be forwarded to the specified destinations,<br/>and all replies will be sent back to you.

## rift blocklist
 - Usage: `?rift blocklist `
 - Aliases: `denylist and blacklist`

Configures blocklists.<br/><br/>Blocklisted destinations cannot have rifts opened to them.

### rift blocklist server
 - Usage: `?rift blocklist server `
 - Restricted to: `ADMIN`
 - Aliases: `server`
 - Checks: `server_only`

Blocklists the current server.<br/><br/>All channels and members in a server are considered blocklisted if the server is blocklisted.<br/>Members can still be reached if they are in another, non-blocklisted server.

### rift blocklist channel
 - Usage: `?rift blocklist channel [channel] `

Blocklists the current channel or the specified channel.<br/><br/>Can also blocklist DM channels.

## rift close
 - Usage: `?rift close `

Closes all rifts that lead to this channel.

### rift close server
 - Usage: `?rift close server `
 - Aliases: `server`
 - Checks: `server_only`

Closes all rifts that lead to this server.

## rift link
 - Usage: `?rift link [one_way=None] <rifts> `

Links this channel to the specified destination(s).<br/><br/>Anything anyone says in this channel will be forwarded.<br/>All replies will be relayed back here.

## rift web
 - Usage: `?rift web <rifts> `
 - Restricted to: `BOT_OWNER`

Opens up all possible connections between this channel and the specified rifts.<br/><br/>See the helptext of `?rift link` for more info.

## rift info
 - Usage: `?rift info [scope] `

Provides info about rifts opened in the specified scope.

