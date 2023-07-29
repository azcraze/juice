# CustomHelp Help

A custom customisable help for fun and profit

# chelp
 - Usage: `?chelp `
 - Restricted to: `BOT_OWNER`

Configure your custom help

## chelp ffs
 - Usage: `?chelp ffs `

Attempt to fix, if the uncategorised index tracker messes up

## chelp set
 - Usage: `?chelp set `
 - Aliases: `settings and setting`

Change various help settings

### chelp set timeout
 - Usage: `?chelp set timeout <wait> `

Set how long the help menu must stay active

### chelp set nav
 - Usage: `?chelp set nav <option> `

Enable/Disable navigation arrows<br/>Disabling this removes every trace of arrows and you can't move to the next page<br/>People wanted this for some reason lol

### chelp set deletemessage
 - Usage: `?chelp set deletemessage <toggle> `
 - Aliases: `deleteusermessage`

Delete the user message that started the help menu.<br/>Note: This only works if the bot has permissions to delete the user message, otherwise it's supressed

### chelp set usereply
 - Usage: `?chelp set usereply <option> `
 - Aliases: `usereplies and reply`

Enable/Disable replies

### chelp set type
 - Usage: `?chelp set type `

Toggles between various menus and arrow types

### chelp set thumbnail
 - Usage: `?chelp set thumbnail [url=None] `
 - Aliases: `setthumbnail`

Set your main thumbnail image here.<br/>use `?chelp settings thumbnail` to reset this

### chelp set arrows
 - Usage: `?chelp set arrows [correct_txt] `
 - Aliases: `arrow`

Add custom arrows for fun and profit

## chelp auto
 - Usage: `?chelp auto `

Auto categorise cogs based on it's tags and display them

## chelp info
 - Usage: `?chelp info `

Short info about various themes

## chelp edit
 - Usage: `?chelp edit [yaml_txt] `

Add reactions and descriptions to the category

## chelp load
 - Usage: `?chelp load <theme> <feature> `

Load another preset theme.<br/>Use `?chelp load <theme> all` to load everything from that theme

## chelp refresh
 - Usage: `?chelp refresh `

Force refresh the list of categories, This would reset all the uninstalled/unloaded cogs and will put them into uncategorised.

## chelp reset
 - Usage: `?chelp reset `

Resets all settings to default **custom** help <br/>use `?chelp set 0` to revert back to the old help

### chelp reset hard
 - Usage: `?chelp reset hard `

Hard reset, clear everything

## chelp listthemes
 - Usage: `?chelp listthemes `
 - Aliases: `getthemes`

List the themes and available features

## chelp create
 - Usage: `?chelp create [yaml_txt] `
 - Aliases: `add`

Create a new category to add cogs to it using yaml

## chelp unload
 - Usage: `?chelp unload <feature> `

Unloads the given feature, this will reset to default

## chelp nsfw
 - Usage: `?chelp nsfw `

Add categories to nsfw, only displayed in nsfw channels

### chelp nsfw add
 - Usage: `?chelp nsfw add <category> `

Add categories to the nsfw list

### chelp nsfw remove
 - Usage: `?chelp nsfw remove <category> `

Remove categories from the nsfw list

## chelp reorder
 - Usage: `?chelp reorder [categories] `

This can be used to reorder the categories.<br/><br/>The categories you type are pushed forward while the rest are pushed back.

## chelp list
 - Usage: `?chelp list `

Show the list of categories and the cogs in them

## chelp dev
 - Usage: `?chelp dev `

Add categories to dev, only displayed to the bot owner(s)

### chelp dev remove
 - Usage: `?chelp dev remove <category> `

Remove categories from the dev list

### chelp dev add
 - Usage: `?chelp dev add <category> `

Add categories to the dev list

## chelp toggle
 - Usage: `?chelp toggle <setval> `

Set to toggle custom formatter or the default help formatter<br/>`?chelp toggle 0` to turn custom off <br/>`?chelp toggle 1` to turn it on

## chelp show
 - Usage: `?chelp show `

Show the current help settings

## chelp remove
 - Usage: `?chelp remove `

Remove categories/cogs or everything

### chelp remove cog
 - Usage: `?chelp remove cog <cog_raw_names> `
 - Aliases: `cogs`

Remove a cog(s) from across categories

### chelp remove category
 - Usage: `?chelp remove category <categories> `
 - Aliases: `categories and cat`

Remove multiple categories

### chelp remove all
 - Usage: `?chelp remove all `

This will delete all the categories

# findcategory
 - Usage: `?findcategory <command> `
 - Aliases: `findcat`

Get the category where the command is present

