# Tools Help

Mod and Admin tools.

# access
 - Usage: `?access `
 - Restricted to: `MOD`
 - Checks: `server_only`

Check channel access

## access compare
 - Usage: `?access compare <user> [server=None] `

Compare channel access with another user.

## access voice
 - Usage: `?access voice [user=None] [server=None] `

Check voice channel access.

## access text
 - Usage: `?access text [user=None] [server=None] `

Check text channel access.

# banlist
 - Usage: `?banlist `
 - Restricted to: `MOD`
 - Checks: `server_only`

Displays the server's banlist.

# cid
 - Usage: `?cid `
 - Checks: `server_only`

Shows the channel id for the current channel.

# chinfo
 - Usage: `?chinfo [channel=None] `
 - Checks: `server_only`

Shows channel information. Defaults to current text channel.

# eid
 - Usage: `?eid <emoji> `
 - Checks: `server_only`

Get an id for an emoji.

# einfo
 - Usage: `?einfo <emoji> `
 - Checks: `server_only`

Emoji information.

# inrole
 - Usage: `?inrole <rolename> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Check members in the role specified.

# joined
 - Usage: `?joined [user=None] `
 - Checks: `server_only`

Show when a user joined the server.

# listservers
 - Usage: `?listservers `
 - Restricted to: `MOD`
 - Aliases: `listservers, serverlist, and serverlist`

List the servers|servers the bot is in.

# listchannel
 - Usage: `?listchannel `
 - Restricted to: `MOD`
 - Aliases: `channellist`
 - Checks: `server_only`

List the channels of the current server

# newusers
 - Usage: `?newusers [count=5] [text_format=py] `
 - Restricted to: `MOD`
 - Checks: `server_only`

Lists the newest 5 members.<br/><br/>`text_format` is the markdown language to use. Defaults to `py`.

# perms
 - Usage: `?perms [user=None] `
 - Restricted to: `MOD`
 - Checks: `server_only`

Fetch a specific user's permissions.

# rid
 - Usage: `?rid <rolename> `
 - Checks: `server_only`

Shows the id of a role.

# rinfo
 - Usage: `?rinfo <rolename> `
 - Checks: `server_only`

Shows role info.

# rolelist
 - Usage: `?rolelist `
 - Restricted to: `MOD`
 - Aliases: `listroles`
 - Checks: `server_only`

Displays the server's roles.

# sharedservers
 - Usage: `?sharedservers [user=None] `

Shows shared server info. Defaults to author.

# sid
 - Usage: `?sid `
 - Checks: `server_only`

Show the server id.

# sinfo
 - Usage: `?sinfo [server=None] `
 - Aliases: `ginfo`
 - Checks: `server_only`

Shows server information.

# stinfo
 - Usage: `?stinfo [message_link=None] `
 - Aliases: `stickerinfo`
 - Checks: `server_only`

Sticker information.<br/><br/>Attach a sticker to the command message or provide a link to a message with a sticker.

# uid
 - Usage: `?uid <partial_name_or_nick> `
 - Checks: `server_only`

Get a member's id from a fuzzy name search.

# uimages
 - Usage: `?uimages [user=None] [embed=False] `
 - Checks: `server_only`

Shows user image urls. Defaults to author.<br/><br/>`embed` is a True/False value for whether to display the info in an embed.

# uinfo
 - Usage: `?uinfo [user=None] `
 - Checks: `server_only`

Shows user information. Defaults to author.

# whatis
 - Usage: `?whatis <what_is_this_id> `
 - Checks: `server_only`

What is it?

