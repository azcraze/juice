# Defender Help

Security tools to protect communities

# dset
 - Usage: `?dset `
 - Restricted to: `ADMIN`
 - Aliases: `defset`
 - Checks: `server_only`

Defender system settings

## dset voteout
 - Usage: `?dset voteout `
 - Restricted to: `ADMIN`

Voteout manual module configuration<br/><br/>See ?defender status for more information about this module

### dset voteout action
 - Usage: `?dset voteout action <action> `

Sets action (ban, kick, softban, punish)

### dset voteout rank
 - Usage: `?dset voteout rank <rank> `

Sets target rank

### dset voteout votes
 - Usage: `?dset voteout votes <votes> `

Sets required votes number for it to pass

### dset voteout wipe
 - Usage: `?dset voteout wipe <days> `

Sets how many days worth of messages to delete if the action is ban<br/><br/>Setting 0 will not delete any message

### dset voteout enable
 - Usage: `?dset voteout enable <on_or_off> `

Toggles voteout

## dset general
 - Usage: `?dset general `
 - Restricted to: `ADMIN`

Defender general settings

### dset general enable
 - Usage: `?dset general enable <on_or_off> `

Toggle defender system

### dset general punishrole
 - Usage: `?dset general punishrole <role> `

Sets the role that will be assigned to misbehaving users<br/><br/>Note: this will only be assigned if the 'action' of a module<br/>is set to 'punish'.

### dset general notifyrole
 - Usage: `?dset general notifyrole <role> `

Sets the role that will be pinged in case of alerts

### dset general notifychannel
 - Usage: `?dset general notifychannel <channel> `

Sets the channel where notifications will be sent<br/><br/>This channel should preferably be staff readable only as it could<br/>potentially contain sensitive info

### dset general trustedroles
 - Usage: `?dset general trustedroles <roles> `

Sets the trusted roles<br/><br/>Users belonging to this role will be classified as Rank 1

### dset general messagecachecap
 - Usage: `?dset general messagecachecap <messages> `
 - Restricted to: `BOT_OWNER`

Sets the maximum # of messages to cache for each user / channel

### dset general helperroles
 - Usage: `?dset general helperroles <roles> `

Sets the helper roles<br/><br/>See ?defender status for more information about these roles

### dset general messagecacheexpire
 - Usage: `?dset general messagecacheexpire <hours> `
 - Restricted to: `BOT_OWNER`

Sets how long a message should be cached before being discarded

### dset general reset
 - Usage: `?dset general reset [confirmation=False] `

Resets Defender configuration for this server

### dset general countmessages
 - Usage: `?dset general countmessages <on_or_off> `

Toggles message count (and rank 4)

### dset general punishmessage
 - Usage: `?dset general punishmessage <message> `

Sets the messages that I will send after assigning the punish role<br/><br/>Supports context variables. You can add the following to your message:<br/>$user -> User's name + tag<br/>$user_name -> User's name<br/>$user_display -> User's nickname if set or user's name<br/>$user_id -> User's id<br/>$user_mention -> User's mention<br/>$user_nickname -> User's nickname if set or 'None'

## dset invitefilter
 - Usage: `?dset invitefilter `
 - Restricted to: `ADMIN`
 - Aliases: `if`

Invite filter auto module configuration<br/><br/>See ?defender status for more information about this module

### dset invitefilter enable
 - Usage: `?dset invitefilter enable <on_or_off> `

Toggle invite filter

### dset invitefilter rank
 - Usage: `?dset invitefilter rank <rank> `

Sets target rank

### dset invitefilter wdchecks
 - Usage: `?dset invitefilter wdchecks [conditions] `

Implement advanced Warden based checks<br/><br/>Issuing this command with no arguments will show the current checks<br/>Passing 'remove' will remove existing checks

### dset invitefilter deletemessage
 - Usage: `?dset invitefilter deletemessage <on_or_off> `

Toggles whether to delete the invite's message

### dset invitefilter excludeowninvites
 - Usage: `?dset invitefilter excludeowninvites <yes_or_no> `

Excludes this server's invites from the filter

### dset invitefilter action
 - Usage: `?dset invitefilter action <action> `

Sets action (ban, kick, softban, punish or none (deletion only))

## dset warden
 - Usage: `?dset warden `
 - Restricted to: `ADMIN`
 - Aliases: `wd`

Warden auto module configuration<br/><br/>See ?defender status for more information about this module

