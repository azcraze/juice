# LevelUp Help

Your friendly neighborhood leveling system<br/><br/>Earn experience by chatting in text and voice channels, compare levels with your friends, customize your profile and view various leaderboards!

# stars
 - Usage: `?stars <user> `
 - Aliases: `givestar, addstar, and thanks`
 - Checks: `server_only`

Reward a good noodle<br/>Give a star to a user for being a good noodle

# mocklvl
 - Usage: `?mocklvl [user] `

Test levelup image gen

# myprofile
 - Usage: `?myprofile `
 - Aliases: `mypf and pfset`
 - Checks: `server_only`

Customize your profile colors<br/><br/>Here is a link to google's color picker:<br/>**[Hex Color Picker](https://htmlcolorcodes.com/)**

## myprofile fontpath
 - Usage: `?myprofile fontpath `
 - Restricted to: `BOT_OWNER`

Get folder path for this cog's default backgrounds

## myprofile bgpath
 - Usage: `?myprofile bgpath `
 - Restricted to: `BOT_OWNER`

Get folder path for this cog's default backgrounds

## myprofile fonts
 - Usage: `?myprofile fonts `
 - Cooldown: `1 per 30.0 seconds`

View available fonts to use

## myprofile namecolor
 - Usage: `?myprofile namecolor <hex_color> `
 - Aliases: `name`

Set a hex color for your username<br/><br/>Here is a link to google's color picker:<br/>**[Hex Color Picker](https://htmlcolorcodes.com/)**<br/><br/>Set to `default` to randomize your name color each time you run the command

## myprofile font
 - Usage: `?myprofile font <font_name> `

Set a font for your profile<br/><br/>To view available fonts, type `?myprofile fonts`<br/>To revert to the default font, use `default` for the `font_name` argument

## myprofile statcolor
 - Usage: `?myprofile statcolor <hex_color> `
 - Aliases: `stat`

Set a hex color for your server stats<br/><br/>Here is a link to google's color picker:<br/>**[Hex Color Picker](https://htmlcolorcodes.com/)**<br/><br/>Set to `default` to randomize your name color each time you run the command

## myprofile rembackground
 - Usage: `?myprofile rembackground <filename> `
 - Restricted to: `BOT_OWNER`

Remove a default background from the cog's backgrounds folder

## myprofile addfont
 - Usage: `?myprofile addfont [preferred_filename=None] `
 - Restricted to: `BOT_OWNER`

Add a custom font to the cog from discord<br/><br/>**Arguments**<br/>`preferred_filename` - If a name is given, it will be saved as this name instead of the filename<br/>**Note:** do not include the file extension in the preferred name, it will be added automatically

## myprofile blur
 - Usage: `?myprofile blur `

Toggle a slight blur effect on the background image where the text is displayed.

## myprofile backgrounds
 - Usage: `?myprofile backgrounds `
 - Cooldown: `1 per 30.0 seconds`

View the default backgrounds

## myprofile remfont
 - Usage: `?myprofile remfont <filename> `
 - Restricted to: `BOT_OWNER`

Remove a font from the cog's font folder

## myprofile background
 - Usage: `?myprofile background [image_url=None] `
 - Aliases: `bg`
 - Cooldown: `1 per 30.0 seconds`

