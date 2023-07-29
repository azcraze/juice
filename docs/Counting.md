# Counting Help

Multifeatured Counting Channel<br/><br/>Create a counting channel for your server, with various additional management options!

# counting
 - Usage: `?counting `
 - Checks: `server_only`

Multifeatured Counting Channel

## counting leaderboard
 - Usage: `?counting leaderboard `
 - Aliases: `top and topcounters`

Show the Counting leaderboard in this server.

## counting highscore
 - Usage: `?counting highscore `
 - Aliases: `score`

Show the highest count reached in this server.

# countingset
 - Usage: `?countingset `
 - Restricted to: `MOD`
 - Checks: `server_only`

Settings for Counting

## countingset allowtext
 - Usage: `?countingset allowtext <true_or_false> `

Set whether messages not starting with a number are allowed.

## countingset delete
 - Usage: `?countingset delete <true_or_false> `

Toggle whether incorrect counts should be deleted.

## countingset autoreset
 - Usage: `?countingset autoreset [message] `

Set the message to be sent on counter reset when a wrong number is sent (leave blank to turn off auto-reset).<br/><br/>The following variables can be included in the message:<br/>- `{author}` for a user mention of the wrong count message's author<br/>- `{count}` for the wrong count number<br/>- `{correct}` for what the count should have been

## countingset clear
 - Usage: `?countingset clear `

Clear & reset the current Counting settings.

## countingset toggle
 - Usage: `?countingset toggle <true_or_false> `

Toggle Counting in this server.

## countingset role
 - Usage: `?countingset role <role> `
 - Restricted to: `ADMIN`

Set the role to assign to the most recent user to count.

## countingset penalty
 - Usage: `?countingset penalty [wrong=None] [mute_time_in_seconds=None] `

Mute users for a specified amount of time if they count wrong x times in a row (leave both values empty to turn off, requires Core `mutes` to be loaded).

## countingset view
 - Usage: `?countingset view `

View the current Counting settings.

## countingset resetcounts
 - Usage: `?countingset resetcounts `

Reset the current Counting scores for all server members.

## countingset react
 - Usage: `?countingset react <true_or_false> `

Toggle whether ✓ and ✗ reactions should be added to messages.

## countingset starting
 - Usage: `?countingset starting <num> `

Set the counter to start off with.

## countingset allowrepeats
 - Usage: `?countingset allowrepeats <true_or_false> `

Toggle whether users can count multiple times in a row.

## countingset assignrole
 - Usage: `?countingset assignrole <true_or_false> `

Toggle whether to assign a role to the most recent user to count (requires add/remove role perms).

## countingset channel
 - Usage: `?countingset channel <channel> `

Set the Counting channel.

