# ConsoleLogs Help

A cog to display the console logs, with buttons and filter options, and to send commands errors in configured channels!

# consolelogs (Hybrid Command)
 - Usage: `?consolelogs [index=-1] [level=None] [logger_name=None] `
 - Slash Usage: `/consolelogs [index=-1] [level=None] [logger_name=None] `
 - Restricted to: `BOT_OWNER`

View a console log, for a provided level/logger name.

## consolelogs view (Hybrid Command)
 - Usage: `?consolelogs view [index=-1] [level=None] [logger_name=None] `
 - Slash Usage: `/consolelogs view [index=-1] [level=None] [logger_name=None] `

View the console logs one by one, for all levels/loggers or provided level/logger name.

## consolelogs scroll (Hybrid Command)
 - Usage: `?consolelogs scroll [lines_break=2] [level=None] [logger_name=None] `
 - Slash Usage: `/consolelogs scroll [lines_break=2] [level=None] [logger_name=None] `

Scroll the console logs, for all levels/loggers or provided level/logger name.

## consolelogs addchannel (Hybrid Command)
 - Usage: `?consolelogs addchannel <channel> [global_errors=True] [prefixed_commands_errors=True] [slash_commands_errors=True] [dpy_ignored_exceptions=False] [server_invite=False] `
 - Slash Usage: `/consolelogs addchannel <channel> [global_errors=True] [prefixed_commands_errors=True] [slash_commands_errors=True] [dpy_ignored_exceptions=False] [server_invite=False] `
 - Aliases: `+`

Enable errors logging in a channel.<br/><br/>**Parameters:**<br/>- `channel`: The channel where the commands errors will be sent.<br/>- `global_errors`: Log errors for the entire bot, not just the channel server.<br/>- `prefixed_commands_errors`: Log prefixed commands errors.<br/>- `slash_commands_errors`: Log slash commands errors.<br/>- `dpy_ignored_exceptions`: Log dpy ignored exceptions (events listeners and Views errors).<br/>- `server_invite`: Add a button "Guild Invite" in commands errors logs, only for community servers.

## consolelogs errors (Hybrid Command)
 - Usage: `?consolelogs errors [index=-1] [logger_name=None] `
 - Slash Usage: `/consolelogs errors [index=-1] [logger_name=None] `
 - Aliases: `error`

View the `ERROR` console logs one by one, for all loggers or a provided logger name.

## consolelogs removechannel (Hybrid Command)
 - Usage: `?consolelogs removechannel <channel> `
 - Slash Usage: `/consolelogs removechannel <channel> `
 - Aliases: `-`

Disable errors logging in a channel.

## consolelogs stats (Hybrid Command)
 - Usage: `?consolelogs stats `
 - Slash Usage: `/consolelogs stats `
 - Aliases: `listloggers`

Scroll the console logs, for all levels/loggers or provided level/logger name.

## consolelogs getdebugloopsstatus (Hybrid Command)
 - Usage: `?consolelogs getdebugloopsstatus `
 - Slash Usage: `/consolelogs getdebugloopsstatus `

Get an embed to check loops status.

