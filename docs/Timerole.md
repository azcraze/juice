# Timerole Help

Add roles to users based on time on server

# runtimerole
 - Usage: `?runtimerole `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Trigger the hourly timerole<br/><br/>Useful for troubleshooting the initial setup

# timerole
 - Usage: `?timerole `
 - Restricted to: `MOD`
 - Checks: `server_only`

Adjust timerole settings

## timerole reapply
 - Usage: `?timerole reapply `

Toggle reapplying roles if the member loses it somehow. Defaults to True

## timerole list
 - Usage: `?timerole list `

Lists all currently setup timeroles

## timerole removerole
 - Usage: `?timerole removerole <role> <time> <requiredroles> `

Add a role to be removed after specified time on server<br/><br/>Useful with an autorole cog

## timerole channel
 - Usage: `?timerole channel [channel=None] `

Sets the announce channel for role adds

## timerole skipbots
 - Usage: `?timerole skipbots `

Toggle skipping bots when adding/removing roles. Defaults to True

## timerole addrole
 - Usage: `?timerole addrole <role> <time> <requiredroles> `

Add a role to be added after specified time on server

## timerole delrole
 - Usage: `?timerole delrole <role> `

Deletes a role from being added/removed after specified time

