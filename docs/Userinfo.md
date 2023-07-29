# Userinfo Help

Replace original Red userinfo command with more details.

# uinfoset
 - Usage: `?uinfoset `
 - Restricted to: `BOT_OWNER`

Manage userinfo settings.

## uinfoset clear
 - Usage: `?uinfoset clear `

Reset emojis to default.

## uinfoset setemoji
 - Usage: `?uinfoset setemoji <status_or_badge> <type> <emoji_id> `

Set status or badge emoji

## uinfoset banner
 - Usage: `?uinfoset banner `

Toggle banner on userinfo.<br/><br/>Note: This causes a fetch request which can be a heavy operation.

# userinfo (Hybrid Command)
 - Usage: `?userinfo [user] `
 - Slash Usage: `/userinfo [user] `
 - Cooldown: `1 per 10.0 seconds`
 - Checks: `server_only`

Show userinfo with some more detail.

