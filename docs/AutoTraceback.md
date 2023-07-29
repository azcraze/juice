# AutoTraceback Help

A cog to display the error traceback of a command automatically after the error!

# traceback (Hybrid Command)
 - Usage: `?traceback [public=True] [index=0] `
 - Slash Usage: `/traceback [public=True] [index=0] `
 - Restricted to: `BOT_OWNER`

Sends to the owner the last command exception that has occurred.<br/><br/>If public (yes is specified), it will be sent to the chat instead.<br/><br/>Warning: Sending the traceback publicly can accidentally reveal sensitive information about your computer or configuration.<br/><br/>**Examples:**<br/>    - `?traceback` - Sends the traceback to your DMs.<br/>    - `?traceback True` - Sends the last traceback in the current context.<br/><br/>**Arguments:**<br/>    - `[public]` - Whether to send the traceback to the current context. Default is `True`.<br/>    - `[index]`  - The error index. `0` is the last one.

