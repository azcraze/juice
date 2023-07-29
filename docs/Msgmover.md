# Msgmover Help

Move messages around, cross-channels, cross-server!<br/><br/>Run `[p]msgmover` to see more details!<br/><br/>msgcopy: Copy a set # of past messages to another channel/server<br/>msgrelay: Forward all of a channel's messages to another channel/server

# msgmover
 - Usage: `?msgmover `
 - Restricted to: `GUILD_OWNER`

Hi! Thanks for installing msgmover!<br/><br/>Msgmover comes with two key features, both of which use webhooks to move messages from one place to another with a close-to-native feel:<br/><br/>**`?msgcopy`** - Copies a set # of messages from one channel to another *(single-use)*<br/>- *Requires users with **Manage Messages** permissions*<br/><br/>**`?msgrelay`** - Forward messages to other channels/servers *(continuous)*<br/>- *Requires server admins with **Administrator** permissions*<br/><br/>Need help? [Reach us in our Support Discord >](https://coffeebank.github.io/discord)

# msgcopy
 - Usage: `?msgcopy <fromChannel> <toChannel> <maxMessages> [skipMessages=0] `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `msgmove`

Copies messages from one channel to another<br/><br/>toChannel can either be a #channel or a webhook URL.<br/><br/>Retrieve 'maxMessages' number of messages from history, and optionally discard 'skipMessages' number of messages from the retrieved list.<br/><br/>Retrieving more than 10 messages will result in Discord ratelimit throttling, so please be patient.<br/><br/>*Errors? Please [help us by reporting them in our Support Discord >](https://coffeebank.github.io/discord)*

# msgrelay
 - Usage: `?msgrelay `
 - Restricted to: `GUILD_OWNER`

Set message relays<br/><br/>Message relays allow you to forward messages to another server via a webhook.<br/><br/>*[Join the Support Discord for announcements and more info](https://coffeebank.github.io/discord)*

## msgrelay v1
 - Usage: `?msgrelay v1 `
 - Restricted to: `BOT_OWNER`

View legacy data<br/><br/>Settings will not be modifiable, and it is encouraged to migrate to v2.<br/><br/>The new v2 shifts data from being under the Bot Owner to separate servers, and allows server owners to create their own relays.<br/><br/>Because of this change, the old settings are incompatible with the new settings.

### msgrelay v1 reset
 - Usage: `?msgrelay v1 reset <areYouSure> `

⚠️ Deletes all V1 relays<br/><br/>Type **`?msgrelay reset True`** if you're absolutely sure.

## msgrelay edit
 - Usage: `?msgrelay edit <fromChannel> <itemToEdit> <toChannel> `

Edit a message relay<br/><br/>Currently only supports webhook urls. [How to create webhooks.](https://support.discord.com/hc/article_attachments/1500000463501/Screen_Shot_2020-12-15_at_4.41.53_PM.png)<br/>*[Help us develop support for #channels >](https://coffeebank.github.io/discord)*

## msgrelay add
 - Usage: `?msgrelay add <fromChannel> <toChannel> `

Create a message relay<br/><br/>Cross-server relays must be a webhook. [How to create webhooks >](https://support.discord.com/hc/article_attachments/1500000463501/Screen_Shot_2020-12-15_at_4.41.53_PM.png)

## msgrelay delete
 - Usage: `?msgrelay delete <fromChannel> <itemToDelete> `
 - Aliases: `remove`

Delete a message relay<br/><br/>fromChannel: the originating #channel<br/>itemToDelete: put 1, 2, ... for which one you want to delete.<br/><br/>To delete all relays for a fromChannel, set itemToDelete to 0 (zero).

## msgrelay settimer
 - Usage: `?msgrelay settimer <seconds> `

Seconds after the relay checks for edited/deleted messages<br/><br/>To disable checking for edits/deleted messages after sending, set seconds to 0 (zero).

# msgcount
 - Usage: `?msgcount `

Find how many messages it has been after a message<br/><br/>Reply to a message to use this command.

