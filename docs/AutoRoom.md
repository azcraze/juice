# AutoRoom Help

Automatic voice channel management.<br/><br/>This cog facilitates automatic voice channel creation.<br/>When a member joins an AutoRoom Source (voice channel),<br/>this cog will move them to a brand new AutoRoom that they have control over.<br/>Once everyone leaves the AutoRoom, it is automatically deleted.<br/><br/>For a quick rundown on how to get started with this cog,<br/>check out [the readme](https://github.com/PhasecoreX/PCXCogs/tree/master/autoroom/README.md)

# autoroomset
 - Usage: `?autoroomset `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Configure the AutoRoom cog.<br/><br/>For a quick rundown on how to get started with this cog,<br/>check out [the readme](https://github.com/PhasecoreX/PCXCogs/tree/master/autoroom/README.md)

## autoroomset settings
 - Usage: `?autoroomset settings `

Display current settings.

## autoroomset create
 - Usage: `?autoroomset create <source_voice_channel> <dest_category> `
 - Aliases: `enable and add`

Create an AutoRoom Source.<br/><br/>Anyone joining an AutoRoom Source will automatically have a new<br/>voice channel (AutoRoom) created in the destination category,<br/>and then be moved into it.

## autoroomset modify
 - Usage: `?autoroomset modify `
 - Aliases: `edit`

Modify an existing AutoRoom Source.

### autoroomset modify type
 - Usage: `?autoroomset modify type `

Choose what type of AutoRoom is created.

#### autoroomset modify type locked
 - Usage: `?autoroomset modify type locked <autoroom_source> `

Rooms will be visible to all, but not joinable. AutoRoom Owner can allow users in.

#### autoroomset modify type server
 - Usage: `?autoroomset modify type server <autoroom_source> `

Rooms will be open to all, but the server owns the AutoRoom (so they can't be modified).

#### autoroomset modify type private
 - Usage: `?autoroomset modify type private <autoroom_source> `

Rooms will be hidden. AutoRoom Owner can allow users in.

#### autoroomset modify type public
 - Usage: `?autoroomset modify type public <autoroom_source> `

Rooms will be open to all. AutoRoom Owner has control over room.

### autoroomset modify text
 - Usage: `?autoroomset modify text `

Configure sending an introductory message to the AutoRoom text channel.

#### autoroomset modify text set
 - Usage: `?autoroomset modify text set <autoroom_source> <hint_text> `

Send a message to the newly generated AutoRoom text channel.<br/><br/>This can have template variables and statements, which you can learn more<br/>about by looking at `?autoroomset modify name custom`, or by looking at<br/>[the readme](https://github.com/PhasecoreX/PCXCogs/tree/master/autoroom/README.md).<br/><br/>The only additional variable that may be useful here is the `mention` variable,<br/>which will insert the users mention (pinging them).<br/><br/>- Example:<br/>`Hello {{mention}}! Welcome to your new AutoRoom!`

#### autoroomset modify text disable
 - Usage: `?autoroomset modify text disable <autoroom_source> `

Disable sending a message to the newly generated AutoRoom text channel.

### autoroomset modify category
 - Usage: `?autoroomset modify category <autoroom_source> <dest_category> `

Set the category that AutoRooms will be created in.

### autoroomset modify name
 - Usage: `?autoroomset modify name `

Set the default name format of an AutoRoom.

#### autoroomset modify name username
 - Usage: `?autoroomset modify name username <autoroom_source> `

Default format: PhasecoreX's Room.<br/><br/>Custom format example:<br/>`{{username}}'s Room{% if dupenum > 1 %} ({{dupenum}}){% endif %}`

#### autoroomset modify name game
 - Usage: `?autoroomset modify name game <autoroom_source> `

The users current playing game, otherwise the username format.<br/><br/>Custom format example:<br/>`{{game}}{% if not game %}{{username}}'s Room{% endif %}{% if dupenum > 1 %} ({{dupenum}}){% endif %}`

#### autoroomset modify name custom
 - Usage: `?autoroomset modify name custom <autoroom_source> <template> `

A custom channel name.<br/><br/>Use `{{ expressions }}` to print variables and `{% statements %}` to do basic evaluations on variables.<br/><br/>Variables supported:<br/>- `username` - AutoRoom Owner's username<br/>- `game    ` - AutoRoom Owner's game<br/>- `dupenum ` - An incrementing number that starts at 1, useful for un-duplicating channel names<br/><br/>Statements supported:<br/>- `if/elif/else/endif`<br/>- Example: `{% if dupenum > 1 %}DupeNum is {{dupenum}}, which is greater than 1{% endif %}`<br/>- Another example: `{% if not game %}User isn't playing a game!{% endif %}`<br/><br/>It's kinda like Jinja2, but way simpler. Check out [the readme](https://github.com/PhasecoreX/PCXCogs/tree/master/autoroom/README.md) for more info.

### autoroomset modify defaults
 - Usage: `?autoroomset modify defaults `
 - Aliases: `bitrate, memberrole, other, perms, and users`

Learn how AutoRoom defaults are set.

## autoroomset permissions
 - Usage: `?autoroomset permissions `
 - Aliases: `perms`

Check that the bot has all needed permissions.

## autoroomset remove
 - Usage: `?autoroomset remove <autoroom_source> `
 - Aliases: `disable, delete, and del`

Remove an AutoRoom Source.

## autoroomset access
 - Usage: `?autoroomset access `

Control access to all AutoRooms.<br/><br/>Roles that are considered "admin" or "moderator" are<br/>set up with the commands `?set addadminrole`<br/>and `?set addmodrole` (plus the remove commands too)

### autoroomset access admin
 - Usage: `?autoroomset access admin `

Allow Admins to join locked/private AutoRooms.

### autoroomset access mod
 - Usage: `?autoroomset access mod `

Allow Moderators to join locked/private AutoRooms.

### autoroomset access bot
 - Usage: `?autoroomset access bot `

Automatically allow bots into AutoRooms.<br/><br/>The AutoRoom Owner is able to freely allow or deny these roles as they see fit.

#### autoroomset access bot add
 - Usage: `?autoroomset access bot add <role> `

Allow a bot role into every AutoRoom.

#### autoroomset access bot remove
 - Usage: `?autoroomset access bot remove <role> `
 - Aliases: `delete and del`

Disallow a bot role from joining every AutoRoom.

# autoroom
 - Usage: `?autoroom `
 - Checks: `server_only`

Manage your AutoRoom.<br/><br/>For a quick rundown on how to manage your AutoRoom,<br/>check out [the readme](https://github.com/PhasecoreX/PCXCogs/tree/master/autoroom/README.md)

## autoroom settings
 - Usage: `?autoroom settings `
 - Aliases: `about and info`

Display current settings.

## autoroom locked
 - Usage: `?autoroom locked `

Lock your AutoRoom (visible, but no one can join).

## autoroom deny
 - Usage: `?autoroom deny <member_or_role> `
 - Aliases: `ban and block`

Deny a user (or role) from accessing your AutoRoom.<br/><br/>If the user is already in your AutoRoom, they will be disconnected.<br/><br/>If a user is no longer able to access the room due to denying a role,<br/>they too will be disconnected. Keep in mind that if the server is using<br/>member roles, denying roles will probably not work as expected.

## autoroom bitrate
 - Usage: `?autoroom bitrate <kbps> `
 - Aliases: `kbps`

Change the bitrate of your AutoRoom.

## autoroom users
 - Usage: `?autoroom users <user_limit> `
 - Aliases: `userlimit`

Change the user limit of your AutoRoom.

## autoroom name
 - Usage: `?autoroom name <name> `

Change the name of your AutoRoom.

## autoroom claim
 - Usage: `?autoroom claim `

Claim ownership of this AutoRoom.

## autoroom private
 - Usage: `?autoroom private `

Make your AutoRoom private.

## autoroom public
 - Usage: `?autoroom public `

Make your AutoRoom public.

## autoroom allow
 - Usage: `?autoroom allow <member_or_role> `
 - Aliases: `add`

Allow a user (or role) into your AutoRoom.

