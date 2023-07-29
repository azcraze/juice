# RoleUtils Help

Useful role commands.<br/><br/>Includes massroling, role targeting, and reaction roles.

# reactrole
 - Usage: `?reactrole `

Base command for Reaction Role management.

## reactrole bind
 - Usage: `?reactrole bind <message> <emoji> <role> `
 - Checks: `bot_has_server_permissions`

Bind a reaction role to an emoji on a message.

## reactrole clear
 - Usage: `?reactrole clear `
 - Restricted to: `BOT_OWNER`

Clear all ReactRole data.

## reactrole delete
 - Usage: `?reactrole delete <message> `
 - Aliases: `remove`

Delete an entire reaction role for a message.

### reactrole delete bind
 - Usage: `?reactrole delete bind <message> <emoji> `

Delete an emoji-role bind for a reaction role.

## reactrole create
 - Usage: `?reactrole create <emoji_role_groups> [channel=None] [color=None] [name] `

Create a reaction role.<br/><br/>Emoji and role groups should be seperated by a ';' and have no space.<br/><br/>Example:<br/>    - ?reactrole create 🎃;@SpookyRole 🅱️;MemeRole #role_channel Red

## reactrole list
 - Usage: `?reactrole list `

View the reaction roles on this server.

# role
 - Usage: `?role <member> <role> `
 - Checks: `server_only`

Base command for modifying roles.<br/><br/>Invoking this command will add or remove the given role from the member, depending on whether they already had it.

## role add
 - Usage: `?role add <member> <role> `

Add a role to a member.

## role humans
 - Usage: `?role humans <role> `

Add a role to all humans (non-bots) in the server.

## role rin
 - Usage: `?role rin <target_role> <remove_role> `

Remove a role from all members of a another role.

## role rhumans
 - Usage: `?role rhumans <role> `

Remove a role from all humans (non-bots) in the server.

## role all
 - Usage: `?role all <role> `

Add a role to all members of the server.

## role remove
 - Usage: `?role remove <member> <role> `

Remove a role from a member.

## role name
 - Usage: `?role name <role> <name> `

Change a role's name.

## role info
 - Usage: `?role info <role> `

Get information about a role.

## role target
 - Usage: `?role target `
 - Checks: `targeter_cog`

Modify roles using 'targeting' args.<br/><br/>An explanation of Targeter and test commands to preview the members affected can be found with `?target`.

### role target remove
 - Usage: `?role target remove <role> <args> `

Remove a role from members using targeting args.<br/><br/>An explanation of Targeter and test commands to preview the members affected can be found with `?target`.

### role target add
 - Usage: `?role target add <role> <args> `

Add a role to members using targeting args.<br/><br/>An explanation of Targeter and test commands to preview the members affected can be found with `?target`.

## role bots
 - Usage: `?role bots <role> `

Add a role to all bots in the server.

## role color
 - Usage: `?role color <role> <color> `
 - Aliases: `colour`

Change a role's color.

## role addmulti
 - Usage: `?role addmulti <role> <members> `

Add a role to multiple members.

## role uniquemembers
 - Usage: `?role uniquemembers <roles> `
 - Aliases: `um`

View the total unique members between multiple roles.

## role hoist
 - Usage: `?role hoist <role> [hoisted=None] `

Toggle whether a role should appear seperate from other roles.

## role rbots
 - Usage: `?role rbots <role> `

Remove a role from all bots in the server.

## role create
 - Usage: `?role create [color=#000000] [hoist=False] [name] `

Creates a role.<br/><br/>Color and whether it is hoisted can be specified.

## role removemulti
 - Usage: `?role removemulti <role> <members> `

Remove a role from multiple members.

## role rall
 - Usage: `?role rall <role> `
 - Aliases: `removeall`

Remove a role from all members of the server.

## role members
 - Usage: `?role members <role> [formatting] `
 - Aliases: `dump`

Sends a list of members in a role.<br/><br/>You can supply a custom formatting tagscript for each member.<br/>The [member](https://phen-cogs.readthedocs.io/en/latest/tags/default_variables.html#author-block) block is available to use, found on the [TagScript documentation](https://phen-cogs.readthedocs.io/en/latest/index.html).<br/><br/>**Example:**<br/>`?role dump @admin <t:{member(timestamp)}> - {member(mention)}`

## role in
 - Usage: `?role in <target_role> <add_role> `

Add a role to all members of a another role.

## role colors
 - Usage: `?role colors `

Sends the server's roles, ordered by color.

# multirole
 - Usage: `?multirole <member> <roles> `

Add multiple roles to a member.

## multirole remove
 - Usage: `?multirole remove <member> <roles> `

Remove multiple roles from a member.

