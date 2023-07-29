# SimpleSanction Help

A cog to sanction members, with buttons!

# setsimplesanction (Hybrid Command)
 - Usage: `?setsimplesanction `
 - Slash Usage: `/setsimplesanction `
 - Restricted to: `ADMIN`
 - Aliases: `simplesanctionset`
 - Checks: `server_only`

Configure SimpleSanction for your server.

## setsimplesanction showsettings (Hybrid Command)
 - Usage: `?setsimplesanction showsettings [with_dev=False] `
 - Slash Usage: `/setsimplesanction showsettings [with_dev=False] `
 - Checks: `server_only`

Show all settings for the cog with defaults and values.

## setsimplesanction showauthor (Hybrid Command)
 - Usage: `?setsimplesanction showauthor <value> `
 - Slash Usage: `/setsimplesanction showauthor <value> `
 - Checks: `server_only`

Show the command author in embeds.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setsimplesanction actionconfirmation (Hybrid Command)
 - Usage: `?setsimplesanction actionconfirmation <value> `
 - Slash Usage: `/setsimplesanction actionconfirmation <value> `
 - Checks: `server_only`

Require a confirmation for each sanction (except userinfo).<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setsimplesanction finishmessage (Hybrid Command)
 - Usage: `?setsimplesanction finishmessage <value> `
 - Slash Usage: `/setsimplesanction finishmessage <value> `
 - Checks: `server_only`

Send an embed after a sanction command execution.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setsimplesanction modalconfig (Hybrid Command)
 - Usage: `?setsimplesanction modalconfig [confirmation=False] `
 - Slash Usage: `/setsimplesanction modalconfig [confirmation=False] `
 - Aliases: `configmodal`
 - Checks: `server_only`

Set all settings for the cog with a Discord Modal.

## setsimplesanction usewarnsystem (Hybrid Command)
 - Usage: `?setsimplesanction usewarnsystem <value> `
 - Slash Usage: `/setsimplesanction usewarnsystem <value> `
 - Checks: `server_only`

Use WarnSystem by Laggron for the sanctions.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setsimplesanction resetsetting (Hybrid Command)
 - Usage: `?setsimplesanction resetsetting <setting> `
 - Slash Usage: `/setsimplesanction resetsetting <setting> `
 - Checks: `server_only`

Reset a setting.

## setsimplesanction thumbnail (Hybrid Command)
 - Usage: `?setsimplesanction thumbnail <value> `
 - Slash Usage: `/setsimplesanction thumbnail <value> `
 - Checks: `server_only`

Set the embed thumbnail.<br/><br/>Default value: https://i.imgur.com/Bl62rGd.png<br/>Dev: <class 'str'>

## setsimplesanction reasonrequired (Hybrid Command)
 - Usage: `?setsimplesanction reasonrequired <value> `
 - Slash Usage: `/setsimplesanction reasonrequired <value> `
 - Checks: `server_only`

Require a reason for each sanction (except userinfo).<br/><br/>Default value: True<br/>Dev: <class 'bool'>

