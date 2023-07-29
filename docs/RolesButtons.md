# RolesButtons Help

A cog to have roles-buttons!

# rolesbuttons (Hybrid Command)
 - Usage: `?rolesbuttons `
 - Slash Usage: `/rolesbuttons `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Group of commands to use RolesButtons.

## rolesbuttons purge (Hybrid Command)
 - Usage: `?rolesbuttons purge `
 - Slash Usage: `/rolesbuttons purge `
 - Checks: `server_only`

Clear all roles-buttons for a server.

## rolesbuttons clear (Hybrid Command)
 - Usage: `?rolesbuttons clear <message> `
 - Slash Usage: `/rolesbuttons clear <message> `
 - Checks: `server_only`

Clear all roles-buttons for a message.

## rolesbuttons list (Hybrid Command)
 - Usage: `?rolesbuttons list [message=None] `
 - Slash Usage: `/rolesbuttons list [message=None] `
 - Checks: `server_only`



## rolesbuttons add (Hybrid Command)
 - Usage: `?rolesbuttons add <message> <role> <emoji> [style_button=2] [text_button] `
 - Slash Usage: `/rolesbuttons add <message> <role> <emoji> [style_button=2] [text_button] `
 - Aliases: `+`
 - Checks: `server_only`

Add a role-button for a message.<br/><br/>(Use the number for the color.)<br/>• `primary`: 1<br/>• `secondary`: 2<br/>• `success`: 3<br/>• `danger`: 4<br/># Aliases<br/>• `blurple`: 1<br/>• `grey`: 2<br/>• `gray`: 2<br/>• `green`: 3<br/>• `red`: 4

## rolesbuttons mode (Hybrid Command)
 - Usage: `?rolesbuttons mode <message> <mode> `
 - Slash Usage: `/rolesbuttons mode <message> <mode> `
 - Checks: `server_only`

Choose a mode for the roles-buttons of a message.<br/><br/>Type `add_or_remove`:<br/>- Users get the role if they do not already have it, or lose it.<br/>Type `add_only`:<br/>- Users can only get the role, but only manual action will remove it.<br/>Type `remove_only`:<br/>- Users can only lose a role, and will not be able to get it again without a manual action.<br/>Type `replace`:<br/>- Same as add_or_remove, but the roles from this message will be mutually exclusive, and getting one will remove the previous.

## rolesbuttons remove (Hybrid Command)
 - Usage: `?rolesbuttons remove <message> <config_identifier> `
 - Slash Usage: `/rolesbuttons remove <message> <config_identifier> `
 - Aliases: `-`
 - Checks: `server_only`

Remove a role-button for a message.<br/><br/>Use `?rolesbuttons list <message>` to find the config identifier.

## rolesbuttons bulk (Hybrid Command)
 - Usage: `?rolesbuttons bulk <message> <roles_buttons> `
 - Slash Usage: `/rolesbuttons bulk <message> <roles_buttons> `
 - Checks: `server_only`

Add roles-buttons for a message.<br/><br/>```?rolesbuttons bulk <message> :reaction1:|@role1 :reaction2:|@role2 :reaction3:|@role3```

