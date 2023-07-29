# NitroRole Help

Welcome new nitro boosters and/or give them a special role!

# nitrorole
 - Usage: `?nitrorole `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Settings for NitroRole cog.

## nitrorole channel
 - Usage: `?nitrorole channel [channel=None] `

Set channel for new booster messages. Leave empty to disable.

## nitrorole listmessages
 - Usage: `?nitrorole listmessages `

List new booster message templates.

## nitrorole unsetimage
 - Usage: `?nitrorole unsetimage `

Unset image for new booster message.

## nitrorole removemessage
 - Usage: `?nitrorole removemessage `
 - Aliases: `deletemessage`

Remove new booster message.

## nitrorole unassignonboostend
 - Usage: `?nitrorole unassignonboostend [enabled=None] `

Set if booster role should be unassigned when someone stops boosting server.<br/><br/>Leave empty to see current settings.

## nitrorole setimage
 - Usage: `?nitrorole setimage `

Set image for new booster message.

## nitrorole addmessage
 - Usage: `?nitrorole addmessage <message> `

Add new booster message.<br/><br/>Those fields will get replaced automatically:<br/>$mention - Mention the user who boosted<br/>$username - The user's display name<br/>$server - The name of the server<br/>$count - The number of boosts server has<br/>(this isn't the same as amount of users that boost this server)<br/>$plural - Empty if count is 1. 's' otherwise<br/><br/>Note: New booster message can also have image.<br/>To set it, use `?nitrorole setimage`

## nitrorole autoassignrole
 - Usage: `?nitrorole autoassignrole [role] `

Set role that will be autoassigned after someone boosts server.<br/><br/>Leave empty to not assign any role.