# sanction (Hybrid Command)
 - Usage: `?sanction [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Slash Usage: `/sanction [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Restricted to: `MOD`
 - Aliases: `punishmember and punishuser`
 - Checks: `server_only`

Sanction a member quickly and easily.<br/><br/>All arguments are optional and will be requested during the action if necessary. You must specify the parameters in this order.<br/><br/>Parameters:<br/>- `user`: Server member.                            Who is the user concerned?<br/>- `confirmation`: True or False.                Confirm the action directly. (Default is the recorded value)<br/>- `show_author`: True or False.                 Do you want the bot to show in its embeds who is the author of the command/sanction? (Default is the recorded value)<br/>- `finish_message`: True or False.              Do you want the bot to show an embed just before the action summarising the action and giving the sanctioned user and the reason? (Default is the recorded value)<br/>- `fake_action`: True or False.             Do you want the command to do everything as usual, but (unintentionally) forget to execute the action?<br/>- `duration`: Duration. (5d, 8h, 1m...) If you choose a TempBan, TempMute or TempMuteChanne, this value will be used for the duration of that action.<br/>- `reason`: Text.                                       The reason for this action. (`not` to not specify one, unless the reason has been made falcutative in the parameters)<br/><br/>Short version: ?sanction<br/>Long version:  ?sanction 10 @member true true true true true true 3d Spam.

## sanction 06 (Hybrid Command)
 - Usage: `?sanction 06 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Slash Usage: `/sanction 06 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Aliases: `6 and kick`

 - 👢 Kick a member from this server.<br/><br/>Examples:<br/>- `?sanction 6 @member not`: Kick for no reason.<br/>- `?sanction 6 @member Insults`: Kick for the reason "Insults".<br/>- `?sanction 6 012345678987654321 Advertising`: Kick the user with the ID provided.

## sanction 07 (Hybrid Command)
 - Usage: `?sanction 07 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Slash Usage: `/sanction 07 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Aliases: `7 and mute`

 - 🔇 Mute a member in all channels, including voice channels.<br/><br/>Examples:<br/>- `?sanction 7 @member not`: Infinite mute for no reason.<br/>- `?sanction 7 @member Spam`:Infinite  mute for the reason "Spam".<br/>- `?sanction 7 @member Advertising`: Infinite mute for the reason "Advertising".

## sanction 09 (Hybrid Command)
 - Usage: `?sanction 09 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Slash Usage: `/sanction 09 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Aliases: `9 and tempmute`

 - ⏳ TempMute a member in all channels, including voice channels.<br/><br/>You can set a timed mute by providing a valid time before the reason.<br/><br/>Examples:<br/>- `?sanction 9 @member 30m not`: 30 minutes mute for no reason.<br/>- `?sanction 9 @member 5h Spam`: 5 hours mute for the reason "Spam".<br/>- `?sanction 9 @member 3d Advertising`: 3 days mute for the reason "Advertising".

## sanction 05 (Hybrid Command)
 - Usage: `?sanction 05 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Slash Usage: `/sanction 05 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Aliases: `5 and tempban`

 - 💨 TempBan a member from this server.<br/><br/>It won't delete messages by default.<br/>If you want to perform a temporary ban, provide the time before the reason.<br/><br/>Examples:<br/>- `?sanction 5 @member not`: Ban for no reason.<br/>- `?sanction 5 @member 7d Insults`: 7 days ban for the reason "Insults".<br/>- `?sanction 5 012345678987654321 Advertising`: Ban the user with the ID provided.

## sanction 08 (Hybrid Command)
 - Usage: `?sanction 08 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Slash Usage: `/sanction 08 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Aliases: `8 and mutechannel`

 - 👊 Mute a member in this channel.<br/><br/>Examples:<br/>- `?sanction 8 @member not`: Infinite mute for no reason.<br/>- `?sanction 8 @member Spam`: Infinite mute for the reason "Spam".<br/>- `?sanction 8 @member Advertising`: Infinite mute for the reason "Advertising".

## sanction 01 (Hybrid Command)
 - Usage: `?sanction 01 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Slash Usage: `/sanction 01 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Aliases: `1, userinfo, memberinfo, and info`

 - ℹ️ Show informations about a member.<br/><br/>Examples:<br/>- `?sanction 1 @member`: UserInfo for no reason.<br/>- `?sanction 1 @member What are these roles?`: UserInfo for the reason "What are these roles?".<br/>- `?sanction 1 012345678987654321`: UserInfo with the ID provided.

## sanction 00 (Hybrid Command)
 - Usage: `?sanction 00 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Slash Usage: `/sanction 00 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Aliases: `0 and sanction`

- Sanction a member quickly and easily.<br/><br/>Examples:<br/>- `?sanction 0 @member`<br/>- `?sanction 0 @member What are these roles?`<br/>- `?sanction 0 012345678987654321`

## sanction 10 (Hybrid Command)
 - Usage: `?sanction 10 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Slash Usage: `/sanction 10 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Aliases: `tempmutechannel`

 - ⌛ TempMute a member in this channel.<br/><br/>You can set a timed mute by providing a valid time before the reason.<br/><br/>Examples:<br/>- `?sanction 10 @member 30m not`: 30 minutes mute for no reason.<br/>- `?sanction 10 @member 5h Spam`: 5 hours mute for the reason "Spam".<br/>- `?sanction 10 @member 3d Advertising`: 3 days mute for the reason "Advertising".

## sanction 03 (Hybrid Command)
 - Usage: `?sanction 03 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Slash Usage: `/sanction 03 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Aliases: `3 and ban`

 - 🔨 Ban a member from this server.<br/><br/>It won't delete messages by default.<br/><br/>Examples:<br/>- `?sanction 3 @member not`: Ban for no reason.<br/>- `?sanction 3 @member Insults`: Ban for the reason "Insults".<br/>- `?sanction 3 012345678987654321 Advertising`: Ban the user with the ID provided.

## sanction 04 (Hybrid Command)
 - Usage: `?sanction 04 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Slash Usage: `/sanction 04 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [reason] `
 - Aliases: `4 and softban`

 - 🔂 SoftBan a member from this server.<br/><br/>This means that the user will be banned and immediately unbanned, so it will purge their messages in a period, in all channels.<br/><br/>Examples:<br/>- `?sanction 4 @member not`: SoftBan for no reason<br/>- `?sanction 4 @member Insults`: SoftBan for the reason "Insults"<br/>- `?sanction 4 012345678987654321 Advertising`: SoftBan the user with the ID provided.

## sanction 02 (Hybrid Command)
 - Usage: `?sanction 02 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Slash Usage: `/sanction 02 [member=None] [confirmation=None] [show_author=None] [finish_message=None] [fake_action=False] [duration_for_mute_or_ban=None] [reason] `
 - Aliases: `2 and warn`

 - ⚠️ Add a simple warning on a member.<br/><br/>Examples:<br/>- `?sanction 2 @member not`: Warn for no reason.<br/>- `?sanction 2 @member Insults`: Warn for the reason "Insults".<br/>- `?sanction 2 012345678987654321 Advertising`: Warn the user with the ID provided.

