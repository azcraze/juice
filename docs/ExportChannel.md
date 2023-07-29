# ExportChannel Help

A cog to export all or part of a channel's messages to an html file!

# exportchannel (Hybrid Command)
 - Usage: `?exportchannel `
 - Slash Usage: `/exportchannel `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `exportmessages`
 - Checks: `server_only`

Commands to export all or part of a channel's messages to an html file.

## exportchannel all (Hybrid Command)
 - Usage: `?exportchannel all [channel=None] `
 - Slash Usage: `/exportchannel all [channel=None] `
 - Checks: `server_only`

Export all of a channel's messages to an html file.<br/><br/>Please note: all attachments and user avatars are saved with the Discord link in this file.<br/>Remember that exporting other users' messages from Discord does not respect the TOS.

## exportchannel messages (Hybrid Command)
 - Usage: `?exportchannel messages <channel> <limit> `
 - Slash Usage: `/exportchannel messages <channel> <limit> `
 - Checks: `server_only`

Export part of a channel's messages to an html file.<br/><br/>Specify the number of messages since the end of the channel.<br/>Please note: all attachments and user avatars are saved with the Discord link in this file.<br/>Remember that exporting other users' messages from Discord does not respect the TOS.

## exportchannel after (Hybrid Command)
 - Usage: `?exportchannel after <channel> <after> `
 - Slash Usage: `/exportchannel after <channel> <after> `
 - Checks: `server_only`

Export part of a channel's messages to an html file.<br/><br/>Specify the after message (id or link) or a valid snowflake.<br/>Please note: all attachments and user avatars are saved with the Discord link in this file.<br/>Remember that exporting other users' messages from Discord does not respect the TOS.

## exportchannel user (Hybrid Command)
 - Usage: `?exportchannel user <channel> <user> [limit=None] `
 - Slash Usage: `/exportchannel user <channel> <user> [limit=None] `
 - Checks: `server_only`

Export part of a channel's messages to an html file.<br/><br/>Specify the user/member (id, name or mention).<br/>Please note: all attachments and user avatars are saved with the Discord link in this file.<br/>Remember that exporting other users' messages from Discord does not respect the TOS.

## exportchannel bot (Hybrid Command)
 - Usage: `?exportchannel bot <channel> [bot=True] [limit=None] `
 - Slash Usage: `/exportchannel bot <channel> [bot=True] [limit=None] `
 - Checks: `server_only`

Export part of a channel's messages to an html file.<br/><br/>Specify the bool option.<br/>Please note: all attachments and user avatars are saved with the Discord link in this file.<br/>Remember that exporting other users' messages from Discord does not respect the TOS.

## exportchannel between (Hybrid Command)
 - Usage: `?exportchannel between <channel> <before> <after> `
 - Slash Usage: `/exportchannel between <channel> <before> <after> `
 - Checks: `server_only`

Export part of a channel's messages to an html file.<br/><br/>Specify the before and after messages (id or link) or a valid snowflake.<br/>Please note: all attachments and user avatars are saved with the Discord link in this file.<br/>Remember that exporting other users' messages from Discord does not respect the TOS.

## exportchannel before (Hybrid Command)
 - Usage: `?exportchannel before <channel> <before> `
 - Slash Usage: `/exportchannel before <channel> <before> `
 - Checks: `server_only`

Export part of a channel's messages to an html file.<br/><br/>Specify the before message (id or link) or a valid snowflake.<br/>Please note: all attachments and user avatars are saved with the Discord link in this file.<br/>Remember that exporting other users' messages from Discord does not respect the TOS.

