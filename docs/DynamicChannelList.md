# DynamicChannelList Help

Create dynamically updating channel lists.

# dynamicchannellist
 - Usage: `?dynamicchannellist `
 - Restricted to: `MOD`
 - Aliases: `dcl`

Group command for DynamicChannelList.

## dynamicchannellist createauto
 - Usage: `?dynamicchannellist createauto [channel=None] [ignoreBlacklist=False] [role=None] `

Create an automatically updating channel list.

## dynamicchannellist reloadauto
 - Usage: `?dynamicchannellist reloadauto `

Reload all automatically updating channel lists.

## dynamicchannellist color
 - Usage: `?dynamicchannellist color <color> `

Set the color to use for embeds.

## dynamicchannellist channelblacklist
 - Usage: `?dynamicchannellist channelblacklist [chan=None] `
 - Aliases: `channelignore`

Toggle if a channel is blacklisted from appearing on channel lists.<br/><br/>If no channel is provided, the currently blacklisted categories will be listed.

## dynamicchannellist removeauto
 - Usage: `?dynamicchannellist removeauto <message> `

Remove an automatically updating channel list.<br/><br/>This will not delete the message, only stop it from updating.<br/>`message` should be a link to the message.

## dynamicchannellist categoryblacklist
 - Usage: `?dynamicchannellist categoryblacklist [cat=None] `
 - Aliases: `categoryignore`

Toggle if a category is blacklisted from appearing on channel lists.<br/><br/>If no category is provided, the currently blacklisted categories will be listed.

## dynamicchannellist generate
 - Usage: `?dynamicchannellist generate [channel=None] [ignoreBlacklist=False] [role=None] `

Generate a one-time channel list.

## dynamicchannellist header
 - Usage: `?dynamicchannellist header [text] `

Set the header for all embed messages.