### dset warden uploadmaxsize
 - Usage: `?dset warden uploadmaxsize <kilobytes> `
 - Restricted to: `BOT_OWNER`

Sets the maximum allowed size for Warden rules upload<br/><br/>Reccommended size is 3KB

### dset warden periodicallowed
 - Usage: `?dset warden periodicallowed <on_or_off> `
 - Restricted to: `BOT_OWNER`

Toggles the ability to globally create periodic rules<br/><br/>Periodic rules are rules that can be scheduled to run against<br/>an entire server userbase on an interval between 5 minutes and 24 hours

### dset warden regexsafetychecks
 - Usage: `?dset warden regexsafetychecks <on_or_off> `
 - Restricted to: `BOT_OWNER`

Globally toggles the safety checks for user defined regex<br/><br/>These checks disable Warden rules with regex that takes too long to be evaluated. It is<br/>recommended to keep this feature enabled.

### dset warden regexallowed
 - Usage: `?dset warden regexallowed <on_or_off> `
 - Restricted to: `BOT_OWNER`

Toggles the ability to globally create rules with user defined regex

### dset warden enable
 - Usage: `?dset warden enable <on_or_off> `

Toggles warden

## dset vaporize
 - Usage: `?dset vaporize `
 - Restricted to: `ADMIN`

Vaporize manual module configuration<br/><br/>See ?defender status for more information about this module

### dset vaporize enable
 - Usage: `?dset vaporize enable <on_or_off> `

Toggle vaporize manual module

### dset vaporize maxtargets
 - Usage: `?dset vaporize maxtargets <max_targets> `

Sets the maximum amount of targets (1-999)<br/><br/>By default only a maximum of 15 users can be vaporized at once

## dset joinmonitor
 - Usage: `?dset joinmonitor `
 - Restricted to: `ADMIN`
 - Aliases: `jm`

Join monitor auto module configuration<br/><br/>See ?defender status for more information about this module

### dset joinmonitor enable
 - Usage: `?dset joinmonitor enable <on_or_off> `

Toggles join monitor

### dset joinmonitor minutes
 - Usage: `?dset joinmonitor minutes <minutes> `

Sets minutes (X users joined in Y minutes)

### dset joinmonitor wdchecks
 - Usage: `?dset joinmonitor wdchecks [conditions] `

Implement advanced Warden based checks<br/><br/>Issuing this command with no arguments will show the current checks<br/>Passing 'remove' will remove existing checks

### dset joinmonitor verificationlevel
 - Usage: `?dset joinmonitor verificationlevel `

Raises the server's verification level on raids<br/><br/>You can find a full description of Discord's verification levels in<br/>the server's settings "Moderation" tab.<br/><br/>Verification levels:<br/>0 - No action<br/>1 - Low: verified email<br/>2 - Medium: must be registered for longer than 5 minutes<br/>3 - High: must be a member of this server for longer than 10 minutes<br/>4 - Highest: must have a verified phone on their Discord account

### dset joinmonitor notifynew
 - Usage: `?dset joinmonitor notifynew <hours> `

Enables notifications for users younger than X hours<br/><br/>Use 0 hours to disable notifications

### dset joinmonitor users
 - Usage: `?dset joinmonitor users <users> `

Sets users (X users joined in Y minutes)

## dset silence
 - Usage: `?dset silence `
 - Restricted to: `ADMIN`

Silence manual module configuration<br/><br/>See ?defender status for more information about this module

### dset silence enable
 - Usage: `?dset silence enable <on_or_off> `

Toggle silence manual module

## dset rank3
 - Usage: `?dset rank3 `
 - Restricted to: `ADMIN`

Rank 3 configuration<br/><br/>See ?defender status for more information about this rank

### dset rank3 minmessages
 - Usage: `?dset rank3 minmessages <messages> `

Minimum messages required to reach Rank 3

### dset rank3 joineddays
 - Usage: `?dset rank3 joineddays <days> `

Days since join required to be considered Rank 3

## dset commentanalysis
 - Usage: `?dset commentanalysis `
 - Restricted to: `ADMIN`
 - Aliases: `ca`

Comment analysis configuration<br/><br/>See ?defender status for more information about this module

### dset commentanalysis deletemessage
 - Usage: `?dset commentanalysis deletemessage <on_or_off> `

Toggles whether to delete the offending message

### dset commentanalysis token
 - Usage: `?dset commentanalysis token <token> `

Sets Perspective API token<br/><br/>https://developers.perspectiveapi.com/s/docs

