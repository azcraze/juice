# Editor Help

Allows for Administrators to edit a bot's messages by providing the new content or by copying another message

# editmessage
 - Usage: `?editmessage <ecid> <editid> <ccid> <content> `
 - Restricted to: `ADMIN`

Edits a message with the content of another message or the specified content.<br/><br/>Arguments:<br/>    - ecid: The ID of the channel of the message you are editing (Required)<br/><br/>    - editid: The ID of the message you are editing (Required)<br/><br/>    - ccid: The ID of the channel of the message you are copying from.  If you are giving the raw content yourself, pass 0 as the channel ID. (Optional)<br/><br/>    - content: The ID of the message that contains the contents of what you want the other message to become, or the new content of the message.  (Required, integer (for message id) or text (for new content)<br/><br/>Examples:<br/>`?editmessage <edit_channel_id> <edit_message_id> <copy_channel_id> <copy_message_id>`<br/>`?editmessage <edit_channel_id> <edit_message_id> 0 New content here`<br/><br/>Real Examples:<br/>`?editmessage 133251234164375552 578969593708806144 133251234164375552 578968157520134161`<br/>`?editmessage 133251234164375552 578969593708806144 0 ah bruh`

