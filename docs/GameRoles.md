# GameRoles Help

Grant roles when a user is playing a specific game.

# gameroles
 - Usage: `?gameroles `
 - Aliases: `gr`
 - Checks: `server_only`

Group command for game roles.

## gameroles addrole
 - Usage: `?gameroles addrole <role> `
 - Restricted to: `GUILD_OWNER`

Sets a role to be managed by gameroles.<br/><br/>Roles with multiple words need to be surrounded in quotes.<br/>The bot's highest role needs to be above the role that you are adding and the bot needs permission to manage roles.

## gameroles currentactivity
 - Usage: `?gameroles currentactivity `
 - Restricted to: `GUILD_OWNER`

Get your current activity.

## gameroles delrole
 - Usage: `?gameroles delrole <role> `
 - Restricted to: `GUILD_OWNER`

Stop a role from being managed by gameroles.<br/><br/>Roles with multiple words need to be surrounded in quotes.<br/>Accepts the ID of the role in case it was deleted.

## gameroles delactivity
 - Usage: `?gameroles delactivity <role> <activity> `
 - Restricted to: `GUILD_OWNER`

Remove an activity from triggering a role.<br/><br/>Roles and activities with multiple words need to be surrounded in quotes.<br/>You can get the name of your current activity with ?gameroles currentactivity.

## gameroles listroles
 - Usage: `?gameroles listroles `
 - Restricted to: `GUILD_OWNER`

List the roles currently managed by gameroles.

## gameroles recheck
 - Usage: `?gameroles recheck `

Force a recheck of your current activities.

## gameroles addactivity
 - Usage: `?gameroles addactivity <role> <activity> `
 - Restricted to: `GUILD_OWNER`

Add an activity to trigger a role.<br/><br/>Roles and activities with multiple words need to be surrounded in quotes.<br/>You can get the name of your current activity with ?gameroles currentactivity.

## gameroles listactivities
 - Usage: `?gameroles listactivities <role> `
 - Restricted to: `GUILD_OWNER`

List the activities that trigger a role.<br/><br/>Roles with multiple words need to be surrounded in quotes.

# gameroleset
 - Usage: `?gameroleset `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `grset`
 - Checks: `server_only`

Config options for gameroles.

## gameroleset remove
 - Usage: `?gameroleset remove [value=None] `

Set if roles should be removed when someone stops playing a game.<br/><br/>Defaults to True.<br/>This value is server specific.

## gameroleset add
 - Usage: `?gameroleset add [value=None] `

Set if roles should be added when someone starts playing a game.<br/><br/>Defaults to True.<br/>This value is server specific.

