# Tags Help

Create and use tags.<br/><br/>The TagScript documentation can be found [here](https://phen-cogs.readthedocs.io/en/latest/).

# tagsettings
 - Usage: `?tagsettings `
 - Restricted to: `BOT_OWNER`
 - Aliases: `tagset`

Manage Tags cog settings.

## tagsettings settings
 - Usage: `?tagsettings settings `

View Tags settings.

## tagsettings dotparam
 - Usage: `?tagsettings dotparam [true_or_false=None] `

Toggle the TagScript parsing style.<br/><br/>If `dot_parameter` is enabled, TagScript blocks will parse like this:<br/>`{declaration.parameter:payload}`<br/>instead of:<br/>`{declaration(parameter):payload}`

## tagsettings async
 - Usage: `?tagsettings async [true_or_false=None] `

Toggle using the asynchronous TagScript interpreter.<br/><br/>If you aren't a developer or don't know what this is, there's no reason for you to change it.

## tagsettings block
 - Usage: `?tagsettings block `

Manage custom TagScript blocks.

### tagsettings block list
 - Usage: `?tagsettings block list `

List all custom blocks in the TagScript interpreter.

### tagsettings block add
 - Usage: `?tagsettings block add <name> <code> `

Add a custom block to the TagScript interpreter.<br/><br/>The passed code must return a block class that inherits from `TagScriptEngine.Block`.

### tagsettings block show
 - Usage: `?tagsettings block show <name> `

Show the code of a custom block.

### tagsettings block remove
 - Usage: `?tagsettings block remove <name> `
 - Aliases: `delete`

Remove a custom block from the TagScript interpreter.

# migratealias
 - Usage: `?migratealias `
 - Restricted to: `BOT_OWNER`

Migrate the Alias cog's global and server aliases into tags.<br/><br/>This converts all aliases created with the Alias cog into tags with command blocks.<br/>This action cannot be undone.<br/><br/>**Example:**<br/>`?migratealias`

# migratecustomcom
 - Usage: `?migratecustomcom `
 - Restricted to: `BOT_OWNER`
 - Aliases: `migratecustomcommands`

Migrate the CustomCommand cog's server commands into tags.<br/><br/>This converts all custom commands created into tags with the command text as TagScript.<br/>Randomized commands are converted into random blocks.<br/>Commands with converters are converted into indexed args blocks.<br/>This action cannot be undone.<br/><br/>**Example:**<br/>`?migratealias`

# invoketag
 - Usage: `?invoketag <response> <tag_name> [args] `
 - Cooldown: `3 per 30.0 seconds`

Manually invoke a tag with its name and arguments.<br/><br/>Restricting this command with permissions in servers will restrict all members from invoking tags.<br/><br/>**Examples:**<br/>`?invoketag searchitem trophy`<br/>`?invoketag donate`

# tags
 - Usage: `?tags `

View all tags and aliases.<br/><br/>This command will show global tags if run in DMs.<br/><br/>**Example:**<br/>`?tags`

# tag
 - Usage: `?tag `
 - Aliases: `customcom, cc, and alias`
 - Checks: `server_only`

Tag management with TagScript.<br/><br/>These commands use TagScriptEngine.<br/>Read the [TagScript documentation](https://phen-cogs.readthedocs.io/en/latest/) to learn how to use TagScript blocks.

## tag alias
 - Usage: `?tag alias <tag> <alias> `
 - Restricted to: `MOD`

        Add an alias for a tag.<br/><br/>        Adding an alias to the tag will make the tag invokable using the alias or the tag name.<br/>        In the example below, running `?donation` will invoke the `donate` tag.<br/>​<br/>        **Example:**<br/>        `?tag alias donate donation`

## tag raw
 - Usage: `?tag raw <tag> `

Get a tag's raw content.<br/><br/>The sent TagScript will be escaped from Discord style formatting characters.<br/><br/>**Example:**<br/>`?tag raw noping`

## tag search
 - Usage: `?tag search <keyword> `

Search for tags by name.<br/><br/>**Example:**<br/>`?tag search notsupport`

## tag run
 - Usage: `?tag run <tagscript> `
 - Restricted to: `BOT_OWNER`
 - Aliases: `execute`

Execute TagScript without storing.<br/><br/>The variables and actions fields display debugging information.<br/><br/>**Example:**<br/>`?tag run {#:yes,no}`

## tag unalias
 - Usage: `?tag unalias <tag> <alias> `
 - Restricted to: `MOD`

Remove an alias for a tag.<br/><br/>​The tag will still be able to be used under its original name.<br/>You can delete the original tag with the `?tag remove` command.<br/><br/>**Example:**<br/>`tag unalias donate donation`

## tag list
 - Usage: `?tag list `

View all stored tags on this server.<br/><br/>To view info on a specific tag, use `?tag info`.<br/><br/>**Example:**<br/>`?tag list`

## tag usage
 - Usage: `?tag usage `
 - Aliases: `stats`

See tag usage stats.<br/><br/>**Example:**<br/>`?tag usage`

## tag edit
 - Usage: `?tag edit <tag> <tagscript> `
 - Restricted to: `MOD`
 - Aliases: `e`

Edit a tag's TagScript.<br/><br/>The passed tagscript will replace the tag's current tagscript.<br/>View the [TagScript docs](https://phen-cogs.readthedocs.io/en/latest/blocks.html) to find information on how to write valid tagscript.<br/><br/>**Example:**<br/>`?tag edit rickroll Never gonna give you up!`

## tag global
 - Usage: `?tag global `
 - Restricted to: `BOT_OWNER`

Global Tag management with TagScript.<br/><br/>These commands use TagScriptEngine.<br/>Read the [TagScript documentation](https://phen-cogs.readthedocs.io/en/latest/) to learn how to use TagScript blocks.

### tag global alias
 - Usage: `?tag global alias <tag> <alias> `

Add an alias for a global tag.<br/><br/>        Adding an alias to the global tag will make the global tag invokable using the alias or the global tag name.<br/>        In the example below, running `?donation` will invoke the `donate` global tag.<br/>​<br/>        **Example:**<br/>        `?tag global alias donate donation`

### tag global edit
 - Usage: `?tag global edit <tag> <tagscript> `
 - Aliases: `e`

Edit a global tag's TagScript.<br/><br/>The passed tagscript will replace the global tag's current tagscript.<br/>View the [TagScript docs](https://phen-cogs.readthedocs.io/en/latest/blocks.html) to find information on how to write valid tagscript.<br/><br/>**Example:**<br/>`?tag global edit rickroll Never gonna give you up!`

### tag global raw
 - Usage: `?tag global raw <tag> `

Get a global tag's raw content.<br/><br/>The sent TagScript will be escaped from Discord style formatting characters.<br/><br/>**Example:**<br/>`?tag global raw noping`

### tag global list
 - Usage: `?tag global list `

View all stored global tags on this server.<br/><br/>To view info on a specific global tag, use `?tag global info`.<br/><br/>**Example:**<br/>`?tag global list`

### tag global remove
 - Usage: `?tag global remove <tag> `
 - Aliases: `delete and -`

Permanently delete a global tag.<br/><br/>If you want to remove a global tag's alias, use `?tag global unalias`.<br/><br/>**Example:**<br/>`?tag global remove RickRoll`

### tag global search
 - Usage: `?tag global search <keyword> `

Search for global tags by name.<br/><br/>**Example:**<br/>`?tag global search notsupport`

### tag global add
 - Usage: `?tag global add <tag_name> <tagscript> `
 - Aliases: `create and +`

Add a global tag with TagScript.<br/><br/>[Global Tag usage guide](https://phen-cogs.readthedocs.io/en/latest/global tags/blocks.html#usage)<br/><br/>**Example:**<br/>`?tag global add lawsofmotion {embed(title):Newton's Laws of motion}<br/>{embed(description): According to all known laws of aviation, there is no way a bee should be able to fly.}`

### tag global unalias
 - Usage: `?tag global unalias <tag> <alias> `

Remove an alias for a global tag.<br/><br/>​The global tag will still be able to be used under its original name.<br/>You can delete the original global tag with the `?tag global remove` command.<br/><br/>**Example:**<br/>`global tag unalias donate donation`

### tag global append
 - Usage: `?tag global append <tag> <tagscript> `

Add text to a global tag's TagScript.<br/><br/>**Example:**<br/>`?tag global append rickroll Never gonna let you down!`

### tag global pastebin
 - Usage: `?tag global pastebin <tag_name> <link> `
 - Aliases: `++`

Add a global tag with a Pastebin link.<br/><br/>**Example:**<br/>`?tag global pastebin starwarsopeningcrawl https://pastebin.com/CKjn6uYv`

### tag global usage
 - Usage: `?tag global usage `
 - Aliases: `stats`

See global tag usage stats.<br/><br/>**Example:**<br/>`?tag global usage`

## tag process
 - Usage: `?tag process <tagscript> `
 - Restricted to: `BOT_OWNER`

Process a temporary Tag without storing.<br/><br/>This differs from `?tag run` as it creates a fake tag and properly handles actions for all blocks.<br/>The `{args}` block is not supported.<br/><br/>**Example:**<br/>`?tag run {require(Admin):You must be admin to use this tag.} Congrats on being an admin!`

## tag remove
 - Usage: `?tag remove <tag> `
 - Restricted to: `MOD`
 - Aliases: `delete and -`

Permanently delete a tag.<br/><br/>If you want to remove a tag's alias, use `?tag unalias`.<br/><br/>**Example:**<br/>`?tag remove RickRoll`

## tag info
 - Usage: `?tag info <tag> `

Show information about a tag.<br/><br/>You can view meta information for a tag on this server or a global tag.<br/>If a tag on this server has the same name as a global tag, it will show the server tag.<br/><br/>**Example:**<br/>`?tag info notsupport`

## tag docs
 - Usage: `?tag docs [keyword=None] `

Search the TagScript documentation for a block.<br/><br/>https://phen-cogs.readthedocs.io/en/latest/<br/><br/>**Example:**<br/>`?tag docs embed`

## tag pastebin
 - Usage: `?tag pastebin <tag_name> <link> `
 - Restricted to: `MOD`
 - Aliases: `++`

Add a tag with a Pastebin link.<br/><br/>**Example:**<br/>`?tag pastebin starwarsopeningcrawl https://pastebin.com/CKjn6uYv`

## tag add
 - Usage: `?tag add <tag_name> <tagscript> `
 - Restricted to: `MOD`
 - Aliases: `create and +`

Add a tag with TagScript.<br/><br/>[Tag usage guide](https://phen-cogs.readthedocs.io/en/latest/tags/blocks.html#usage)<br/><br/>**Example:**<br/>`?tag add lawsofmotion {embed(title):Newton's Laws of motion}<br/>{embed(description): According to all known laws of aviation, there is no way a bee should be able to fly.}`

## tag append
 - Usage: `?tag append <tag> <tagscript> `
 - Restricted to: `MOD`

Add text to a tag's TagScript.<br/><br/>**Example:**<br/>`?tag append rickroll Never gonna let you down!`