Set a background for your profile<br/><br/>This will override your profile banner as the background<br/><br/>**WARNING**<br/>Profile backgrounds are wide landscapes (1050 by 450 pixels) with an aspect ratio of 21:9<br/>Using portrait images will be cropped.<br/><br/>Tip: Googling "dual monitor backgrounds" gives good results for the right images<br/><br/>Here are some good places to look.<br/>[dualmonitorbackgrounds](https://www.dualmonitorbackgrounds.com/)<br/>[setaswall](https://www.setaswall.com/dual-monitor-wallpapers/)<br/>[pexels](https://www.pexels.com/photo/panoramic-photography-of-trees-and-lake-358482/)<br/>[teahub](https://www.teahub.io/searchw/dual-monitor/)<br/><br/>**Additional Options**<br/> - Leave image_url blank to reset back to using your profile banner (or random if you don't have one)<br/> - `random` will randomly select from a pool of default backgrounds each time<br/> - `filename` run `?mypf backgrounds` to view default options you can use by including their filename

## myprofile levelbar
 - Usage: `?myprofile levelbar <hex_color> `
 - Aliases: `lvlbar and bar`

Set a hex color for your level bar<br/><br/>Here is a link to google's color picker:<br/>**[Hex Color Picker](https://htmlcolorcodes.com/)**<br/><br/>Set to `default` to randomize your name color each time you run the command

## myprofile type
 - Usage: `?myprofile type `

Toggle your profile image type (full/slim)<br/><br/>Full size includes your balance, role icon and prestige icon<br/>Slim is a smaller slimmed down version

## myprofile addbackground
 - Usage: `?myprofile addbackground [preferred_filename=None] `
 - Restricted to: `BOT_OWNER`

Add a custom background to the cog from discord<br/><br/>**Arguments**<br/>`preferred_filename` - If a name is given, it will be saved as this name instead of the filename<br/>**Note:** do not include the file extension in the preferred name, it will be added automatically

# pf
 - Usage: `?pf [user] `
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only`

View your profile

# prestige
 - Usage: `?prestige `
 - Checks: `server_only`

Prestige your rank!<br/>Once you have reached this servers prestige level requirement, you can<br/>reset your level and experience to gain a prestige level and any perks associated with it<br/><br/>If you are over level and xp when you prestige, your xp and levels will carry over

# lvltop
 - Usage: `?lvltop <stat> `
 - Aliases: `topstats, membertop, and topranks`
 - Checks: `server_only`

View the Leaderboard<br/><br/>**Arguments**<br/>`stat`: What kind of stat to display the weekly leaderboard for<br/>Valid options are `exp`, `messages`, and `voice`<br/>Abbreviations of those arguments may also be used

# startop
 - Usage: `?startop `
 - Aliases: `starlb`
 - Checks: `server_only`

View the star leaderboard

# weekly
 - Usage: `?weekly <stat> `
 - Checks: `server_only`

View the weekly leaderboard<br/><br/>**Arguments**<br/>`stat`: What kind of stat to display the weekly leaderboard for<br/>Valid options are `exp`, `messages`, `stars`, and `voice`<br/>Abbreviations of those arguments may also be used

# lastweekly
 - Usage: `?lastweekly `
 - Checks: `server_only`

View the last weekly embed

# lvlset
 - Usage: `?lvlset `
 - Aliases: `lset and levelup`
 - Checks: `server_only`

Access LevelUp setting commands

## lvlset setlevel
 - Usage: `?lvlset setlevel <user> <level> `

Set a user to a specific level

## lvlset starmentiondelete
 - Usage: `?lvlset starmentiondelete <deleted_after> `

Toggle whether the bot auto-deletes the star mentions<br/>Set to 0 to disable auto-delete

## lvlset mention
 - Usage: `?lvlset mention `

Toggle levelup mentions<br/>Toggle whether the user in mentioned in LevelUp messages

## lvlset admin
 - Usage: `?lvlset admin `
 - Restricted to: `GUILD_OWNER`

Cog admin commands<br/><br/>Reset levels, backup and restore cog data

### lvlset admin profilecache
 - Usage: `?lvlset admin profilecache <seconds> `
 - Restricted to: `BOT_OWNER`

Set how long to keep profile images in cache<br/>When a user runs the profile command their generated image will be stored in cache to be reused for X seconds<br/><br/>If profile embeds are enabled this setting will have no effect<br/>Anything less than 5 seconds will effectively disable the cache

### lvlset admin globalbackup
 - Usage: `?lvlset admin globalbackup `
 - Restricted to: `BOT_OWNER`

Create a backup of the LevelUp config

### lvlset admin globalreset
 - Usage: `?lvlset admin globalreset `
 - Restricted to: `BOT_OWNER`

Reset cog data for all servers

### lvlset admin serverreset
 - Usage: `?lvlset admin serverreset `

Reset cog data for this server

### lvlset admin cleanup
 - Usage: `?lvlset admin cleanup `
 - Restricted to: `GUILD_OWNER`

Delete users no longer in the server<br/><br/>Also cleans up any missing keys or discrepancies in the config

### lvlset admin statreset
 - Usage: `?lvlset admin statreset `

Reset everyone's exp and level

### lvlset admin view
 - Usage: `?lvlset admin view `

View current loop times and cached data

### lvlset admin importmee6
 - Usage: `?lvlset admin importmee6 <import_by> <replace> <include_settings> <i_agree> `
 - Restricted to: `GUILD_OWNER`

Import levels and exp from MEE6<br/><br/>**Make sure your server's leaderboard is public!**<br/><br/>**Arguments**<br/>`import_by` - which stat to prioritize (`level` or `exp`)<br/>If exp is entered, it will import their experience and base their new level off of that.<br/>If level is entered, it will import their level and calculate their exp based off of that.<br/>`replace` - (True/False) if True, it will replace the user's exp or level, otherwise it will add it<br/>`include_settings` - import level roles and exp settings from MEE6<br/>`i_agree` - (Yes/No) Just an extra option to make sure you want to execute this command<br/><br/>**Note**<br/>Instead of typing true/false<br/>1 = True<br/>0 = False

### lvlset admin rendergifs
 - Usage: `?lvlset admin rendergifs `
 - Restricted to: `BOT_OWNER`

Toggle whether to render profiles as gifs if the user's discord profile is animated

### lvlset admin globalrestore
 - Usage: `?lvlset admin globalrestore `
 - Restricted to: `BOT_OWNER`

Restore a global backup<br/><br/>Attach the .json file to the command message to import

### lvlset admin serverrestore
 - Usage: `?lvlset admin serverrestore `
 - Restricted to: `GUILD_OWNER`

Restore a server backup<br/><br/>Attach the .json file to the command message to import

### lvlset admin serverbackup
 - Usage: `?lvlset admin serverbackup `
 - Restricted to: `BOT_OWNER`

Create a backup of the LevelUp config

### lvlset admin importfixator
 - Usage: `?lvlset admin importfixator <i_agree> `
 - Restricted to: `BOT_OWNER`

Import data from Fixator's Leveler cog<br/><br/>This will overwrite existing LevelUp level data and stars<br/>It will also import XP range level roles, and ignored channels<br/>*Obviously you will need MongoDB running while you run this command*

### lvlset admin importmalarne
 - Usage: `?lvlset admin importmalarne <import_by> <replace> <i_agree> `
 - Restricted to: `BOT_OWNER`

Import levels and exp from Malarne's Leveler cog<br/><br/>**Arguments**<br/>`export_by` - which stat to prioritize (`level` or `exp`)<br/>If exp is entered, it will import their experience and base their new level off of that.<br/>If level is entered, it will import their level and calculate their exp based off of that.<br/>`replace` - (True/False) if True, it will replace the user's exp or level, otherwise it will add it<br/>`i_agree` - (Yes/No) Just an extra option to make sure you want to execute this command

## lvlset starmention
 - Usage: `?lvlset starmention `

Toggle star reaction mentions<br/>Toggle whether the bot mentions that a user reacted to a message with a star

## lvlset algorithm
 - Usage: `?lvlset algorithm `

Customize the leveling algorithm for your server

### lvlset algorithm exp
 - Usage: `?lvlset algorithm exp <exponent_multiplier> `

Exponent multiplier for the leveling algorithm<br/><br/>Affects leveling on an exponential scale(higher values makes leveling take exponentially longer)

### lvlset algorithm base
 - Usage: `?lvlset algorithm base <base_multiplier> `

Base multiplier for the leveling algorithm<br/><br/>Affects leveling on a more linear scale(higher values makes leveling take longer)

## lvlset levelchannel
 - Usage: `?lvlset levelchannel [levelup_channel=None] `

Set LevelUP message channel<br/>Set a channel for all level up messages to send to

## lvlset addxp
 - Usage: `?lvlset addxp <user_or_role> <xp> `

Add XP to a user or role

## lvlset ignored
 - Usage: `?lvlset ignored `

Base command for all ignore lists

### lvlset ignored channel
 - Usage: `?lvlset ignored channel <channel> `

Add/Remove a channel in the ignore list<br/>Channels in the ignore list don't gain XP<br/><br/>Use the command with a channel already in the ignore list to remove it

### lvlset ignored role
 - Usage: `?lvlset ignored role <role> `

Add/Remove a role from the ignore list<br/>Roles in the ignore list don't gain XP<br/><br/>Use the command with a role already in the ignore list to remove it

### lvlset ignored server
 - Usage: `?lvlset ignored server <server_id> `
 - Restricted to: `BOT_OWNER`

Add/Remove a server in the ignore list<br/><br/>**THIS IS A GLOBAL SETTING ONLY BOT OWNERS CAN USE**<br/><br/>Use the command with a server already in the ignore list to remove it

### lvlset ignored member
 - Usage: `?lvlset ignored member <member> `

Add/Remove a member from the ignore list<br/>Members in the ignore list don't gain XP<br/><br/>Use the command with a member already in the ignore list to remove them

## lvlset seelevels
 - Usage: `?lvlset seelevels `

Test the level algorithm<br/>View the first 20 levels using the current algorithm to test experience curve

## lvlset showbalance
 - Usage: `?lvlset showbalance `

Toggle whether to show user's economy credit balance in their profile

## lvlset view
 - Usage: `?lvlset view `

View all LevelUP settings

## lvlset setprestige
 - Usage: `?lvlset setprestige <user> <prestige> `

Set a user to a specific prestige level<br/><br/>Prestige roles will need to be manually added/removed when using this command

## lvlset voice
 - Usage: `?lvlset voice `

Voice settings

### lvlset voice streambonus
 - Usage: `?lvlset voice streambonus <min_xp> <max_xp> `

Add a range of bonus XP to users who are Discord streaming<br/><br/>This bonus applies to voice time xp<br/><br/>Set both min and max to 0 to remove the bonus

### lvlset voice channelbonus
 - Usage: `?lvlset voice channelbonus <channel> <min_xp> <max_xp> `

Add a range of bonus XP to apply to certain channels<br/><br/>This bonus applies to voice time xp<br/><br/>Set both min and max to 0 to remove the role bonus

### lvlset voice deafened
 - Usage: `?lvlset voice deafened `

Ignore deafened voice users<br/>Toggle whether deafened users in a voice channel can gain voice XP

### lvlset voice rolebonus
 - Usage: `?lvlset voice rolebonus <role> <min_xp> <max_xp> `

Add a range of bonus XP to apply to certain roles<br/><br/>This bonus applies to voice time xp<br/><br/>Set both min and max to 0 to remove the role bonus

### lvlset voice xp
 - Usage: `?lvlset voice xp <voice_xp> `

Set voice XP gain<br/>Sets the amount of XP gained per minute in a voice channel (default is 2)

### lvlset voice solo
 - Usage: `?lvlset voice solo `

Ignore solo voice users<br/>Toggle whether solo users in a voice channel can gain voice XP

### lvlset voice muted
 - Usage: `?lvlset voice muted `

Ignore muted voice users<br/>Toggle whether self-muted users in a voice channel can gain voice XP

### lvlset voice invisible
 - Usage: `?lvlset voice invisible `

Ignore invisible voice users<br/>Toggle whether invisible users in a voice channel can gain voice XP

## lvlset barlength
 - Usage: `?lvlset barlength <bar_length> `

Set the progress bar length for embed profiles

## lvlset roles
 - Usage: `?lvlset roles `
 - Restricted to: `ADMIN`

Level role assignment

### lvlset roles autoremove
 - Usage: `?lvlset roles autoremove `

Automatic removal of previous level roles

### lvlset roles del
 - Usage: `?lvlset roles del <level> `

Assign a role to a level

### lvlset roles initialize
 - Usage: `?lvlset roles initialize `

Initialize level roles<br/><br/>This command is for if you added level roles after users have achieved that level,<br/>it will apply all necessary roles to a user according to their level and prestige

### lvlset roles add
 - Usage: `?lvlset roles add <level> <role> `

Assign a role to a level

## lvlset prestige
 - Usage: `?lvlset prestige `

Level Prestige Settings

### lvlset prestige level
 - Usage: `?lvlset prestige level <level> `

Set the level required to prestige<br/>Set to 0 to disable prestige

### lvlset prestige del
 - Usage: `?lvlset prestige del <prestige_level> `

Delete a prestige level role

### lvlset prestige autoremove
 - Usage: `?lvlset prestige autoremove `

Automatic removal of previous prestige level roles

### lvlset prestige add
 - Usage: `?lvlset prestige add <prestige_level> <role> <emoji> `

Add a prestige level role<br/>Add a role and emoji associated with a specific prestige level<br/><br/>When a user prestiges, they will get that role and the emoji will show on their profile

## lvlset dm
 - Usage: `?lvlset dm `

Toggle DM notifications<br/>Toggle whether LevelUp messages are DM'd to the user

## lvlset messages
 - Usage: `?lvlset messages `
 - Aliases: `message and msg`

Message settings

### lvlset messages channelbonus
 - Usage: `?lvlset messages channelbonus <channel> <min_xp> <max_xp> `

Add a range of bonus XP to apply to certain channels<br/><br/>This bonus applies to message xp<br/><br/>Set both min and max to 0 to remove the role bonus

### lvlset messages length
 - Usage: `?lvlset messages length <minimum_length> `

Set minimum message length for XP<br/>Minimum length a message must be to count towards XP gained<br/><br/>Set to 0 to disable

### lvlset messages xp
 - Usage: `?lvlset messages xp [min_xp=3] [max_xp=6] `

Set message XP range<br/>Set the Min and Max amount of XP that a message can gain

### lvlset messages rolebonus
 - Usage: `?lvlset messages rolebonus <role> <min_xp> <max_xp> `

Add a range of bonus XP to apply to certain roles<br/><br/>This bonus applies to message xp<br/><br/>Set both min and max to 0 to remove the role bonus

### lvlset messages cooldown
 - Usage: `?lvlset messages cooldown <cooldown> `

Cooldown threshold for message XP<br/><br/>When a user sends a message they will have to wait X seconds before their message<br/>counts as XP gained

## lvlset levelnotify
 - Usage: `?lvlset levelnotify `

Toggle the level up message when a user levels up

## lvlset starcooldown
 - Usage: `?lvlset starcooldown <time_in_seconds> `

Set the star cooldown<br/><br/>Users can give another user a star every X seconds

## lvlset embeds
 - Usage: `?lvlset embeds `

Toggle using embeds or generated pics

# etest
 - Usage: `?etest <emoji> `

Test emojis to see if the bot is able to get a valid url for them

# weeklyset
 - Usage: `?weeklyset `
 - Aliases: `wset`
 - Checks: `server_only`

Access the weekly settings for levelUp

## weeklyset toggle
 - Usage: `?weeklyset toggle `

Toggle weekly stat tracking

## weeklyset roleall
 - Usage: `?weeklyset roleall `

Toggle whether to give the weekly winner role to all winners or only 1st place

## weeklyset view
 - Usage: `?weeklyset view `

View the current weekly settings

## weeklyset hour
 - Usage: `?weeklyset hour <hour> `

What hour the weekly stats reset<br/>Set the hour (0 - 23 in UTC) for the weekly reset to take place

## weeklyset day
 - Usage: `?weeklyset day <day_of_the_week> `

What day of the week the weekly stats reset<br/>Set the day of the week (0 - 6 = Monday - Sunday) for weekly reset to take place

## weeklyset role
 - Usage: `?weeklyset role <role> `

Weekly winner role reward<br/>Set the role awarded to the top member of the weekly leaderboard

## weeklyset bonus
 - Usage: `?weeklyset bonus <exp_bonus> `

Weekly winners bonus experience points<br/>Set to 0 to disable exp bonus

## weeklyset reset
 - Usage: `?weeklyset reset <yes_or_no> `

Reset the weekly leaderboard manually and announce winners

## weeklyset channel
 - Usage: `?weeklyset channel <channel> `

Weekly winner announcement channel<br/>set the channel for weekly winners to be announced in when auto-reset is enabled

## weeklyset autoremove
 - Usage: `?weeklyset autoremove `

One role holder at a time<br/>Toggle whether the winner role is removed from the previous holder when a new winner is selected

## weeklyset top
 - Usage: `?weeklyset top <top_count> `

Top weekly member count<br/>Set amount of members to include in the weekly top leaderboard

## weeklyset autoreset
 - Usage: `?weeklyset autoreset `

Toggle weekly auto-reset

# mocklvlup
 - Usage: `?mocklvlup [person] `
 - Restricted to: `BOT_OWNER`
 - Checks: `server_only`

Force level a user or yourself

# mocklvldown
 - Usage: `?mocklvldown [person] `
 - Restricted to: `BOT_OWNER`
 - Checks: `server_only`

Force de-level a user or yourself

# forceinit
 - Usage: `?forceinit `
 - Restricted to: `BOT_OWNER`

Force Initialization

# forcesave
 - Usage: `?forcesave `
 - Restricted to: `BOT_OWNER`

Force save the cache

