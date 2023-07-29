# StealEmoji Help

This cog steals emojis and creates servers for them

# stealemoji
 - Usage: `?stealemoji `

Base command for this cog. Check help for the commands list.

## stealemoji clearemojis
 - Usage: `?stealemoji clearemojis [confirm=False] `
 - Restricted to: `BOT_OWNER`

Removes the history of all stolen emojis. Will not delete emojis from server banks

## stealemoji print
 - Usage: `?stealemoji print `
 - Restricted to: `BOT_OWNER`

Prints all the emojis that have been stolen so far

## stealemoji bank
 - Usage: `?stealemoji bank `
 - Restricted to: `BOT_OWNER`
 - Checks: `server_only`

Add or remove current server as emoji bank

## stealemoji collect
 - Usage: `?stealemoji collect `
 - Restricted to: `BOT_OWNER`

Toggles whether emoji's are collected or not

## stealemoji notify
 - Usage: `?stealemoji notify `
 - Restricted to: `BOT_OWNER`

Cycles between notification settings for when an emoji is stolen<br/><br/>None (Default)<br/>DM Owner<br/>Msg in server channel

## stealemoji autobank
 - Usage: `?stealemoji autobank `
 - Restricted to: `BOT_OWNER`

Toggles automatically creating new servers as emoji banks

## stealemoji deleteserver
 - Usage: `?stealemoji deleteserver [server_id=None] `
 - Restricted to: `BOT_OWNER`
 - Aliases: `deleteserver`
 - Checks: `server_only`

Delete servers the bot is the owner of.<br/><br/>Useful for auto-generated serverbanks.