### dset commentanalysis wipe
 - Usage: `?dset commentanalysis wipe <days> `

Sets how many days worth of messages to delete if the action is ban<br/><br/>Setting 0 will not delete any message

### dset commentanalysis enable
 - Usage: `?dset commentanalysis enable <on_or_off> `

Toggles comment analysis

### dset commentanalysis reason
 - Usage: `?dset commentanalysis reason <reason> `

Sets a reason for the action (modlog use)

### dset commentanalysis action
 - Usage: `?dset commentanalysis action <action> `

Sets action (ban, kick, softban, punish or none (notification only))

### dset commentanalysis rank
 - Usage: `?dset commentanalysis rank <rank> `

Sets target rank

### dset commentanalysis threshold
 - Usage: `?dset commentanalysis threshold <threshold> `

Sets the threshold that will trigger CA's action (20-100)

### dset commentanalysis attributes
 - Usage: `?dset commentanalysis attributes `

Setup the attributes that CA will check

### dset commentanalysis wdchecks
 - Usage: `?dset commentanalysis wdchecks [conditions] `

Implement advanced Warden based checks<br/><br/>Issuing this command with no arguments will show the current checks<br/>Passing 'remove' will remove existing checks

## dset emergency
 - Usage: `?dset emergency `
 - Restricted to: `ADMIN`

Emergency mode configuration<br/><br/>See ?defender status for more information about emergency mode

### dset emergency minutes
 - Usage: `?dset emergency minutes <minutes> `

Sets max inactivity minutes for staff<br/><br/>After X minutes of inactivity following an alert emergency<br/>mode will be engaged and helper roles will be able to use<br/>the emergency modules.

### dset emergency modules
 - Usage: `?dset emergency modules `

Sets emergency modules<br/><br/>Emergency modules will be rendered available to helper roles<br/>during emergency mode. Selecting no modules to this command will<br/>disable emergency mode.<br/>Available emergency modules: voteout, vaporize, silence

## dset importfrom
 - Usage: `?dset importfrom <server> `

Import the configuration from another server<br/><br/>This is permitted only if the command issuer is admin in both servers

## dset alert
 - Usage: `?dset alert `
 - Restricted to: `ADMIN`

Alert manual module configuration<br/><br/>See ?defender status for more information about this module

### dset alert enable
 - Usage: `?dset alert enable <on_or_off> `

Toggle alert manual module

## dset raiderdetection
 - Usage: `?dset raiderdetection `
 - Restricted to: `ADMIN`
 - Aliases: `rd`

Raider detection auto module configuration<br/><br/>See ?defender status for more information about this module

### dset raiderdetection action
 - Usage: `?dset raiderdetection action <action> `

Sets action (ban, kick, softban, punish or none (notify only))

### dset raiderdetection rank
 - Usage: `?dset raiderdetection rank <rank> `

Sets target rank

### dset raiderdetection minutes
 - Usage: `?dset raiderdetection minutes <minutes> `

Sets minutes (User posted X messages in Y minutes)

### dset raiderdetection enable
 - Usage: `?dset raiderdetection enable <on_or_off> `

Toggles raider detection

### dset raiderdetection messages
 - Usage: `?dset raiderdetection messages <messages> `

Sets messages (User posted X messages in Y minutes)

### dset raiderdetection wdchecks
 - Usage: `?dset raiderdetection wdchecks [conditions] `

Implement advanced Warden based checks<br/><br/>Issuing this command with no arguments will show the current checks<br/>Passing 'remove' will remove existing checks

### dset raiderdetection wipe
 - Usage: `?dset raiderdetection wipe <days> `

Sets how many days worth of messages to delete if the action is ban<br/><br/>Setting 0 will not delete any message

# defender
 - Usage: `?defender `
 - Restricted to: `MOD`
 - Aliases: `def`
 - Checks: `server_only`

Defender commands reserved to staff

## defender freshmeat
 - Usage: `?defender freshmeat [hours=24] [keywords] `

Returns a list of the new users of the day<br/><br/>Can be filtered. Supports wildcards (* and ?)

## defender identify
 - Usage: `?defender identify <user> `

Shows a member's rank + info

## defender notifynew
 - Usage: `?defender notifynew <hours> `

Sends you a DM if a user younger than X hours joins<br/><br/>Use 0 hours to disable notifications

## defender memberranks
 - Usage: `?defender memberranks `

Counts how many members are in each rank

