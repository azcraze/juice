# Sticky Help

Sticky messages to your channels.

# sticky
 - Usage: `?sticky <content> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Sticky a message to this channel.

## sticky existing
 - Usage: `?sticky existing <message_id_or_url> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Sticky an existing message to this channel.<br/><br/>This will try to sticky the content and embed of the message.<br/>Attachments will not be added to the stickied message.<br/><br/>Stickying messages with multiple embeds may result in unexpected<br/>behaviour, as the bot cannot send multiple rich embeds in a<br/>single message.

## sticky toggleheader
 - Usage: `?sticky toggleheader <true_or_false> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Toggle the header for stickied messages in this channel.<br/><br/>The header is enabled by default.

# unsticky
 - Usage: `?unsticky [force=False] `
 - Restricted to: `MOD`
 - Checks: `server_only`

Remove the sticky message from this channel.<br/><br/>Deleting the sticky message will also unsticky it.<br/><br/>Do `?unsticky yes` to skip the confirmation prompt.

