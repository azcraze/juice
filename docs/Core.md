# Core Help

The Core cog has many commands related to core functions.<br/><br/>These commands come loaded with every Red bot, and cover some of the most basic usage of the bot.

# ping
 - Usage: `?ping `

Pong.

# info
 - Usage: `?info `

Shows info about JuiceBot.

# uptime
 - Usage: `?uptime `

Shows JuiceBot's uptime.

# mydata
 - Usage: `?mydata `

Commands which interact with the data JuiceBot has about you.<br/><br/>More information can be found in the [End User Data Documentation.](https://docs.discord.red/en/stable/red_core_data_statement.html)

## mydata whatdata
 - Usage: `?mydata whatdata `
 - Cooldown: `1 per 600.0 seconds`

Find out what type of data JuiceBot stores and why.<br/><br/>**Example:**<br/>- `?mydata whatdata`

## mydata 3rdparty
 - Usage: `?mydata 3rdparty `
 - Cooldown: `1 per 1800.0 seconds`

View the End User Data statements of each 3rd-party module.<br/><br/>This will send an attachment with the End User Data statements of all loaded 3rd party cogs.<br/><br/>**Example:**<br/>- `?mydata 3rdparty`

## mydata getmydata
 - Usage: `?mydata getmydata `
 - Cooldown: `1 per 7200.0 seconds`

[Coming Soon] Get what data JuiceBot has about you.

## mydata forgetme
 - Usage: `?mydata forgetme `
 - Cooldown: `1 per 86400.0 seconds`

Have JuiceBot forget what it knows about you.<br/><br/>This may not remove all data about you, data needed for operation,<br/>such as command cooldowns will be kept until no longer necessary.<br/><br/>Further interactions with JuiceBot may cause it to learn about you again.<br/><br/>**Example:**<br/>- `?mydata forgetme`

## mydata ownermanagement
 - Usage: `?mydata ownermanagement `
 - Restricted to: `BOT_OWNER`

Commands for more complete data handling.

### mydata ownermanagement setuserdeletionlevel
 - Usage: `?mydata ownermanagement setuserdeletionlevel <level> `

Sets how user deletions are treated.<br/><br/>**Example:**<br/>- `?mydata ownermanagement setuserdeletionlevel 1`<br/><br/>**Arguments:**<br/>- `<level>` - The strictness level for user deletion. See Level guide below.<br/><br/>Level:<br/>- `0`: What users can delete is left entirely up to each cog.<br/>- `1`: Cogs should delete anything the cog doesn't need about the user.

### mydata ownermanagement deleteuserasowner
 - Usage: `?mydata ownermanagement deleteuserasowner <user_id> `

Delete data JuiceBot has about a user.<br/><br/>This will cause the bot to get rid of or disassociate a lot of data about the specified user.<br/>This may include more than just end user data, including anti abuse records.<br/><br/>**Arguments:**<br/>- `<user_id>` - The id of the user whose data would be deleted.

### mydata ownermanagement deleteforuser
 - Usage: `?mydata ownermanagement deleteforuser <user_id> `

Delete data JuiceBot has about a user for a user.<br/><br/>This will cause the bot to get rid of or disassociate a lot of non-operational data from the specified user.<br/>Users have access to a different command for this unless they can't interact with the bot at all.<br/>This is a mostly safe operation, but you should not use it unless processing a request from this user as it may impact their usage of the bot.<br/><br/>**Arguments:**<br/>- `<user_id>` - The id of the user whose data would be deleted.

### mydata ownermanagement allowuserdeletions
 - Usage: `?mydata ownermanagement allowuserdeletions `

Set the bot to allow users to request a data deletion.<br/><br/>This is on by default.<br/>Opposite of `?mydata ownermanagement disallowuserdeletions`<br/><br/>**Example:**<br/>- `?mydata ownermanagement allowuserdeletions`

### mydata ownermanagement processdiscordrequest
 - Usage: `?mydata ownermanagement processdiscordrequest <user_id> `

Handle a deletion request from Discord.<br/><br/>This will cause the bot to get rid of or disassociate all data from the specified user ID.<br/>You should not use this unless Discord has specifically requested this with regard to a deleted user.<br/>This will remove the user from various anti-abuse measures.<br/>If you are processing a manual request from a user, you may want `?mydata ownermanagement deleteforuser` instead.<br/><br/>**Arguments:**<br/>- `<user_id>` - The id of the user whose data would be deleted.

### mydata ownermanagement disallowuserdeletions
 - Usage: `?mydata ownermanagement disallowuserdeletions `

Set the bot to not allow users to request a data deletion.<br/><br/>Opposite of `?mydata ownermanagement allowuserdeletions`<br/><br/>**Example:**<br/>- `?mydata ownermanagement disallowuserdeletions`

# embedset
 - Usage: `?embedset `

Commands for toggling embeds on or off.<br/><br/>This setting determines whether or not to use embeds as a response to a command (for commands that support it).<br/>The default is to use embeds.<br/><br/>The embed settings are checked until the first True/False in this order:<br/><br/>- In server context:<br/>  1. Channel override - `?embedset channel`<br/>  2. Server command override - `?embedset command server`<br/>  3. Server override - `?embedset server`<br/>  4. Global command override - `?embedset command global`<br/>  5. Global setting  -`?embedset global`<br/><br/>- In DM context:<br/>  1. User override - `?embedset user`<br/>  2. Global command override - `?embedset command global`<br/>  3. Global setting - `?embedset global`

## embedset showsettings
 - Usage: `?embedset showsettings [command=None] `

Show the current embed settings.<br/><br/>Provide a command name to check for command specific embed settings.<br/><br/>**Examples:**<br/>- `?embedset showsettings` - Shows embed settings.<br/>- `?embedset showsettings info` - Also shows embed settings for the 'info' command.<br/>- `?embedset showsettings "ignore list"` - Checking subcommands requires quotes.<br/><br/>**Arguments:**<br/>- `[command]` - Checks this command for command specific embed settings.

## embedset channel
 - Usage: `?embedset channel <channel> [enabled=None] `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Set's a channel's embed setting.<br/><br/>If set, this is used instead of the server and command defaults to determine whether or not to use embeds.<br/>This is used for all commands done in a channel.<br/><br/>If enabled is left blank, the setting will be unset and the server default will be used instead.<br/><br/>To see full evaluation order of embed settings, run `?help embedset`.<br/><br/>**Examples:**<br/>- `?embedset channel #text-channel False` - Disables embeds in the #text-channel.<br/>- `?embedset channel #forum-channel disable` - Disables embeds in the #forum-channel.<br/>- `?embedset channel #text-channel` - Resets value to use server default in the #text-channel.<br/><br/>**Arguments:**<br/>    - `<channel>` - The text, voice, stage, or forum channel to set embed setting for.<br/>    - `[enabled]` - Whether to use embeds in this channel. Leave blank to reset to default.

## embedset user
 - Usage: `?embedset user [enabled=None] `

Sets personal embed setting for DMs.<br/><br/>If set, this is used instead of the global default to determine whether or not to use embeds.<br/>This is used for all commands executed in a DM with the bot.<br/><br/>If enabled is left blank, the setting will be unset and the global default will be used instead.<br/><br/>To see full evaluation order of embed settings, run `?help embedset`.<br/><br/>**Examples:**<br/>- `?embedset user False` - Disables embeds in your DMs.<br/>- `?embedset user` - Resets value to use global default.<br/><br/>**Arguments:**<br/>- `[enabled]` - Whether to use embeds in your DMs. Leave blank to reset to default.

## embedset server
 - Usage: `?embedset server [enabled=None] `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `server`
 - Checks: `server_only`

Set the server's embed setting.<br/><br/>If set, this is used instead of the global default to determine whether or not to use embeds.<br/>This is used for all commands done in a server.<br/><br/>If enabled is left blank, the setting will be unset and the global default will be used instead.<br/><br/>To see full evaluation order of embed settings, run `?help embedset`.<br/><br/>**Examples:**<br/>- `?embedset server False` - Disables embeds on this server.<br/>- `?embedset server` - Resets value to use global default.<br/><br/>**Arguments:**<br/>- `[enabled]` - Whether to use embeds on this server. Leave blank to reset to default.

## embedset global
 - Usage: `?embedset global `
 - Restricted to: `BOT_OWNER`

Toggle the global embed setting.<br/><br/>This is used as a fallback if the user or server hasn't set a preference.<br/>The default is to use embeds.<br/><br/>To see full evaluation order of embed settings, run `?help embedset`.<br/><br/>**Example:**<br/>- `?embedset global`

## embedset command
 - Usage: `?embedset command <command> [enabled=None] `
 - Restricted to: `GUILD_OWNER`

Sets a command's embed setting.<br/><br/>If you're the bot owner, this will try to change the command's embed setting globally by default.<br/>Otherwise, this will try to change embed settings on the current server.<br/><br/>If enabled is left blank, the setting will be unset.<br/><br/>To see full evaluation order of embed settings, run `?help embedset`.<br/><br/>**Examples:**<br/>- `?embedset command info` - Clears command specific embed settings for 'info'.<br/>- `?embedset command info False` - Disables embeds for 'info'.<br/>- `?embedset command "ignore list" True` - Quotes are needed for subcommands.<br/><br/>**Arguments:**<br/>- `[enabled]` - Whether to use embeds for this command. Leave blank to reset to default.

### embedset command server
 - Usage: `?embedset command server <command> [enabled=None] `
 - Aliases: `server`
 - Checks: `server_only`

Sets a command's embed setting for the current server.<br/><br/>If set, this is used instead of the server default to determine whether or not to use embeds.<br/><br/>If enabled is left blank, the setting will be unset and the server default will be used instead.<br/><br/>To see full evaluation order of embed settings, run `?help embedset`.<br/><br/>**Examples:**<br/>- `?embedset command server info` - Clears command specific embed settings for 'info'.<br/>- `?embedset command server info False` - Disables embeds for 'info'.<br/>- `?embedset command server "ignore list" True` - Quotes are needed for subcommands.<br/><br/>**Arguments:**<br/>- `[enabled]` - Whether to use embeds for this command. Leave blank to reset to default.

### embedset command global
 - Usage: `?embedset command global <command> [enabled=None] `
 - Restricted to: `BOT_OWNER`

Sets a command's embed setting globally.<br/><br/>If set, this is used instead of the global default to determine whether or not to use embeds.<br/><br/>If enabled is left blank, the setting will be unset.<br/><br/>To see full evaluation order of embed settings, run `?help embedset`.<br/><br/>**Examples:**<br/>- `?embedset command global info` - Clears command specific embed settings for 'info'.<br/>- `?embedset command global info False` - Disables embeds for 'info'.<br/>- `?embedset command global "ignore list" True` - Quotes are needed for subcommands.<br/><br/>**Arguments:**<br/>- `[enabled]` - Whether to use embeds for this command. Leave blank to reset to default.

# traceback
 - Usage: `?traceback [public=False] `
 - Restricted to: `BOT_OWNER`

Sends to the owner the last command exception that has occurred.<br/><br/>If public (yes is specified), it will be sent to the chat instead.<br/><br/>Warning: Sending the traceback publicly can accidentally reveal sensitive information about your computer or configuration.<br/><br/>**Examples:**<br/>- `?traceback` - Sends the traceback to your DMs.<br/>- `?traceback True` - Sends the last traceback in the current context.<br/><br/>**Arguments:**<br/>- `[public]` - Whether to send the traceback to the current context. Leave blank to send to your DMs.

# invite
 - Usage: `?invite `
 - Checks: `CoreLogic`

Shows JuiceBot's invite url.<br/><br/>This will always send the invite to DMs to keep it private.<br/><br/>This command is locked to the owner unless `?inviteset public` is set to True.<br/><br/>**Example:**<br/>- `?invite`

# inviteset
 - Usage: `?inviteset `
 - Restricted to: `BOT_OWNER`

Commands to setup JuiceBot's invite settings.

## inviteset perms
 - Usage: `?inviteset perms <level> `

Make the bot create its own role with permissions on join.<br/><br/>The bot will create its own role with the desired permissions when it joins a new server. This is a special role that can't be deleted or removed from the bot.<br/><br/>For that, you need to provide a valid permissions level.<br/>You can generate one here: https://discordapi.com/permissions.html<br/><br/>Please note that you might need two factor authentication for some permissions.<br/><br/>**Example:**<br/>- `?inviteset perms 134217728` - Adds a "Manage Nicknames" permission requirement to the invite.<br/><br/>**Arguments:**<br/>- `<level>` - The permission level to require for the bot in the generated invite.

## inviteset commandscope
 - Usage: `?inviteset commandscope `

Add the `applications.commands` scope to your invite URL.<br/><br/>This allows the usage of slash commands on the servers that invited your bot with that scope.<br/><br/>Note that previous servers that invited the bot without the scope cannot have slash commands, they will have to invite the bot a second time.

## inviteset public
 - Usage: `?inviteset public [confirm=False] `

Toggles if `?invite` should be accessible for the average user.<br/><br/>The bot must be made into a `Public bot` in the developer dashboard for public invites to work.<br/><br/>**Example:**<br/>- `?inviteset public yes` - Toggles the public invite setting.<br/><br/>**Arguments:**<br/>- `[confirm]` - Required to set to public. Not required to toggle back to private.

# leave
 - Usage: `?leave <servers> `
 - Restricted to: `BOT_OWNER`

Leaves servers.<br/><br/>If no server IDs are passed the local server will be left instead.<br/><br/>Note: This command is interactive.<br/><br/>**Examples:**<br/>- `?leave` - Leave the current server.<br/>- `?leave "Red - Discord Bot"` - Quotes are necessary when there are spaces in the name.<br/>- `?leave 133049272517001216 240154543684321280` - Leaves multiple servers, using IDs.<br/><br/>**Arguments:**<br/>- `[servers...]` - The servers to leave. When blank, attempts to leave the current server.

# servers
 - Usage: `?servers `
 - Restricted to: `BOT_OWNER`

Lists the servers JuiceBot is currently in.<br/><br/>Note: This command is interactive.

# load
 - Usage: `?load <cogs> `
 - Restricted to: `BOT_OWNER`

Loads cog packages from the local paths and installed cogs.<br/><br/>See packages available to load with `?cogs`.<br/><br/>Additional cogs can be added using Downloader, or from local paths using `?addpath`.<br/><br/>**Examples:**<br/>- `?load general` - Loads the `general` cog.<br/>- `?load admin mod mutes` - Loads multiple cogs.<br/><br/>**Arguments:**<br/>- `<cogs...>` - The cog packages to load.

# unload
 - Usage: `?unload <cogs> `
 - Restricted to: `BOT_OWNER`

Unloads previously loaded cog packages.<br/><br/>See packages available to unload with `?cogs`.<br/><br/>**Examples:**<br/>- `?unload general` - Unloads the `general` cog.<br/>- `?unload admin mod mutes` - Unloads multiple cogs.<br/><br/>**Arguments:**<br/>- `<cogs...>` - The cog packages to unload.

# reload
 - Usage: `?reload <cogs> `
 - Restricted to: `BOT_OWNER`

Reloads cog packages.<br/><br/>This will unload and then load the specified cogs.<br/><br/>Cogs that were not loaded will only be loaded.<br/><br/>**Examples:**<br/>- `?reload general` - Unloads then loads the `general` cog.<br/>- `?reload admin mod mutes` - Unloads then loads multiple cogs.<br/><br/>**Arguments:**<br/>- `<cogs...>` - The cog packages to reload.

# slash
 - Usage: `?slash `
 - Restricted to: `BOT_OWNER`

Base command for managing what application commands are able to be used on JuiceBot.

## slash enablecog
 - Usage: `?slash enablecog <cog_name> `

Marks all application commands in a cog as being enabled, allowing them to be added to the bot.<br/><br/>See a list of cogs with application commands with `?slash list`.<br/><br/>This command does NOT sync the enabled commands with Discord, that must be done manually with `?slash sync` for commands to appear in users' clients.<br/><br/>**Arguments:**<br/>    - `<cog_name>` - The cog to enable commands from. This argument is case sensitive.

## slash sync
 - Usage: `?slash sync [server=None] `
 - Cooldown: `1 per 60.0 seconds`

Syncs the slash settings to discord.<br/><br/>Settings from `?slash list` will be synced with discord, changing what commands appear for users.<br/>This should be run sparingly, make all necessary changes before running this command.<br/><br/>**Arguments:**<br/>    - `[server]` - If provided, syncs commands for that server. Otherwise, syncs global commands.

## slash list
 - Usage: `?slash list `

List the slash commands the bot can see, and whether or not they are enabled.<br/><br/>This command shows the state that will be changed to when `?slash sync` is run.<br/>Commands from the same cog are grouped, with the cog name as the header.<br/><br/>The prefix denotes the state of the command:<br/>- Commands starting with `- ` have not yet been enabled.<br/>- Commands starting with `+ ` have been manually enabled.<br/>- Commands starting with `++` have been enabled by the cog author, and cannot be disabled.

## slash disablecog
 - Usage: `?slash disablecog <cog_name> `

Marks all application commands in a cog as being disabled, preventing them from being added to the bot.<br/><br/>See a list of cogs with application commands with `?slash list`.<br/><br/>This command does NOT sync the enabled commands with Discord, that must be done manually with `?slash sync` for commands to appear in users' clients.<br/><br/>**Arguments:**<br/>    - `<cog_name>` - The cog to disable commands from. This argument is case sensitive.

## slash disable
 - Usage: `?slash disable <command_name> [command_type=slash] `

Marks an application command as being disabled, preventing it from being added to the bot.<br/><br/>See commands available to disable with `?slash list`.<br/><br/>This command does NOT sync the enabled commands with Discord, that must be done manually with `?slash sync` for commands to appear in users' clients.<br/><br/>**Arguments:**<br/>    - `<command_name>` - The command name to disable. Only the top level name of a group command should be used.<br/>    - `[command_type]` - What type of application command to disable. Must be one of `slash`, `message`, or `user`. Defaults to `slash`.

## slash enable
 - Usage: `?slash enable <command_name> [command_type=slash] `

Marks an application command as being enabled, allowing it to be added to the bot.<br/><br/>See commands available to enable with `?slash list`.<br/><br/>This command does NOT sync the enabled commands with Discord, that must be done manually with `?slash sync` for commands to appear in users' clients.<br/><br/>**Arguments:**<br/>    - `<command_name>` - The command name to enable. Only the top level name of a group command should be used.<br/>    - `[command_type]` - What type of application command to enable. Must be one of `slash`, `message`, or `user`. Defaults to `slash`.

# shutdown
 - Usage: `?shutdown [silently=False] `
 - Restricted to: `BOT_OWNER`

Shuts down the bot.<br/><br/>Allows JuiceBot to shut down gracefully.<br/><br/>This is the recommended method for shutting down the bot.<br/><br/>**Examples:**<br/>- `?shutdown`<br/>- `?shutdown True` - Shutdowns silently.<br/><br/>**Arguments:**<br/>- `[silently]` - Whether to skip sending the shutdown message. Defaults to False.

# restart
 - Usage: `?restart [silently=False] `
 - Restricted to: `BOT_OWNER`

Attempts to restart JuiceBot.<br/><br/>Makes JuiceBot quit with exit code 26.<br/>The restart is not guaranteed: it must be dealt with by the process manager in use.<br/><br/>**Examples:**<br/>- `?restart`<br/>- `?restart True` - Restarts silently.<br/><br/>**Arguments:**<br/>- `[silently]` - Whether to skip sending the restart message. Defaults to False.

# bankset
 - Usage: `?bankset `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Base command for bank settings.

## bankset registeramount
 - Usage: `?bankset registeramount <creds> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Set the initial balance for new bank accounts.<br/><br/>Example:<br/>- `?bankset registeramount 5000`<br/><br/>**Arguments**<br/><br/>- `<creds>` The new initial balance amount. Default is 0.

## bankset reset
 - Usage: `?bankset reset [confirmation=False] `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Delete all bank accounts.<br/><br/>Examples:<br/>- `?bankset reset` - Did not confirm. Shows the help message.<br/>- `?bankset reset yes`<br/><br/>**Arguments**<br/><br/>- `<confirmation>` This will default to false unless specified.

## bankset prune
 - Usage: `?bankset prune `
 - Restricted to: `ADMIN`
 - Checks: `is_owner_if_bank_global`

Base command for pruning bank accounts.

### bankset prune user
 - Usage: `?bankset prune user <member_or_id> [confirmation=False] `

Delete the bank account of a specified user.<br/><br/>Examples:<br/>- `?bankset prune user @Twentysix` - Did not confirm. Shows the help message.<br/>- `?bankset prune user @Twentysix yes`<br/><br/>**Arguments**<br/><br/>- `<user>` The user to delete the bank of. Takes mentions, names, and user ids.<br/>- `<confirmation>` This will default to false unless specified.

### bankset prune server
 - Usage: `?bankset prune server [confirmation=False] `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `server and local`
 - Checks: `server_only`

Prune bank accounts for users no longer in the server.<br/><br/>Cannot be used with a global bank. See `?bankset prune global`.<br/><br/>Examples:<br/>- `?bankset prune server` - Did not confirm. Shows the help message.<br/>- `?bankset prune server yes`<br/><br/>**Arguments**<br/><br/>- `<confirmation>` This will default to false unless specified.

### bankset prune global
 - Usage: `?bankset prune global [confirmation=False] `
 - Restricted to: `BOT_OWNER`

Prune bank accounts for users who no longer share a server with the bot.<br/><br/>Cannot be used without a global bank. See `?bankset prune server`.<br/><br/>Examples:<br/>- `?bankset prune global` - Did not confirm. Shows the help message.<br/>- `?bankset prune global yes`<br/><br/>**Arguments**<br/><br/>- `<confirmation>` This will default to false unless specified.

## bankset maxbal
 - Usage: `?bankset maxbal <amount> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Set the maximum balance a user can get.

## bankset showsettings
 - Usage: `?bankset showsettings `

Show the current bank settings.

## bankset bankname
 - Usage: `?bankset bankname <name> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Set the bank's name.

## bankset creditsname
 - Usage: `?bankset creditsname <name> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Set the name for the bank's currency.

## bankset toggleglobal
 - Usage: `?bankset toggleglobal [confirm=False] `
 - Restricted to: `BOT_OWNER`

Toggle whether the bank is global or not.<br/><br/>If the bank is global, it will become per-server.<br/>If the bank is per-server, it will become global.

# modlogset
 - Usage: `?modlogset `
 - Restricted to: `GUILD_OWNER`

Manage modlog settings.

## modlogset cases
 - Usage: `?modlogset cases [action=None] `
 - Checks: `server_only`

Enable or disable case creation for a mod action.<br/><br/>An action can be enabling or disabling specific cases. (Ban, kick, mute, etc.)<br/><br/>Example: `?modlogset cases kick enabled`

## modlogset modlog
 - Usage: `?modlogset modlog [channel=None] `
 - Aliases: `channel`
 - Checks: `server_only`

Set a channel as the modlog.<br/><br/>Omit `[channel]` to disable the modlog.

## modlogset resetcases
 - Usage: `?modlogset resetcases `
 - Checks: `server_only`

Reset all modlog cases in this server.

## modlogset fixcasetypes
 - Usage: `?modlogset fixcasetypes `
 - Restricted to: `BOT_OWNER`

Command to fix misbehaving casetypes.

# set
 - Usage: `?set `

Commands for changing JuiceBot's settings.

## set api
 - Usage: `?set api [service=None] [tokens] `
 - Restricted to: `BOT_OWNER`

Commands to set, list or remove various external API tokens.<br/><br/>This setting will be asked for by some 3rd party cogs and some core cogs.<br/><br/>If passed without the `<service>` or `<tokens>` arguments it will allow you to open a modal to set your API keys securely.<br/><br/>To add the keys provide the service name and the tokens as a comma separated<br/>list of key,values as described by the cog requesting this command.<br/><br/>Note: API tokens are sensitive, so this command should only be used in a private channel or in DM with the bot.<br/><br/>**Examples:**<br/>- `?set api`<br/>- `?set api spotify`<br/>- `?set api spotify redirect_uri localhost`<br/>- `?set api github client_id,whoops client_secret,whoops`<br/><br/>**Arguments:**<br/>- `<service>` - The service you're adding tokens to.<br/>- `<tokens>` - Pairs of token keys and values. The key and value should be separated by one of ` `, `,`, or `;`.

### set api remove
 - Usage: `?set api remove <services> `

Remove the given services with all their keys and tokens.<br/><br/>**Examples:**<br/>- `?set api remove spotify`<br/>- `?set api remove github youtube`<br/><br/>**Arguments:**<br/>- `<services...>` - The services to remove.

### set api list
 - Usage: `?set api list `

Show all external API services along with their keys that have been set.<br/><br/>Secrets are not shown.<br/><br/>**Example:**<br/>- `?set api list`

## set serverfuzzy
 - Usage: `?set serverfuzzy `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Toggle whether to enable fuzzy command search for the server.<br/><br/>This allows the bot to identify potential misspelled commands and offer corrections.<br/><br/>Note: This can be processor intensive and may be unsuitable for larger servers.<br/><br/>Default is for fuzzy command search to be disabled.<br/><br/>**Example:**<br/>- `?set serverfuzzy`

## set fuzzy
 - Usage: `?set fuzzy `
 - Restricted to: `BOT_OWNER`

Toggle whether to enable fuzzy command search in DMs.<br/><br/>This allows the bot to identify potential misspelled commands and offer corrections.<br/><br/>Default is for fuzzy command search to be disabled.<br/><br/>**Example:**<br/>- `?set fuzzy`

## set serverprefix
 - Usage: `?set serverprefix <server> <prefixes> `
 - Restricted to: `ADMIN`
 - Aliases: `serverprefixes`

Sets JuiceBot's server prefix(es).<br/><br/>Warning: This will override global prefixes, the bot will not respond to any global prefixes in this server.<br/>    This is not additive. It will replace all current server prefixes.<br/>    A prefix cannot have more than 25 characters.<br/><br/>**Examples:**<br/>- `?set serverprefix !`<br/>- `?set serverprefix "! "` - Quotes are needed to use spaces in prefixes.<br/>- `?set serverprefix "@JuiceBot "` - This uses a mention as the prefix.<br/>- `?set serverprefix ! ? .` - Sets multiple prefixes.<br/>- `?set serverprefix "Red - Discord Bot" ?` - Sets the prefix for a specific server. Quotes are needed to use spaces in the server name.<br/><br/>**Arguments:**<br/>- `[server]` - The server to set the prefix for. Defaults to current server.<br/>- `[prefixes...]` - The prefixes the bot will respond to on this server. Leave blank to clear server prefixes.

## set ownernotifications
 - Usage: `?set ownernotifications `
 - Restricted to: `BOT_OWNER`

Commands for configuring owner notifications.<br/><br/>Owner notifications include usage of `?contact` and available Red updates.

### set ownernotifications optout
 - Usage: `?set ownernotifications optout `

Opt-out of receiving owner notifications.<br/><br/>Note: This will only stop sending owner notifications to your DMs.<br/>    Additional owners and destinations will still receive notifications.<br/><br/>**Example:**<br/>- `?set ownernotifications optout`

### set ownernotifications removedestination
 - Usage: `?set ownernotifications removedestination <channel> `
 - Aliases: `remdestination, deletedestination, and deldestination`

Removes a destination text channel from receiving owner notifications.<br/><br/>**Examples:**<br/>- `?set ownernotifications removedestination #owner-notifications`<br/>- `?set ownernotifications deletedestination 168091848718417920` - Accepts channel IDs.<br/><br/>**Arguments:**<br/>- `<channel>` - The channel to stop sending owner notifications to.

### set ownernotifications adddestination
 - Usage: `?set ownernotifications adddestination <channel> `

Adds a destination text channel to receive owner notifications.<br/><br/>**Examples:**<br/>- `?set ownernotifications adddestination #owner-notifications`<br/>- `?set ownernotifications adddestination 168091848718417920` - Accepts channel IDs.<br/><br/>**Arguments:**<br/>- `<channel>` - The channel to send owner notifications to.

### set ownernotifications optin
 - Usage: `?set ownernotifications optin `

Opt-in on receiving owner notifications.<br/><br/>This is the default state.<br/><br/>Note: This will only resume sending owner notifications to your DMs.<br/>    Additional owners and destinations will not be affected.<br/><br/>**Example:**<br/>- `?set ownernotifications optin`

### set ownernotifications listdestinations
 - Usage: `?set ownernotifications listdestinations `

Lists the configured extra destinations for owner notifications.<br/><br/>**Example:**<br/>- `?set ownernotifications listdestinations`

## set deletedelay
 - Usage: `?set deletedelay [time=None] `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Set the delay until the bot removes the command message.<br/><br/>Must be between -1 and 60.<br/><br/>Set to -1 to disable this feature.<br/><br/>This is only applied to the current server and not globally.<br/><br/>**Examples:**<br/>- `?set deletedelay` - Shows the current delete delay setting.<br/>- `?set deletedelay 60` - Sets the delete delay to the max of 60 seconds.<br/>- `?set deletedelay -1` - Disables deleting command messages.<br/><br/>**Arguments:**<br/>- `[time]` - The seconds to wait before deleting the command message. Use -1 to disable.

## set regionalformat
 - Usage: `?set regionalformat <language_code> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `region`

Changes the bot's regional format in this server. This is used for formatting date, time and numbers.<br/><br/>`language_code` can be any language code with country code included, e.g. `en-US`, `de-DE`, `fr-FR`, `pl-PL`, etc.<br/>Pass "reset" to `language_code` to base regional formatting on bot's locale in this server.<br/><br/>If you want to change bot's global regional format, see `?set regionalformat global` command.<br/><br/>**Examples:**<br/>- `?set regionalformat en-US`<br/>- `?set region de-DE`<br/>- `?set regionalformat reset` - Resets to the locale.<br/><br/>**Arguments:**<br/>- `[language_code]` - The region format to use for the bot in this server.

### set regionalformat server
 - Usage: `?set regionalformat server <language_code> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `local and server`
 - Checks: `server_only`

Changes the bot's regional format in this server. This is used for formatting date, time and numbers.<br/><br/>`language_code` can be any language code with country code included, e.g. `en-US`, `de-DE`, `fr-FR`, `pl-PL`, etc.<br/>Pass "reset" to `language_code` to base regional formatting on bot's locale in this server.<br/><br/>**Examples:**<br/>- `?set regionalformat server en-US`<br/>- `?set region local de-DE`<br/>- `?set regionalformat server reset` - Resets to the locale.<br/><br/>**Arguments:**<br/>- `[language_code]` - The region format to use for the bot in this server.

### set regionalformat global
 - Usage: `?set regionalformat global <language_code> `
 - Restricted to: `BOT_OWNER`

Changes the bot's regional format. This is used for formatting date, time and numbers.<br/><br/>`language_code` can be any language code with country code included, e.g. `en-US`, `de-DE`, `fr-FR`, `pl-PL`, etc.<br/>Pass "reset" to `language_code` to base regional formatting on bot's locale.<br/><br/>**Examples:**<br/>- `?set regionalformat global en-US`<br/>- `?set region global de-DE`<br/>- `?set regionalformat global reset` - Resets to the locale.<br/><br/>**Arguments:**<br/>- `[language_code]` - The default region format to use for the bot.

## set status
 - Usage: `?set status `
 - Restricted to: `BOT_OWNER`
 - Checks: `bot_in_a_server`

Commands for setting JuiceBot's status.

### set status invisible
 - Usage: `?set status invisible `
 - Restricted to: `BOT_OWNER`
 - Aliases: `offline`
 - Checks: `bot_in_a_server`

Set JuiceBot's status to invisible.

### set status playing
 - Usage: `?set status playing [game] `
 - Restricted to: `BOT_OWNER`
 - Aliases: `game`
 - Checks: `bot_in_a_server`

Sets JuiceBot's playing status.<br/><br/>This will appear as `Playing <game>` or `PLAYING A GAME: <game>` depending on the context.<br/><br/>Maximum length for a playing status is 128 characters.<br/><br/>**Examples:**<br/>- `?set status playing` - Clears the activity status.<br/>- `?set status playing the keyboard`<br/><br/>**Arguments:**<br/>- `[game]` - The text to follow `Playing`. Leave blank to clear the current activity status.

### set status streaming
 - Usage: `?set status streaming [streamer=None] [stream_title] `
 - Restricted to: `BOT_OWNER`
 - Aliases: `stream and twitch`
 - Checks: `bot_in_a_server`

Sets JuiceBot's streaming status to a twitch stream.<br/><br/>This will appear as `Streaming <stream_title>` or `LIVE ON TWITCH` depending on the context.<br/>It will also include a `Watch` button with a twitch.tv url for the provided streamer.<br/><br/>Maximum length for a stream title is 128 characters.<br/><br/>Leaving both streamer and stream_title empty will clear it.<br/><br/>**Examples:**<br/>- `?set status stream` - Clears the activity status.<br/>- `?set status stream 26 Twentysix is streaming` - Sets the stream to `https://www.twitch.tv/26`.<br/>- `?set status stream https://twitch.tv/26 Twentysix is streaming` - Sets the URL manually.<br/><br/>**Arguments:**<br/>- `<streamer>` - The twitch streamer to provide a link to. This can be their twitch name or the entire URL.<br/>- `<stream_title>` - The text to follow `Streaming` in the status.

### set status online
 - Usage: `?set status online `
 - Restricted to: `BOT_OWNER`
 - Checks: `bot_in_a_server`

Set JuiceBot's status to online.

### set status dnd
 - Usage: `?set status dnd `
 - Restricted to: `BOT_OWNER`
 - Aliases: `donotdisturb and busy`
 - Checks: `bot_in_a_server`

Set JuiceBot's status to do not disturb.

### set status idle
 - Usage: `?set status idle `
 - Restricted to: `BOT_OWNER`
 - Aliases: `away and afk`
 - Checks: `bot_in_a_server`

Set JuiceBot's status to idle.

### set status listening
 - Usage: `?set status listening [listening] `
 - Restricted to: `BOT_OWNER`
 - Checks: `bot_in_a_server`

Sets JuiceBot's listening status.<br/><br/>This will appear as `Listening to <listening>`.<br/><br/>Maximum length for a listening status is 128 characters.<br/><br/>**Examples:**<br/>- `?set status listening` - Clears the activity status.<br/>- `?set status listening jams`<br/><br/>**Arguments:**<br/>- `[listening]` - The text to follow `Listening to`. Leave blank to clear the current activity status.

### set status competing
 - Usage: `?set status competing [competing] `
 - Restricted to: `BOT_OWNER`
 - Checks: `bot_in_a_server`

Sets JuiceBot's competing status.<br/><br/>This will appear as `Competing in <competing>`.<br/><br/>Maximum length for a competing status is 128 characters.<br/><br/>**Examples:**<br/>- `?set status competing` - Clears the activity status.<br/>- `?set status competing London 2012 Olympic Games`<br/><br/>**Arguments:**<br/>- `[competing]` - The text to follow `Competing in`. Leave blank to clear the current activity status.

### set status watching
 - Usage: `?set status watching [watching] `
 - Restricted to: `BOT_OWNER`
 - Checks: `bot_in_a_server`

Sets JuiceBot's watching status.<br/><br/>This will appear as `Watching <watching>`.<br/><br/>Maximum length for a watching status is 128 characters.<br/><br/>**Examples:**<br/>- `?set status watching` - Clears the activity status.<br/>- `?set status watching ?help`<br/><br/>**Arguments:**<br/>- `[watching]` - The text to follow `Watching`. Leave blank to clear the current activity status.

## set prefix
 - Usage: `?set prefix <prefixes> `
 - Restricted to: `BOT_OWNER`
 - Aliases: `prefixes, globalprefix, and globalprefixes`

Sets JuiceBot's global prefix(es).<br/><br/>Warning: This is not additive. It will replace all current prefixes.<br/><br/>See also the `--mentionable` flag to enable mentioning the bot as the prefix.<br/><br/>**Examples:**<br/>- `?set prefix !`<br/>- `?set prefix "! "` - Quotes are needed to use spaces in prefixes.<br/>- `?set prefix "@JuiceBot "` - This uses a mention as the prefix. See also the `--mentionable` flag.<br/>- `?set prefix ! ? .` - Sets multiple prefixes.<br/><br/>**Arguments:**<br/>- `<prefixes...>` - The prefixes the bot will respond to globally.

## set locale
 - Usage: `?set locale <language_code> `
 - Restricted to: `GUILD_OWNER`

Changes JuiceBot's locale in this server.<br/><br/>Go to [Red's Crowdin page](https://translate.discord.red) to see locales that are available with translations.<br/><br/>Use "default" to return to the bot's default set language.<br/><br/>If you want to change bot's global locale, see `?set locale global` command.<br/><br/>**Examples:**<br/>- `?set locale en-US`<br/>- `?set locale de-DE`<br/>- `?set locale fr-FR`<br/>- `?set locale pl-PL`<br/>- `?set locale default` - Resets to the global default locale.<br/><br/>**Arguments:**<br/>- `<language_code>` - The default locale to use for the bot. This can be any language code with country code included.

### set locale server
 - Usage: `?set locale server <language_code> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `local and server`
 - Checks: `server_only`

Changes JuiceBot's locale in this server.<br/><br/>Go to [Red's Crowdin page](https://translate.discord.red) to see locales that are available with translations.<br/><br/>Use "default" to return to the bot's default set language.<br/><br/>**Examples:**<br/>- `?set locale server en-US`<br/>- `?set locale server de-DE`<br/>- `?set locale server fr-FR`<br/>- `?set locale server pl-PL`<br/>- `?set locale server default` - Resets to the global default locale.<br/><br/>**Arguments:**<br/>- `<language_code>` - The default locale to use for the bot. This can be any language code with country code included.

### set locale global
 - Usage: `?set locale global <language_code> `
 - Restricted to: `BOT_OWNER`

Changes JuiceBot's default locale.<br/><br/>This will be used when a server has not set a locale, or in DMs.<br/><br/>Go to [Red's Crowdin page](https://translate.discord.red) to see locales that are available with translations.<br/><br/>To reset to English, use "en-US".<br/><br/>**Examples:**<br/>- `?set locale global en-US`<br/>- `?set locale global de-DE`<br/>- `?set locale global fr-FR`<br/>- `?set locale global pl-PL`<br/><br/>**Arguments:**<br/>- `<language_code>` - The default locale to use for the bot. This can be any language code with country code included.

## set usebuttons
 - Usage: `?set usebuttons [use_buttons=None] `
 - Restricted to: `BOT_OWNER`

Set a global bot variable for using buttons in menus.<br/><br/>When enabled, all usage of cores menus API will use buttons instead of reactions.<br/><br/>This defaults to False.<br/>Using this without a setting will toggle.<br/><br/>**Examples:**<br/>    - `?set usebuttons True` - Enables using buttons.<br/>    - `?helpset usebuttons` - Toggles the value.<br/><br/>**Arguments:**<br/>    - `[use_buttons]` - Whether to use buttons. Leave blank to toggle.

## set showsettings
 - Usage: `?set showsettings [server=None] `

Show the current settings for JuiceBot.<br/><br/>Accepts optional server parameter to allow prefix recovery.

## set usebotcolour
 - Usage: `?set usebotcolour `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `usebotcolor`
 - Checks: `server_only`

Toggle whether to use the bot owner-configured colour for embeds.<br/><br/>Default is to use the bot's configured colour.<br/>Otherwise, the colour used will be the colour of the bot's top role.<br/><br/>**Example:**<br/>- `?set usebotcolour`

## set colour
 - Usage: `?set colour [colour] `
 - Restricted to: `BOT_OWNER`
 - Aliases: `color`

Sets a default colour to be used for the bot's embeds.<br/><br/>Acceptable values for the colour parameter can be found at:<br/><br/>https://discordpy.readthedocs.io/en/stable/ext/commands/api.html#discord.ext.commands.ColourConverter<br/><br/>**Examples:**<br/>- `?set colour dark red`<br/>- `?set colour blurple`<br/>- `?set colour 0x5DADE2`<br/>- `?set color 0x#FDFEFE`<br/>- `?set color #7F8C8D`<br/><br/>**Arguments:**<br/>- `[colour]` - The colour to use for embeds. Leave blank to set to the default value (red).

## set errormsg
 - Usage: `?set errormsg [msg] `
 - Restricted to: `BOT_OWNER`

Set the message that will be sent on uncaught bot errors.<br/><br/>To include the command name in the message, use the `{command}` placeholder.<br/><br/>If you omit the `msg` argument, the message will be reset to the default one.<br/><br/>**Examples:**<br/>    - `?set errormsg` - Resets the error message back to the default: "Error in command '{command}'.". If the command invoker is one of the bot owners, the message will also include "Check your console or logs for details.".<br/>    - `?set errormsg Oops, the command {command} has failed! Please try again later.` - Sets the error message to a custom one.<br/><br/>**Arguments:**<br/>    - `[msg]` - The custom error message. Must be less than 1000 characters. Omit to reset to the default one.

## set bot
 - Usage: `?set bot `
 - Restricted to: `ADMIN`
 - Aliases: `metadata`

Commands for changing JuiceBot's metadata.

### set bot avatar
 - Usage: `?set bot avatar [url=None] `
 - Restricted to: `BOT_OWNER`

Sets JuiceBot's avatar<br/><br/>Supports either an attachment or an image URL.<br/><br/>**Examples:**<br/>- `?set bot avatar` - With an image attachment, this will set the avatar.<br/>- `?set bot avatar` - Without an attachment, this will show the command help.<br/>- `?set bot avatar https://links.flaree.xyz/k95` - Sets the avatar to the provided url.<br/><br/>**Arguments:**<br/>- `[url]` - An image url to be used as an avatar. Leave blank when uploading an attachment.

#### set bot avatar remove
 - Usage: `?set bot avatar remove `
 - Restricted to: `BOT_OWNER`
 - Aliases: `clear`

Removes JuiceBot's avatar.<br/><br/>**Example:**<br/>- `?set bot avatar remove`

### set bot custominfo
 - Usage: `?set bot custominfo [text] `
 - Restricted to: `BOT_OWNER`

Customizes a section of `?info`.<br/><br/>The maximum amount of allowed characters is 1024.<br/>Supports markdown, links and "mentions".<br/><br/>Link example: `[My link](https://example.com)`<br/><br/>**Examples:**<br/>- `?set bot custominfo >>> I can use **markdown** such as quotes, ||spoilers|| and multiple lines.`<br/>- `?set bot custominfo Join my [support server](discord.gg/discord)!`<br/>- `?set bot custominfo` - Removes custom info text.<br/><br/>**Arguments:**<br/>- `[text]` - The custom info text.

### set bot username
 - Usage: `?set bot username <username> `
 - Restricted to: `BOT_OWNER`
 - Aliases: `name`

Sets JuiceBot's username.<br/><br/>Maximum length for a username is 32 characters.<br/><br/>Note: The username of a verified bot cannot be manually changed.<br/>    Please contact Discord support to change it.<br/><br/>**Example:**<br/>- `?set bot username BaguetteBot`<br/><br/>**Arguments:**<br/>- `<username>` - The username to give the bot.

### set bot nickname
 - Usage: `?set bot nickname [nickname] `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Sets JuiceBot's nickname for the current server.<br/><br/>Maximum length for a nickname is 32 characters.<br/><br/>**Example:**<br/>- `?set bot nickname 🎃 SpookyBot 🎃`<br/><br/>**Arguments:**<br/>- `[nickname]` - The nickname to give the bot. Leave blank to clear the current nickname.

### set bot description
 - Usage: `?set bot description [description] `
 - Restricted to: `BOT_OWNER`

Sets the bot's description.<br/><br/>Use without a description to reset.<br/>This is shown in a few locations, including the help menu.<br/><br/>The maximum description length is 250 characters to ensure it displays properly.<br/><br/>The default is "Red V3".<br/><br/>**Examples:**<br/>- `?set bot description` - Resets the description to the default setting.<br/>- `?set bot description MyBot: A Red V3 Bot`<br/><br/>**Arguments:**<br/>- `[description]` - The description to use for this bot. Leave blank to reset to the default.

## set roles
 - Usage: `?set roles `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Set server's admin and mod roles for JuiceBot.

### set roles removeadminrole
 - Usage: `?set roles removeadminrole <role> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `remadmindrole, deladminrole, and deleteadminrole`
 - Checks: `server_only`

Removes an admin role for this server.<br/><br/>**Examples:**<br/>- `?set roles removeadminrole @Admins`<br/>- `?set roles removeadminrole Super Admins`<br/><br/>**Arguments:**<br/>- `<role>` - The role to remove from being an admin.

### set roles addmodrole
 - Usage: `?set roles addmodrole <role> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Adds a moderator role for this server.<br/><br/>This grants access to moderator level commands like:<br/> - `?mute`<br/> - `?cleanup`<br/> - `?customcommand create`<br/><br/> And more.<br/><br/>**Examples:**<br/>- `?set roles addmodrole @Mods`<br/>- `?set roles addmodrole Loyal Helpers`<br/><br/>**Arguments:**<br/>- `<role>` - The role to add as a moderator.

### set roles addadminrole
 - Usage: `?set roles addadminrole <role> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Adds an admin role for this server.<br/><br/>Admins have the same access as Mods, plus additional admin level commands like:<br/> - `?set serverprefix`<br/> - `?addrole`<br/> - `?ban`<br/> - `?ignore server`<br/><br/> And more.<br/><br/>**Examples:**<br/>- `?set roles addadminrole @Admins`<br/>- `?set roles addadminrole Super Admins`<br/><br/>**Arguments:**<br/>- `<role>` - The role to add as an admin.

### set roles removemodrole
 - Usage: `?set roles removemodrole <role> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `remmodrole, delmodrole, and deletemodrole`
 - Checks: `server_only`

Removes a mod role for this server.<br/><br/>**Examples:**<br/>- `?set roles removemodrole @Mods`<br/>- `?set roles removemodrole Loyal Helpers`<br/><br/>**Arguments:**<br/>- `<role>` - The role to remove from being a moderator.

# helpset
 - Usage: `?helpset `
 - Restricted to: `BOT_OWNER`

Commands to manage settings for the help command.<br/><br/>All help settings are applied globally.

## helpset pagecharlimit
 - Usage: `?helpset pagecharlimit <limit> `

Set the character limit for each page in the help message.<br/><br/>Note: This setting only applies to embedded help.<br/><br/>The default value is 1000 characters. The minimum value is 500.<br/>The maximum is based on the lower of what you provide and what discord allows.<br/><br/>Please note that setting a relatively small character limit may<br/>mean some pages will exceed this limit.<br/><br/>**Example:**<br/>- `?helpset pagecharlimit 1500`<br/><br/>**Arguments:**<br/>- `<limit>` - The max amount of characters to show per page in the help message.

## helpset resetformatter
 - Usage: `?helpset resetformatter `

This resets JuiceBot's help formatter to the default formatter.<br/><br/>**Example:**<br/>- `?helpset resetformatter`

## helpset tagline
 - Usage: `?helpset tagline [tagline] `

Set the tagline to be used.<br/><br/>The maximum tagline length is 2048 characters.<br/>This setting only applies to embedded help. If no tagline is specified, the default will be used instead.<br/><br/>**Examples:**<br/>- `?helpset tagline Thanks for using the bot!`<br/>- `?helpset tagline` - Resets the tagline to the default.<br/><br/>**Arguments:**<br/>- `[tagline]` - The tagline to appear at the bottom of help embeds. Leave blank to reset.

## helpset verifychecks
 - Usage: `?helpset verifychecks [verify=None] `

Sets if commands which can't be run in the current context should be filtered from help.<br/><br/>Defaults to True.<br/>Using this without a setting will toggle.<br/><br/>**Examples:**<br/>- `?helpset verifychecks False` - Enables showing unusable commands in help.<br/>- `?helpset verifychecks` - Toggles the value.<br/><br/>**Arguments:**<br/>- `[verify]` - Whether to hide unusable commands in help. Leave blank to toggle.

## helpset verifyexists
 - Usage: `?helpset verifyexists [verify=None] `

Sets whether the bot should respond to help commands for nonexistent topics.<br/><br/>When enabled, this will indicate the existence of help topics, even if the user can't use it.<br/><br/>Note: This setting on its own does not fully prevent command enumeration.<br/><br/>Defaults to False.<br/>Using this without a setting will toggle.<br/><br/>**Examples:**<br/>- `?helpset verifyexists True` - Enables sending help for nonexistent topics.<br/>- `?helpset verifyexists` - Toggles the value.<br/><br/>**Arguments:**<br/>- `[verify]` - Whether to respond to help for nonexistent topics. Leave blank to toggle.

## helpset showsettings
 - Usage: `?helpset showsettings `

Show the current help settings.<br/><br/>Warning: These settings may not be accurate if the default formatter is not in use.<br/><br/>**Example:**<br/>- `?helpset showsettings`

## helpset usetick
 - Usage: `?helpset usetick [use_tick=None] `

This allows the help command message to be ticked if help is sent to a DM.<br/><br/>Ticking is reacting to the help message with a ✅.<br/><br/>Defaults to False.<br/>Using this without a setting will toggle.<br/><br/>Note: This is only used when the bot is not using menus.<br/><br/>**Examples:**<br/>- `?helpset usetick False` - Disables ticking when help is sent to DMs.<br/>- `?helpset usetick` - Toggles the value.<br/><br/>**Arguments:**<br/>- `[use_tick]` - Whether to tick the help command when help is sent to DMs. Leave blank to toggle.

## helpset deletedelay
 - Usage: `?helpset deletedelay <seconds> `

Set the delay after which help pages will be deleted.<br/><br/>The setting is disabled by default, and only applies to non-menu help,<br/>sent in server text channels.<br/>Setting the delay to 0 disables this feature.<br/><br/>The bot has to have MANAGE_MESSAGES permission for this to work.<br/><br/>**Examples:**<br/>- `?helpset deletedelay 60` - Delete the help pages after a minute.<br/>- `?helpset deletedelay 1` - Delete the help pages as quickly as possible.<br/>- `?helpset deletedelay 1209600` - Max time to wait before deleting (14 days).<br/>- `?helpset deletedelay 0` - Disable deleting help pages.<br/><br/>**Arguments:**<br/>- `<seconds>` - The seconds to wait before deleting help pages.

## helpset showhidden
 - Usage: `?helpset showhidden [show_hidden=None] `

This allows the help command to show hidden commands.<br/><br/>This defaults to False.<br/>Using this without a setting will toggle.<br/><br/>**Examples:**<br/>- `?helpset showhidden True` - Enables showing hidden commands.<br/>- `?helpset showhidden` - Toggles the value.<br/><br/>**Arguments:**<br/>- `[show_hidden]` - Whether to use show hidden commands in help. Leave blank to toggle.

## helpset showaliases
 - Usage: `?helpset showaliases [show_aliases=None] `

This allows the help command to show existing commands aliases if there is any.<br/><br/>This defaults to True.<br/>Using this without a setting will toggle.<br/><br/>**Examples:**<br/>- `?helpset showaliases False` - Disables showing aliases on this server.<br/>- `?helpset showaliases` - Toggles the value.<br/><br/>**Arguments:**<br/>- `[show_aliases]` - Whether to include aliases in help. Leave blank to toggle.

## helpset usemenus
 - Usage: `?helpset usemenus <use_menus> `

Allows the help command to be sent as a paginated menu instead of separate<br/>messages.<br/><br/>When "reactions", "buttons", "select", or "selectonly" is passed,<br/> `?help` will only show one page at a time<br/>and will use the associated control scheme to navigate between pages.<br/><br/> **Examples:**<br/>- `?helpset usemenus reactions` - Enables using reaction menus.<br/>- `?helpset usemenus buttons` - Enables using button menus.<br/>- `?helpset usemenus select` - Enables buttons with a select menu.<br/>- `?helpset usemenus selectonly` - Enables a select menu only on help.<br/>- `?helpset usemenus disable` - Disables help menus.<br/><br/>**Arguments:**<br/>    - `<"buttons"|"reactions"|"select"|"selectonly"|"disable">` - Whether to use `buttons`,<br/>    `reactions`, `select`, `selectonly`, or no menus.

## helpset reacttimeout
 - Usage: `?helpset reacttimeout <seconds> `

Set the timeout for reactions, if menus are enabled.<br/><br/>The default is 30 seconds.<br/>The timeout has to be between 15 and 300 seconds.<br/><br/>**Examples:**<br/>- `?helpset reacttimeout 30` - The default timeout.<br/>- `?helpset reacttimeout 60` - Timeout of 1 minute.<br/>- `?helpset reacttimeout 15` - Minimum allowed timeout.<br/>- `?helpset reacttimeout 300` - Max allowed timeout (5 mins).<br/><br/>**Arguments:**<br/>- `<seconds>` - The timeout, in seconds, of the reactions.

## helpset resetsettings
 - Usage: `?helpset resetsettings `

This resets JuiceBot's help settings to their defaults.<br/><br/>This may not have an impact when using custom formatters from 3rd party cogs<br/><br/>**Example:**<br/>- `?helpset resetsettings`

## helpset maxpages
 - Usage: `?helpset maxpages <pages> `

Set the maximum number of help pages sent in a server channel.<br/><br/>Note: This setting does not apply to menu help.<br/><br/>If a help message contains more pages than this value, the help message will<br/>be sent to the command author via DM. This is to help reduce spam in server<br/>text channels.<br/><br/>The default value is 2 pages.<br/><br/>**Examples:**<br/>- `?helpset maxpages 50` - Basically never send help to DMs.<br/>- `?helpset maxpages 0` - Always send help to DMs.<br/><br/>**Arguments:**<br/>- `<limit>` - The max pages allowed to send per help in a server.

# contact
 - Usage: `?contact <message> `
 - Cooldown: `1 per 60.0 seconds`

Sends a message to the owner.<br/><br/>This is limited to one message every 60 seconds per person.<br/><br/>**Example:**<br/>- `?contact Help! The bot has become sentient!`<br/><br/>**Arguments:**<br/>- `[message]` - The message to send to the owner.

# dm
 - Usage: `?dm <user_id> <message> `
 - Restricted to: `BOT_OWNER`

Sends a DM to a user.<br/><br/>This command needs a user ID to work.<br/><br/>To get a user ID, go to Discord's settings and open the 'Appearance' tab.<br/>Enable 'Developer Mode', then right click a user and click on 'Copy ID'.<br/><br/>**Example:**<br/>- `?dm 262626262626262626 Do you like me? Yes / No`<br/><br/>**Arguments:**<br/>- `[message]` - The message to dm to the user.

# datapath
 - Usage: `?datapath `
 - Restricted to: `BOT_OWNER`

Prints the bot's data path.

# debuginfo
 - Usage: `?debuginfo `
 - Restricted to: `BOT_OWNER`

Shows debug information useful for debugging.

# diagnoseissues
 - Usage: `?diagnoseissues [channel=operator.attrgetter('channel')] <member> <command_name> `
 - Restricted to: `BOT_OWNER`

Diagnose issues with the command checks with ease!<br/><br/>If you want to diagnose the command from a text channel in a different server,<br/>you can do so by using the command in DMs.<br/><br/>**Example:**<br/>- `?diagnoseissues #general @Slime ban` - Diagnose why @Slime can't use `?ban` in #general channel.<br/><br/>**Arguments:**<br/>- `[channel]` - The text channel that the command should be tested for. Defaults to the current channel.<br/>- `<member>` - The member that should be considered as the command caller.<br/>- `<command_name>` - The name of the command to test.

# allowlist
 - Usage: `?allowlist `
 - Restricted to: `BOT_OWNER`
 - Aliases: `whitelist`

Commands to manage the allowlist.<br/><br/>Warning: When the allowlist is in use, the bot will ignore commands from everyone not on the list.<br/><br/>Use `?allowlist clear` to disable the allowlist

## allowlist list
 - Usage: `?allowlist list `

Lists users on the allowlist.<br/><br/>**Example:**<br/>- `?allowlist list`

## allowlist add
 - Usage: `?allowlist add <users> `

Adds users to the allowlist.<br/><br/>**Examples:**<br/>- `?allowlist add @26 @Will` - Adds two users to the allowlist.<br/>- `?allowlist add 262626262626262626` - Adds a user by ID.<br/><br/>**Arguments:**<br/>- `<users...>` - The user or users to add to the allowlist.

## allowlist remove
 - Usage: `?allowlist remove <users> `

Removes users from the allowlist.<br/><br/>The allowlist will be disabled if all users are removed.<br/><br/>**Examples:**<br/>- `?allowlist remove @26 @Will` - Removes two users from the allowlist.<br/>- `?allowlist remove 262626262626262626` - Removes a user by ID.<br/><br/>**Arguments:**<br/>- `<users...>` - The user or users to remove from the allowlist.

## allowlist clear
 - Usage: `?allowlist clear `

Clears the allowlist.<br/><br/>This disables the allowlist.<br/><br/>**Example:**<br/>- `?allowlist clear`

# blocklist
 - Usage: `?blocklist `
 - Restricted to: `BOT_OWNER`
 - Aliases: `blacklist and denylist`

Commands to manage the blocklist.<br/><br/>Use `?blocklist clear` to disable the blocklist

## blocklist add
 - Usage: `?blocklist add <users> `

Adds users to the blocklist.<br/><br/>**Examples:**<br/>- `?blocklist add @26 @Will` - Adds two users to the blocklist.<br/>- `?blocklist add 262626262626262626` - Blocks a user by ID.<br/><br/>**Arguments:**<br/>- `<users...>` - The user or users to add to the blocklist.

## blocklist list
 - Usage: `?blocklist list `

Lists users on the blocklist.<br/><br/>**Example:**<br/>- `?blocklist list`

## blocklist clear
 - Usage: `?blocklist clear `

Clears the blocklist.<br/><br/>**Example:**<br/>- `?blocklist clear`

## blocklist remove
 - Usage: `?blocklist remove <users> `

Removes users from the blocklist.<br/><br/>**Examples:**<br/>- `?blocklist remove @26 @Will` - Removes two users from the blocklist.<br/>- `?blocklist remove 262626262626262626` - Removes a user by ID.<br/><br/>**Arguments:**<br/>- `<users...>` - The user or users to remove from the blocklist.

# localallowlist
 - Usage: `?localallowlist `
 - Restricted to: `ADMIN`
 - Aliases: `localwhitelist`
 - Checks: `server_only`

Commands to manage the server specific allowlist.<br/><br/>Warning: When the allowlist is in use, the bot will ignore commands from everyone not on the list in the server.<br/><br/>Use `?localallowlist clear` to disable the allowlist

## localallowlist clear
 - Usage: `?localallowlist clear `

Clears the allowlist.<br/><br/>This disables the local allowlist and clears all entries.<br/><br/>**Example:**<br/>- `?localallowlist clear`

## localallowlist add
 - Usage: `?localallowlist add <users_or_roles> `

Adds a user or role to the server allowlist.<br/><br/>**Examples:**<br/>- `?localallowlist add @26 @Will` - Adds two users to the local allowlist.<br/>- `?localallowlist add 262626262626262626` - Allows a user by ID.<br/>- `?localallowlist add "Super Admins"` - Allows a role with a space in the name without mentioning.<br/><br/>**Arguments:**<br/>- `<users_or_roles...>` - The users or roles to remove from the local allowlist.

## localallowlist remove
 - Usage: `?localallowlist remove <users_or_roles> `

Removes user or role from the allowlist.<br/><br/>The local allowlist will be disabled if all users are removed.<br/><br/>**Examples:**<br/>- `?localallowlist remove @26 @Will` - Removes two users from the local allowlist.<br/>- `?localallowlist remove 262626262626262626` - Removes a user by ID.<br/>- `?localallowlist remove "Super Admins"` - Removes a role with a space in the name without mentioning.<br/><br/>**Arguments:**<br/>- `<users_or_roles...>` - The users or roles to remove from the local allowlist.

## localallowlist list
 - Usage: `?localallowlist list `

Lists users and roles on the server allowlist.<br/><br/>**Example:**<br/>- `?localallowlist list`

# localblocklist
 - Usage: `?localblocklist `
 - Restricted to: `ADMIN`
 - Aliases: `localblacklist`
 - Checks: `server_only`

Commands to manage the server specific blocklist.<br/><br/>Use `?localblocklist clear` to disable the blocklist

## localblocklist remove
 - Usage: `?localblocklist remove <users_or_roles> `

Removes user or role from local blocklist.<br/><br/>**Examples:**<br/>- `?localblocklist remove @26 @Will` - Removes two users from the local blocklist.<br/>- `?localblocklist remove 262626262626262626` - Unblocks a user by ID.<br/>- `?localblocklist remove "Bad Apples"` - Unblocks a role with a space in the name without mentioning.<br/><br/>**Arguments:**<br/>- `<users_or_roles...>` - The users or roles to remove from the local blocklist.

## localblocklist list
 - Usage: `?localblocklist list `

Lists users and roles on the server blocklist.<br/><br/>**Example:**<br/>- `?localblocklist list`

## localblocklist clear
 - Usage: `?localblocklist clear `

Clears the server blocklist.<br/><br/>This disables the server blocklist and clears all entries.<br/><br/>**Example:**<br/>- `?blocklist clear`

## localblocklist add
 - Usage: `?localblocklist add <users_or_roles> `

Adds a user or role to the local blocklist.<br/><br/>**Examples:**<br/>- `?localblocklist add @26 @Will` - Adds two users to the local blocklist.<br/>- `?localblocklist add 262626262626262626` - Blocks a user by ID.<br/>- `?localblocklist add "Bad Apples"` - Blocks a role with a space in the name without mentioning.<br/><br/>**Arguments:**<br/>- `<users_or_roles...>` - The users or roles to add to the local blocklist.

# command
 - Usage: `?command `
 - Restricted to: `GUILD_OWNER`

Commands to enable and disable commands and cogs.

## command disable
 - Usage: `?command disable <command> `

Disable a command.<br/><br/>If you're the bot owner, this will disable commands globally by default.<br/>Otherwise, this will disable commands on the current server.<br/><br/>**Examples:**<br/>- `?command disable userinfo` - Disables the `userinfo` command in the Mod cog.<br/>- `?command disable urban` - Disables the `urban` command in the General cog.<br/><br/>**Arguments:**<br/>- `<command>` - The command to disable.

### command disable server
 - Usage: `?command disable server <command> `
 - Aliases: `server`
 - Checks: `server_only`

Disable a command in this server only.<br/><br/>**Examples:**<br/>- `?command disable server userinfo` - Disables the `userinfo` command in the Mod cog.<br/>- `?command disable server urban` - Disables the `urban` command in the General cog.<br/><br/>**Arguments:**<br/>- `<command>` - The command to disable for the current server.

### command disable global
 - Usage: `?command disable global <command> `
 - Restricted to: `BOT_OWNER`

Disable a command globally.<br/><br/>**Examples:**<br/>- `?command disable global userinfo` - Disables the `userinfo` command in the Mod cog.<br/>- `?command disable global urban` - Disables the `urban` command in the General cog.<br/><br/>**Arguments:**<br/>- `<command>` - The command to disable globally.

## command disablecog
 - Usage: `?command disablecog <cog> `
 - Checks: `server_only`

Disable a cog in this server.<br/><br/>Note: This will only work on loaded cogs, and must reference the title-case cog name.<br/><br/>**Examples:**<br/>- `?command disablecog Economy`<br/>- `?command disablecog ModLog`<br/><br/>**Arguments:**<br/>- `<cog>` - The name of the cog to disable on this server. Must be title-case.

## command listdisabledcogs
 - Usage: `?command listdisabledcogs `
 - Checks: `server_only`

List the cogs which are disabled in this server.<br/><br/>**Example:**<br/>- `?command listdisabledcogs`

## command listdisabled
 - Usage: `?command listdisabled `

List disabled commands.<br/><br/>If you're the bot owner, this will show global disabled commands by default.<br/>Otherwise, this will show disabled commands on the current server.<br/><br/>**Example:**<br/>- `?command listdisabled`

### command listdisabled global
 - Usage: `?command listdisabled global `

List disabled commands globally.<br/><br/>**Example:**<br/>- `?command listdisabled global`

### command listdisabled server
 - Usage: `?command listdisabled server `
 - Checks: `server_only`

List disabled commands in this server.<br/><br/>**Example:**<br/>- `?command listdisabled server`

## command defaultenablecog
 - Usage: `?command defaultenablecog <cog> `
 - Restricted to: `BOT_OWNER`

Set the default state for a cog as enabled.<br/><br/>This will re-enable the cog for all servers by default.<br/>To override it, use `?command disablecog` on the servers you want to disallow usage.<br/><br/>Note: This will only work on loaded cogs, and must reference the title-case cog name.<br/><br/>**Examples:**<br/>- `?command defaultenablecog Economy`<br/>- `?command defaultenablecog ModLog`<br/><br/>**Arguments:**<br/>- `<cog>` - The name of the cog to make enabled by default. Must be title-case.

## command enablecog
 - Usage: `?command enablecog <cogname> `
 - Checks: `server_only`

Enable a cog in this server.<br/><br/>Note: This will only work on loaded cogs, and must reference the title-case cog name.<br/><br/>**Examples:**<br/>- `?command enablecog Economy`<br/>- `?command enablecog ModLog`<br/><br/>**Arguments:**<br/>- `<cog>` - The name of the cog to enable on this server. Must be title-case.

## command enable
 - Usage: `?command enable <command> `

Enable a command.<br/><br/>If you're the bot owner, this will try to enable a globally disabled command by default.<br/>Otherwise, this will try to enable a command disabled on the current server.<br/><br/>**Examples:**<br/>- `?command enable userinfo` - Enables the `userinfo` command in the Mod cog.<br/>- `?command enable urban` - Enables the `urban` command in the General cog.<br/><br/>**Arguments:**<br/>- `<command>` - The command to enable.

### command enable global
 - Usage: `?command enable global <command> `
 - Restricted to: `BOT_OWNER`

Enable a command globally.<br/><br/>**Examples:**<br/>- `?command enable global userinfo` - Enables the `userinfo` command in the Mod cog.<br/>- `?command enable global urban` - Enables the `urban` command in the General cog.<br/><br/>**Arguments:**<br/>- `<command>` - The command to enable globally.

### command enable server
 - Usage: `?command enable server <command> `
 - Aliases: `server`
 - Checks: `server_only`

    Enable a command in this server.<br/><br/>**Examples:**<br/>- `?command enable server userinfo` - Enables the `userinfo` command in the Mod cog.<br/>- `?command enable server urban` - Enables the `urban` command in the General cog.<br/><br/>**Arguments:**<br/>- `<command>` - The command to enable for the current server.

## command disabledmsg
 - Usage: `?command disabledmsg [message] `
 - Restricted to: `BOT_OWNER`

Set the bot's response to disabled commands.<br/><br/>Leave blank to send nothing.<br/><br/>To include the command name in the message, include the `{command}` placeholder.<br/><br/>**Examples:**<br/>- `?command disabledmsg This command is disabled`<br/>- `?command disabledmsg {command} is disabled`<br/>- `?command disabledmsg` - Sends nothing when a disabled command is attempted.<br/><br/>**Arguments:**<br/>- `[message]` - The message to send when a disabled command is attempted.

## command defaultdisablecog
 - Usage: `?command defaultdisablecog <cog> `
 - Restricted to: `BOT_OWNER`

Set the default state for a cog as disabled.<br/><br/>This will disable the cog for all servers by default.<br/>To override it, use `?command enablecog` on the servers you want to allow usage.<br/><br/>Note: This will only work on loaded cogs, and must reference the title-case cog name.<br/><br/>**Examples:**<br/>- `?command defaultdisablecog Economy`<br/>- `?command defaultdisablecog ModLog`<br/><br/>**Arguments:**<br/>- `<cog>` - The name of the cog to make disabled by default. Must be title-case.

# autoimmune
 - Usage: `?autoimmune `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Commands to manage server settings for immunity from automated actions.<br/><br/>This includes duplicate message deletion and mention spam from the Mod cog, and filters from the Filter cog.

## autoimmune list
 - Usage: `?autoimmune list `

Gets the current members and roles configured for automatic moderation action immunity.<br/><br/>**Example:**<br/>- `?autoimmune list`

## autoimmune remove
 - Usage: `?autoimmune remove <user_or_role> `

Remove a user or role from being immune to automated moderation actions.<br/><br/>**Examples:**<br/>- `?autoimmune remove @Twentysix` - Removes a user.<br/>- `?autoimmune remove @Mods` - Removes a role.<br/><br/>**Arguments:**<br/>- `<user_or_role>` - The user or role to remove immunity from.

## autoimmune isimmune
 - Usage: `?autoimmune isimmune <user_or_role> `

Checks if a user or role would be considered immune from automated actions.<br/><br/>**Examples:**<br/>- `?autoimmune isimmune @Twentysix`<br/>- `?autoimmune isimmune @Mods`<br/><br/>**Arguments:**<br/>- `<user_or_role>` - The user or role to check the immunity of.

## autoimmune add
 - Usage: `?autoimmune add <user_or_role> `

Makes a user or role immune from automated moderation actions.<br/><br/>**Examples:**<br/>- `?autoimmune add @Twentysix` - Adds a user.<br/>- `?autoimmune add @Mods` - Adds a role.<br/><br/>**Arguments:**<br/>- `<user_or_role>` - The user or role to add immunity to.

# ignore
 - Usage: `?ignore `
 - Checks: `server_only`

Commands to add servers or channels to the ignore list.<br/><br/>The ignore list will prevent the bot from responding to commands in the configured locations.<br/><br/>Note: Owners and Admins override the ignore list.

## ignore channel
 - Usage: `?ignore channel [channel=operator.attrgetter('channel')] `

Ignore commands in the channel, thread, or category.<br/><br/>Defaults to the current thread or channel.<br/><br/>Note: Owners, Admins, and those with Manage Channel permissions override ignored channels.<br/><br/>**Examples:**<br/>- `?ignore channel #general` - Ignores commands in the #general channel.<br/>- `?ignore channel` - Ignores commands in the current channel.<br/>- `?ignore channel "General Channels"` - Use quotes for categories with spaces.<br/>- `?ignore channel 356236713347252226` - Also accepts IDs.<br/><br/>**Arguments:**<br/>- `<channel>` - The channel to ignore. This can also be a thread or category channel.

## ignore list
 - Usage: `?ignore list `

List the currently ignored servers and channels.<br/><br/>**Example:**<br/>- `?ignore list`

## ignore server
 - Usage: `?ignore server `
 - Restricted to: `ADMIN`
 - Aliases: `server`

Ignore commands in this server.<br/><br/>Note: Owners, Admins, and those with Manage Server permissions override ignored servers.<br/><br/>**Example:**<br/>- `?ignore server` - Ignores the current server

# unignore
 - Usage: `?unignore `
 - Checks: `server_only`

Commands to remove servers or channels from the ignore list.

## unignore channel
 - Usage: `?unignore channel [channel=operator.attrgetter('channel')] `

Remove a channel, thread, or category from the ignore list.<br/><br/>Defaults to the current thread or channel.<br/><br/>**Examples:**<br/>- `?unignore channel #general` - Unignores commands in the #general channel.<br/>- `?unignore channel` - Unignores commands in the current channel.<br/>- `?unignore channel "General Channels"` - Use quotes for categories with spaces.<br/>- `?unignore channel 356236713347252226` - Also accepts IDs. Use this method to unignore categories.<br/><br/>**Arguments:**<br/>- `<channel>` - The channel to unignore. This can also be a thread or category channel.

## unignore server
 - Usage: `?unignore server `
 - Restricted to: `ADMIN`
 - Aliases: `server`

Remove this server from the ignore list.<br/><br/>**Example:**<br/>- `?unignore server` - Stops ignoring the current server

# licenseinfo
 - Usage: `?licenseinfo `
 - Aliases: `licenceinfo`
 - Cooldown: `1 per 180.0 seconds`

Get info about Red's licenses.

