# SlashTags Help

Create custom slash commands.<br/><br/>The TagScript documentation can be found [here](https://phen-cogs.readthedocs.io/en/latest/index.html).

# slashtag
 - Usage: `?slashtag `
 - Aliases: `st`
 - Checks: `server_only`

Slash Tag management with TagScript.<br/><br/>These commands use TagScriptEngine.<br/>[This site](https://phen-cogs.readthedocs.io/en/latest/index.html) has documentation on how to use TagScript blocks.

## slashtag restore
 - Usage: `?slashtag restore `
 - Restricted to: `BOT_OWNER`

Restore all slash tags from the database.

## slashtag edit
 - Usage: `?slashtag edit <tag> <tagscript> `
 - Restricted to: `MOD`
 - Aliases: `e`

Edit a slash tag.

### slashtag edit argument
 - Usage: `?slashtag edit argument <tag> <argument> `
 - Aliases: `option`

Edit a single slash tag's argument by name.

### slashtag edit tagscript
 - Usage: `?slashtag edit tagscript <tag> <tagscript> `

Edit a slash tag's TagScript.

### slashtag edit name
 - Usage: `?slashtag edit name <tag> <name> `

Edit a slash tag's name.

### slashtag edit description
 - Usage: `?slashtag edit description <tag> <description> `

Edit a slash tag's description.

### slashtag edit arguments
 - Usage: `?slashtag edit arguments <tag> `
 - Aliases: `options`

Edit a slash tag's arguments.<br/><br/>See [this documentation page](https://phen-cogs.readthedocs.io/en/latest/slashtags/slash_arguments.html) for more information on slash tag arguments.

## slashtag info
 - Usage: `?slashtag info <tag> `

Get info about a slash tag that is stored on this server.

## slashtag usage
 - Usage: `?slashtag usage `
 - Aliases: `stats`

See slash tag usage stats.<br/><br/>**Example:**<br/>`?slashtag usage`

## slashtag user
 - Usage: `?slashtag user <tag_name> <tagscript> `
 - Restricted to: `MOD`

Add a user command tag with TagScript.<br/><br/>[Slash tag usage guide](https://phen-cogs.readthedocs.io/en/latest/slashtags/slashtags.html)

## slashtag raw
 - Usage: `?slashtag raw <tag> `

Get a slash tag's raw content.

## slashtag list
 - Usage: `?slashtag list `

View stored slash tags.

## slashtag message
 - Usage: `?slashtag message <tag_name> <tagscript> `
 - Restricted to: `MOD`

Add a message command tag with TagScript.<br/><br/>[Slash tag usage guide](https://phen-cogs.readthedocs.io/en/latest/slashtags/slashtags.html)

## slashtag pastebin
 - Usage: `?slashtag pastebin <tag_name> <link> `
 - Restricted to: `MOD`
 - Aliases: `++`

Add a slash tag with a Pastebin link.

## slashtag clear
 - Usage: `?slashtag clear `
 - Restricted to: `BOT_OWNER`

Clear all slash tags for this server.

## slashtag global
 - Usage: `?slashtag global `
 - Restricted to: `BOT_OWNER`

Global Slash Tag management with TagScript.<br/><br/>These commands use TagScriptEngine.<br/>[This site](https://phen-cogs.readthedocs.io/en/latest/index.html) has documentation on how to use TagScript blocks.

### slashtag global restore
 - Usage: `?slashtag global restore `

Restore all global slash tags from the database.

### slashtag global remove
 - Usage: `?slashtag global remove <tag> `
 - Aliases: `delete and -`

Delete a global slash tag.

### slashtag global list
 - Usage: `?slashtag global list `

View stored global slash tags.

### slashtag global message
 - Usage: `?slashtag global message <tag_name> <tagscript> `
 - Restricted to: `MOD`

Add a message command global tag with TagScript.<br/><br/>[global Slash tag usage guide](https://phen-cogs.readthedocs.io/en/latest/global slashtags/global slashtags.html)

### slashtag global pastebin
 - Usage: `?slashtag global pastebin <tag_name> <link> `
 - Aliases: `++`

Add a global slash tag with a Pastebin link.

### slashtag global raw
 - Usage: `?slashtag global raw <tag> `

Get a global slash tag's raw content.

### slashtag global usage
 - Usage: `?slashtag global usage `
 - Aliases: `stats`

See global slash tag usage stats.<br/><br/>**Example:**<br/>`?slashtag global usage`

### slashtag global edit
 - Usage: `?slashtag global edit <tag> <tagscript> `
 - Aliases: `e`

Edit a global slash tag.

#### slashtag global edit name
 - Usage: `?slashtag global edit name <tag> <name> `

Edit a global slash tag's name.

#### slashtag global edit description
 - Usage: `?slashtag global edit description <tag> <description> `

Edit a global slash tag's description.

#### slashtag global edit arguments
 - Usage: `?slashtag global edit arguments <tag> `
 - Aliases: `options`

Edit a global slash tag's arguments.<br/><br/>See [this documentation page](https://phen-cogs.readthedocs.io/en/latest/global slashtags/slash_arguments.html) for more information on global slash tag arguments.

#### slashtag global edit tagscript
 - Usage: `?slashtag global edit tagscript <tag> <tagscript> `

Edit a global slash tag's TagScript.

#### slashtag global edit argument
 - Usage: `?slashtag global edit argument <tag> <argument> `
 - Aliases: `option`

Edit a single global slash tag's argument by name.

### slashtag global user
 - Usage: `?slashtag global user <tag_name> <tagscript> `
 - Restricted to: `MOD`

Add a user command global tag with TagScript.<br/><br/>[global Slash tag usage guide](https://phen-cogs.readthedocs.io/en/latest/global slashtags/global slashtags.html)

### slashtag global info
 - Usage: `?slashtag global info <tag> `

Get info about a global slash tag that is stored on this server.

### slashtag global add
 - Usage: `?slashtag global add <tag_name> <tagscript> `

Add a global slash tag with TagScript.<br/><br/>[global Slash tag usage guide](https://phen-cogs.readthedocs.io/en/latest/global slashtags/global slashtags.html)

## slashtag remove
 - Usage: `?slashtag remove <tag> `
 - Restricted to: `MOD`
 - Aliases: `delete and -`

Delete a slash tag.

## slashtag add
 - Usage: `?slashtag add <tag_name> <tagscript> `
 - Restricted to: `MOD`
 - Aliases: `create and +`

Add a slash tag with TagScript.<br/><br/>[Slash tag usage guide](https://phen-cogs.readthedocs.io/en/latest/slashtags/slashtags.html)

# slashtagset
 - Usage: `?slashtagset `
 - Restricted to: `BOT_OWNER`
 - Aliases: `slashset`

Manage SlashTags settings.

## slashtagset addeval
 - Usage: `?slashtagset addeval `
 - Checks: `dev_check`

Add a slash eval command for debugging.

## slashtagset rmeval
 - Usage: `?slashtagset rmeval `
 - Checks: `dev_check`

Remove the slash eval command.

## slashtagset appid
 - Usage: `?slashtagset appid [id=None] `

Manually set the application ID for JuiceBot slash commands if it differs from the bot user ID.<br/><br/>This only applies to legacy bots. If you don't know what this means, you don't need to worry about it.

## slashtagset settings
 - Usage: `?slashtagset settings `

View SlashTags settings.

## slashtagset testing
 - Usage: `?slashtagset testing [true_or_false=None] `

Load or unload the SlashTag interaction development test cog.

