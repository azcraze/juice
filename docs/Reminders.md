# Reminders Help

Don't forget anything anymore! Reminders in DMs, channels, FIFO commands scheduler, say scheduler... With 'Me Too', snooze and buttons.

# remindme (Hybrid Command)
 - Usage: `?remindme <time> [message_or_text] `
 - Slash Usage: `/remindme <time> [message_or_text] `

Create a reminder with optional reminder text or message.<br/><br/>The specified time can be fuzzy parsed or use the kwargs `in`, `on` and `every` to find a repeat rule and your text.<br/>You don't have to put quotes around the time argument. For more precise parsing, you can place quotation marks around the text. Put quotation marks around the time too, if it contains spaces.<br/>Use `?reminder timetips` to display tips for time parsing.<br/><br/>**Examples:**<br/>- `?remindme in 8min45sec to do that thing`<br/>- `?remindme to water my plants in 2 hours`<br/>- `?remindme in 3 days`<br/>- `?remindme 8h`<br/>- `?remindme every 1 week to take out the trash`<br/>- `?remindme in 1 hour <message_link>`<br/>- `?remindme at 10h to add some feature to my codes`

# remind (Hybrid Command)
 - Usage: `?remind <destination> <targets> <time> [message_or_text] `
 - Slash Usage: `/remind <destination> <targets> <time> [message_or_text] `
 - Checks: `server_only`

Create a reminder with optional reminder text or message, in a channel with an user/role ping.<br/><br/>The specified time can be fuzzy parsed or use the kwargs `in`, `on` and `every` to find a repeat rule and your text.<br/>You don't have to put quotes around the time argument. For more precise parsing, you can place quotation marks around the text. Put quotation marks around the time too, if it contains spaces.<br/>Use `?reminder timetips` to display tips for time parsing.<br/><br/>Examples:<br/>- `?remind #destination @user1 @user2 @user2 in 2 hours to buy a gift`

# reminder (Hybrid Command)
 - Usage: `?reminder `
 - Slash Usage: `/reminder `
 - Aliases: `reminders`

List, edit and delete existing reminders, or create FIFO/commands or Say reminders.

## reminder timezone (Hybrid Command)
 - Usage: `?reminder timezone <timezone> `
 - Slash Usage: `/reminder timezone <timezone> `

Set your timezone for the time converter.<br/><br/>`Europe/Paris`, `America/New_York`...

## reminder timetips (Hybrid Command)
 - Usage: `?reminder timetips `
 - Slash Usage: `/reminder timetips `
 - Aliases: `parsingtips`

Show time parsing tips.

## reminder edit (Hybrid Command)
 - Usage: `?reminder edit <reminder> `
 - Slash Usage: `/reminder edit <reminder> `

Edit an existing Reminder from its ID.<br/><br/>- Use `last` to edit your last created reminder.<br/>- Use `next` to edit your next triggered reminder.

## reminder text (Hybrid Command)
 - Usage: `?reminder text <reminder> <text> `
 - Slash Usage: `/reminder text <reminder> <text> `

Edit the text of an existing Reminder from its ID.<br/><br/>- Use `last` to edit your last created reminder.<br/>- Use `next` to edit your next triggered reminder.

## reminder clear (Hybrid Command)
 - Usage: `?reminder clear [confirmation=False] `
 - Slash Usage: `/reminder clear [confirmation=False] `

Clear all your existing reminders.

## reminder remove (Hybrid Command)
 - Usage: `?reminder remove <reminders> `
 - Slash Usage: `/reminder remove <reminders> `
 - Aliases: `delete and -`

Remove existing Reminder(s) from their IDs.<br/><br/>- Use `last` to remove your last created reminder.<br/>- Use `next` to remove your next triggered reminder.

## reminder expires (Hybrid Command)
 - Usage: `?reminder expires <reminder> <time> `
 - Slash Usage: `/reminder expires <reminder> <time> `
 - Aliases: `expiresat`

Edit the expires time of an existing Reminder from its ID.<br/><br/>- Use `last` to edit your last created reminder.<br/>- Use `next` to edit your next triggered reminder.<br/>It's the same converter as for creation, but without the option of repetition.

## reminder list (Hybrid Command)
 - Usage: `?reminder list [card=False] [content_type=None] [sort=expire] `
 - Slash Usage: `/reminder list [card=False] [content_type=None] [sort=expire] `

List your existing reminders.<br/><br/>Sort options:<br/>- `expire`: Display them in order of next triggering.<br/>- `created`: Display them in order of creating.<br/>- `id`: Display them in order of their ID.

## reminder repeat (Hybrid Command)
 - Usage: `?reminder repeat <reminder> <repeat> `
 - Slash Usage: `/reminder repeat <reminder> <repeat> `

Edit the repeat of an existing Reminder from its ID.<br/><br/>- Use `last` to edit your last created reminder.<br/>- Use `next` to edit your next triggered reminder.<br/><br/>Allowed **intervals** are:<br/>• `years`/`year`/`y`<br/>• `months`/`month`/`mo`<br/>• `weeks`/`week`/`w`<br/>• `days`/`day`/`d`<br/>• `hours`/`hour`/`hrs`/`hr`/`h`<br/>• `minutes`/`minute`/`mins`/`min`/`m`<br/><br/>You can combine **relative intervals** like this:<br/>• `1y 1mo 2 days -5h`

