# InfoChannel Help

Create a channel with updating server info<br/><br/>This relies on editing channels, which is a strictly rate-limited activity.<br/>As such, updates will not be frequent. Currently capped at 1 per 5 minutes per server.

# infochannel
 - Usage: `?infochannel `
 - Restricted to: `ADMIN`

Toggle info channel for this server

# infochannelset
 - Usage: `?infochannelset `
 - Restricted to: `ADMIN`
 - Aliases: `icset`

Toggle different types of infochannels

## infochannelset togglerole
 - Usage: `?infochannelset togglerole <role> [enabled=None] `

Toggle an infochannel that shows the count of users with the specified role

## infochannelset name
 - Usage: `?infochannelset name <channel_type> [text] `

Change the name of the infochannel for the specified channel type.<br/><br/>{count} must be used to display number of total members in the server.<br/>Leave blank to set back to default.<br/><br/>Examples:<br/>- `?infochannelset name members Cool Cats: {count}`<br/>- `?infochannelset name bots {count} Robot Overlords`<br/><br/>Valid Types are:<br/>- `members`: Total members on the server<br/>- `humans`: Total members that aren't bots<br/>- `boosters`: Total amount of boosters<br/>- `bots`: Total bots<br/>- `roles`: Total number of roles<br/>- `channels`: Total number of channels excluding infochannels<br/>- `online`: Total online members<br/>- `offline`: Total offline members<br/><br/>Warning: This command counts against the channel update rate limit and may be queued.

## infochannelset rolename
 - Usage: `?infochannelset rolename <role> [text] `

Change the name of the infochannel for specific roles.<br/><br/>{count} must be used to display number members with the given role.<br/>{role} can be used for the roles name.<br/>Leave blank to set back to default.<br/><br/>Default is set to: `{role}: {count}`<br/><br/>Examples:<br/>- `?infochannelset rolename @Patrons {role}: {count}`<br/>- `?infochannelset rolename Elite {count} members with {role} role`<br/>- `?infochannelset rolename "Space Role" Total boosters: {count}`<br/><br/>Warning: This command counts against the channel update rate limit and may be queued.

## infochannelset togglechannel
 - Usage: `?infochannelset togglechannel <channel_type> [enabled=None] `

Toggles the infochannel for the specified channel type.<br/><br/>Valid Types are:<br/>- `members`: Total members on the server<br/>- `humans`: Total members that aren't bots<br/>- `boosters`: Total amount of boosters<br/>- `bots`: Total bots<br/>- `roles`: Total number of roles<br/>- `channels`: Total number of channels excluding infochannels,<br/>- `online`: Total online members,<br/>- `offline`: Total offline members,

