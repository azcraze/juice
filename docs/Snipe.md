# Snipe Help

Snipe the last message from a server.

# snipe (Hybrid Command)
 - Usage: `?snipe [amount=1] [channel=None] `
 - Slash Usage: `/snipe [amount=1] [channel=None] `
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`

Shows the last deleted message from a specified channel.

# editsnipe
 - Usage: `?editsnipe [amount=1] [channel=None] `
 - Aliases: `esnipe`
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`

Shows the last deleted message from a specified channel.

# snipeset
 - Usage: `?snipeset `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Group Command for Snipe Settings.

## snipeset max
 - Usage: `?snipeset max <amount> `

Set the max amount of snipes to store per channel.

## snipeset ignore
 - Usage: `?snipeset ignore <user_or_channel> `

Add a user or channel to the ignore list.

## snipeset deletetime
 - Usage: `?snipeset deletetime <time> `
 - Restricted to: `BOT_OWNER`

Set the time for snipes to be removed automatically.<br/><br/>Takes seconds or minutes, use the whole unit name with the amount.<br/>Defaults to seconds if no unit name used.

## snipeset enable
 - Usage: `?snipeset enable <state> `

Enable or disable sniping.<br/><br/>State must be a bool or one of the following: True/False, On/Off, Y/N

## snipeset time
 - Usage: `?snipeset time <time> `

Set the time before snipes expire.<br/><br/>Takes seconds or minutes, use the whole unit name with the amount.<br/>Defaults to seconds if no unit name used.