## reminder say (Hybrid Command)
 - Usage: `?reminder say <destination> <time> <text> `
 - Slash Usage: `/reminder say <destination> <time> <text> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `server_only`

Create a reminder who will say/send text.<br/><br/>The specified time can be fuzzy parsed or use the kwargs `in`, `on` and `every` to find a repeat rule and your text.<br/>You don't have to put quotes around the time argument. For more precise parsing, you can place quotation marks around the text. Put quotation marks around the time too, if it contains spaces.<br/>Use `?reminder timetips` to display tips for time parsing.<br/><br/>Examples:<br/>- `?reminder say #destination "at 9h every day" Hello everyone!

## reminder fifo (Hybrid Command)
 - Usage: `?reminder fifo <destination> <time> <command> `
 - Slash Usage: `/reminder fifo <destination> <time> <command> `
 - Restricted to: `ADMIN`
 - Aliases: `command`
 - Checks: `server_only`

Create a FIFO/command reminder. The chosen command will be executed with you as invoker. Don't provide the prefix.<br/><br/>The specified time can be fuzzy parsed or use the kwargs `in`, `on` and `every` to find a repeat rule and your text.<br/>You don't have to put quotes around the time argument. For more precise parsing, you can place quotation marks around the text. Put quotation marks around the time too, if it contains spaces.<br/>Use `?reminder timetips` to display tips for time parsing.<br/><br/>Examples:<br/>- `?reminder fifo #destination "at 10h every day" ping

# setreminders (Hybrid Command)
 - Usage: `?setreminders `
 - Slash Usage: `/setreminders `
 - Restricted to: `BOT_OWNER`

Configure Reminders.

## setreminders migratefromfifo (Hybrid Command)
 - Usage: `?setreminders migratefromfifo `
 - Slash Usage: `/setreminders migratefromfifo `

Migrate Reminders from FIFO by Fox.

## setreminders metoo (Hybrid Command)
 - Usage: `?setreminders metoo <value> `
 - Slash Usage: `/setreminders metoo <value> `

Show a `Me too` button in reminders.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setreminders repeatallowed (Hybrid Command)
 - Usage: `?setreminders repeatallowed <value> `
 - Slash Usage: `/setreminders repeatallowed <value> `

Enable or disabled repeat option for users.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setreminders clearuserreminders (Hybrid Command)
 - Usage: `?setreminders clearuserreminders <user> [confirmation=False] `
 - Slash Usage: `/setreminders clearuserreminders <user> [confirmation=False] `

Clear all existing reminders for a user.

## setreminders migratefromremindme (Hybrid Command)
 - Usage: `?setreminders migratefromremindme `
 - Slash Usage: `/setreminders migratefromremindme `

Migrate Reminders from RemindMe by PhasecoreX.

## setreminders maximumuserreminders (Hybrid Command)
 - Usage: `?setreminders maximumuserreminders <value> `
 - Slash Usage: `/setreminders maximumuserreminders <value> `

Change the reminders limit for a user.<br/><br/>Default value: 20<br/>Dev: Range[int, 1, 125]

## setreminders fifoallowed (Hybrid Command)
 - Usage: `?setreminders fifoallowed <value> `
 - Slash Usage: `/setreminders fifoallowed <value> `

Allow or deny commands reminders for users (except bot owners).<br/><br/>Default value: False<br/>Dev: <class 'bool'>

## setreminders modalconfig (Hybrid Command)
 - Usage: `?setreminders modalconfig [confirmation=False] `
 - Slash Usage: `/setreminders modalconfig [confirmation=False] `
 - Aliases: `configmodal`

Set all settings for the cog with a Discord Modal.

## setreminders minimumrepeat (Hybrid Command)
 - Usage: `?setreminders minimumrepeat <value> `
 - Slash Usage: `/setreminders minimumrepeat <value> `

Change the minimum minutes number for a repeat time.<br/><br/>Default value: 60<br/>Dev: Range[int, 10, None]

## setreminders getdebugloopsstatus (Hybrid Command)
 - Usage: `?setreminders getdebugloopsstatus `
 - Slash Usage: `/setreminders getdebugloopsstatus `

Get an embed to check loops status.

## setreminders showsettings (Hybrid Command)
 - Usage: `?setreminders showsettings [with_dev=False] `
 - Slash Usage: `/setreminders showsettings [with_dev=False] `

Show all settings for the cog with defaults and values.

## setreminders snoozeview (Hybrid Command)
 - Usage: `?setreminders snoozeview <value> `
 - Slash Usage: `/setreminders snoozeview <value> `

Send Snooze view/buttons when reminders sending.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setreminders resetsetting (Hybrid Command)
 - Usage: `?setreminders resetsetting <setting> `
 - Slash Usage: `/setreminders resetsetting <setting> `

Reset a setting.

## setreminders creationview (Hybrid Command)
 - Usage: `?setreminders creationview <value> `
 - Slash Usage: `/setreminders creationview <value> `

Send Creation view/buttons when reminders creation.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