## defender monitor
 - Usage: `?defender monitor [keywords] `

Shows recent events that might require your attention<br/><br/>Can be filtered. Supports wildcards (* and ?)

## defender messages
 - Usage: `?defender messages `
 - Aliases: `msg`

Access recorded messages of users / channels

### defender messages exportchannel
 - Usage: `?defender messages exportchannel <channel> `

Exports recent messages of a channel to a file

### defender messages channel
 - Usage: `?defender messages channel <channel> `

Shows recent messages of a channel

### defender messages user
 - Usage: `?defender messages user <user> `

Shows recent messages of a user

### defender messages exportuser
 - Usage: `?defender messages exportuser <user> `

Exports recent messages of a user to a file

## defender status
 - Usage: `?defender status `

Shows overall status of the Defender system

## defender updates
 - Usage: `?defender updates `

Shows all the past announcements of Defender

## defender emergency
 - Usage: `?defender emergency <on_or_off> `

Manually engage or turn off emergency mode<br/><br/>Upon activation, staff will be pinged and any module<br/>that is set to be active in emergency mode will be rendered<br/>available to helpers

## defender debuginfo
 - Usage: `?defender debuginfo `
 - Restricted to: `BOT_OWNER`

Debug info about Defender and its dependencies

## defender warden
 - Usage: `?defender warden `
 - Restricted to: `ADMIN`
 - Aliases: `wd`

Warden rules management<br/><br/>See ?defender status for more information about Warden

### defender warden export
 - Usage: `?defender warden export <name> `

Sends the rule as a YAML file

### defender warden find
 - Usage: `?defender warden find <text> `
 - Aliases: `search`

Search for text in existing rules

### defender warden upload
 - Usage: `?defender warden upload `
 - Cooldown: `1 per 86400.0 seconds`

Starts a rule upload session

### defender warden debug
 - Usage: `?defender warden debug <_id> <event> [rank=None] `

Simulate and give a detailed summary of an event<br/><br/>A Warden event must be passed with the proper target ID (user or local message)<br/><br/>When this command is issued all the rules registered to the event will be<br/>processed in a safe way against the target, if any.<br/>If the target satisfies the conditions, *only* the heatpoint related actions<br/>will be carried on.<br/>The heatpoint actions will be "sandboxed", so the newly added heatpoints won't<br/>have any effect outside this test.<br/>Remember that Warden evaluates each condition in order and stops at the first failed<br/>root condition: the last condition that is listed in a failed rule is where Warden<br/>stopped evaluating them.<br/>If a valid Rank is also passed it will be used in place of the target's real<br/>rank during the test.<br/>See the documentation for a full list of Warden events.<br/><br/>Example:<br/>?def warden debug <valid_user_id> on-user-join<br/>?def warden debug <valid_message_id> on-message<br/>?def warden debug <valid_message_id> on-message-edit 3

### defender warden show
 - Usage: `?defender warden show <name> `

Shows a rule

### defender warden list
 - Usage: `?defender warden list `

Lists existing rules

### defender warden add
 - Usage: `?defender warden add <rule> `

Adds a new rule

### defender warden exportall
 - Usage: `?defender warden exportall `

Sends all the rules as a tar.gz archive

### defender warden removeall
 - Usage: `?defender warden removeall `

Removes all rules

### defender warden run
 - Usage: `?defender warden run <name> `

Runs a rule against the whole userbase<br/><br/>Confirmation is asked before execution.

### defender warden remove
 - Usage: `?defender warden remove <name> `

Removes a rule by name

### defender warden memory
 - Usage: `?defender warden memory [keywords] `

Shows or resets the memory of Warden<br/><br/>Can be filtered. Supports wildcards (* and ?)

# alert
 - Usage: `?alert `
 - Aliases: `staff`
 - Cooldown: `1 per 120.0 seconds`
 - Checks: `server_only`

Alert the staff members

# vaporize
 - Usage: `?vaporize <members> `
 - Checks: `server_only`

Gets rid of bad actors in a quick and silent way<br/><br/>Works only on Rank 3 and under

# voteout
 - Usage: `?voteout <user> `
 - Cooldown: `1 per 22.0 seconds`
 - Checks: `server_only`

Initiates a vote to expel a user from the server<br/><br/>Can be used by members with helper roles during emergency mode

# silence
 - Usage: `?silence <rank> `
 - Checks: `server_only`

Enables server wide message autodeletion for the specified rank (and below)<br/><br/>Passing 0 will disable this.

