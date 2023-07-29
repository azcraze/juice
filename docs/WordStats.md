# WordStats Help

Tracks commonly used words.

# wordstats
 - Usage: `?wordstats [member_or_server=None] [amount_or_word=30] `
 - Checks: `server_only`

Prints the most commonly used words.<br/><br/>Use the optional parameter "member_or_server" to see the stats of a member or server.<br/>Use the optional parameter "amount_or_word" to change the number of words that are displayed or to check the stats of a specific word.

## wordstats global
 - Usage: `?wordstats global [amount_or_word=30] `

Prints the most commonly used words across all servers.<br/><br/>Use the optional parameter "amount_or_word" to change the number of words that are displayed or to check the stats of a specific word.

# topchatters
 - Usage: `?topchatters [server=None] [word=None] [amount=10] `
 - Checks: `server_only`

Prints the members who have said the most words.<br/><br/>Use the optional parameter "server" to see the topchatters in a specific server.<br/>Use the optional parameter "word" to see the topchatters of a specific word.<br/>Use the optional parameter "amount" to change the number of members that are displayed.

## topchatters global
 - Usage: `?topchatters global [word=None] [amount=10] `

Prints the members who have said the most words across all servers.<br/><br/>Use the optional parameter "word" to see the topchatters of a specific word.<br/>Use the optional parameter "amount" to change the number of members that are displayed.

# topratio
 - Usage: `?topratio <word> [server=None] [amount=10] [min_total=0] `
 - Checks: `server_only`

Prints the members with the highest "word to all words" ratio.<br/><br/>Use the parameter "word" to set the word to compare.<br/>Use the optional parameter "server" to see the ratio in a specific server.<br/>Use the optional parameter "amount" to change the number of members that are displayed.<br/>Use the optional parameter "min_total" to change the minimum number of words a user needs to have said to be shown.

## topratio global
 - Usage: `?topratio global <word> [amount=10] [min_total=0] `

Prints the members with the highest "word to all words" ratio in all servers.<br/><br/>Use the parameter "word" to set the word to compare.<br/>Use the optional parameter "amount" to change the number of members that are displayed.<br/>Use the optional parameter "min_total" to change the minimum number of words a user needs to have said to be shown.

# wordstatsset
 - Usage: `?wordstatsset `

Config options for wordstats.

## wordstatsset convert
 - Usage: `?wordstatsset convert `
 - Restricted to: `BOT_OWNER`

Convert data from config to the SQLite database.

## wordstatsset channel
 - Usage: `?wordstatsset channel [value=None] `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Set if wordstats should record stats for this channel.<br/><br/>Defaults to True.<br/>This value is channel specific.

## wordstatsset minlength
 - Usage: `?wordstatsset minlength [value=None] `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Set the minimum length a word has to be in order to be displayed.<br/><br/>Shorter words will still be included in numerical counts, they will only be hidden from list displays.<br/>Set to 0 to disable.<br/>Defaults to 0.<br/>This value is server specific.

## wordstatsset server
 - Usage: `?wordstatsset server [value=None] `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Set if wordstats should record stats for this server.<br/><br/>Defaults to True.<br/>This value is server specific.

## wordstatsset forgetme
 - Usage: `?wordstatsset forgetme `

Make wordstats forget all data about you.<br/><br/>This is equivalent to `?mydata forgetme`, but only for wordstats.<br/>This cannot be undone.

## wordstatsset user
 - Usage: `?wordstatsset user [value=None] `

Set if wordstats should record stats for you.<br/><br/>Defaults to True.<br/>This value is user specific.

## wordstatsset stopwords
 - Usage: `?wordstatsset stopwords [value=None] `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Set if stopwords should be included in outputs.<br/><br/>Stopwords are common words such as "a", "it" and "the".<br/>Stopwords will still be included in numerical counts, they will only be hidden from list displays.<br/>Defaults to True.<br/>This value is server specific.

## wordstatsset deleteall
 - Usage: `?wordstatsset deleteall [confirm=False] `
 - Restricted to: `BOT_OWNER`

Delete all wordstats data.<br/><br/>This removes all existing data, creating a blank state.<br/>This cannot be undone.

