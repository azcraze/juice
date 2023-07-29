# Timestamp Help

A discord timestamp creator cog.

# timestamp (Hybrid Command)
 - Usage: `?timestamp `
 - Slash Usage: `/timestamp `
 - Aliases: `ts`

Make your very own discord timestamp!

## timestamp timezone (Hybrid Command)
 - Usage: `?timestamp timezone [timezone=None] `
 - Slash Usage: `/timestamp timezone [timezone=None] `
 - Aliases: `tz`

Timezone related commands

### timestamp timezone set (Hybrid Command)
 - Usage: `?timestamp timezone set <timezone> `
 - Slash Usage: `/timestamp timezone set <timezone> `

Set your timezone for conversions<br/><br/>To see the available timezones use the command:<br/>- `?timestamp timezone`<br/><br/>Choose the timezone closest to your actual location for best results.<br/>Timezone names like PST, PT, MDT, MST, etc. are abbreviations and don't<br/>represent the full daylight saving time calculation. Whereas<br/>a timezone like `America/Pacific` Will automatically adjust<br/>for timezones in your location. Unless, of course, you always<br/>follow a timezone like MST.

## timestamp relative (Hybrid Command)
 - Usage: `?timestamp relative <relative_time> `
 - Slash Usage: `/timestamp relative <relative_time> `
 - Aliases: `r`

Produce a timestamp relative to right now.<br/><br/>Example:<br/>    `?ts r in 2 hours`<br/>    Will produce a timestamp 2 hours from the time the command was run.

## timestamp snowflake (Hybrid Command)
 - Usage: `?timestamp snowflake <snowflake> `
 - Slash Usage: `/timestamp snowflake <snowflake> `
 - Aliases: `s`

Produce a snowflake's timestamp<br/><br/>Snowflakes are discord ID's and contain the time of creation within them.<br/>This command can expose that as discord timestamps.<br/><br/>Example:<br/>    `?ts s 218773382617890828`<br/>    Will produce <t:1472230039:F>.

## timestamp absolute (Hybrid Command)
 - Usage: `?timestamp absolute <time> `
 - Slash Usage: `/timestamp absolute <time> `
 - Aliases: `a`

Produce an absolute timestamp.<br/><br/>See `?timestamp timezone` to set your timezone so this is accurate for you.<br/>Usage:<br/>- `year:` The year you want the timestamp to be for. Defaults to current year if not provided.<br/>- `month:` The month you want the timestamp to be for. Defaults to current month if not provided.<br/>- `day:` The day you want the timestamp to be for. Defaults to current day if not provided.<br/>- `hour:` The hour you want the timestamp to be for. Defaults to current hour if not provided.<br/>- `minute:` The minute you want the timestamp to be for. Defaults to 0 if not provided.<br/>- `second:` The second you want the timestamp to be for. Defaults to 0 if not provided.<br/>Example:<br/>    `?ts a year: 2023 month: 7 day: 11 hour: 12`<br/>    Will produce <t:1689076800:F> with no timezone set.

