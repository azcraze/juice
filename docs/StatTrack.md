# StatTrack Help

Track your bot's metrics and view them in Discord.<br/>This cog creates its own SQLite database to store data, using around 150KB per day.<br/><br/>Commands will output as a graph.<br/>Data can also be exported with `[p]stattrack export` into a few different formats.

# stattrack
 - Usage: `?stattrack `
 - Cooldown: `10 per 60.0 seconds`

View my stats.

## stattrack debug
 - Usage: `?stattrack debug `
 - Restricted to: `BOT_OWNER`

View debug info for the last plot.<br/><br/>This is for development purposes only.

## stattrack latency
 - Usage: `?stattrack latency [timespan=1 day, 0:00:00] `
 - Aliases: `ping`

Get my latency stats.<br/><br/>**Arguments**<br/><br/>`<timespan>` How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>**Examples:**<br/>- `?stattrack latency 3w2d`<br/>- `?stattrack latency 5d`<br/>- `?stattrack latency all`

## stattrack messages
 - Usage: `?stattrack messages [timespan=1 day, 0:00:00] `

Get message stats.<br/><br/>**Arguments**<br/><br/>`<timespan>` How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>**Examples:**<br/>- `?stattrack messages 3w2d`<br/>- `?stattrack messages 5d`<br/>- `?stattrack messages all`

## stattrack users
 - Usage: `?stattrack users [timespan=1 day, 0:00:00] <metrics> `

Get user stats.<br/><br/>You can just run this command on its own to see all metrics,<br/>or specify some metrics - see below.<br/><br/>**Arguments**<br/><br/>`[timespan]` How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>`[metrics]` The metrics to show. Valid options: `total`, `unique`, `humans`, `bots`.<br/>Defaults to all of them.<br/><br/>Note that `total` will count users multiple times if they share multiple servers with the<br/>JuiceBot, while `unique` will only count them once.<br/><br/>**Examples:**<br/>- `?stattrack users` - show all metrics, 1 day<br/>- `?stattrack users 3w2d` - show all metrics, 3 weeks 2 days<br/>- `?stattrack users 5d total unique` - show total & unique, 5 days<br/>- `?stattrack users all humans bots` - show humans & bots, all time

## stattrack channels
 - Usage: `?stattrack channels [timespan=1 day, 0:00:00] <metrics> `

Get channel stats.<br/><br/>You can just run this command on its own to see all metrics,<br/>or specify some metrics - see below.<br/><br/>**Arguments**<br/><br/>`[timespan]` How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>`[metrics]` The metrics to show.<br/>Valid options: `total`, `text`, `voice`, `stage`, `category`.<br/>Defaults to all of them.<br/><br/>Note that `total` will count users multiple times if they share multiple servers with the<br/>JuiceBot, while `unique` will only count them once.<br/><br/>**Examples:**<br/>**Examples:**<br/>- `?stattrack servers 3w2d`<br/>- `?stattrack servers 5d`<br/>- `?stattrack servers all`

## stattrack devimport
 - Usage: `?stattrack devimport `
 - Restricted to: `BOT_OWNER`

Import data from a JSON string, orient "split".<br/><br/>This is for development purposes only.<br/><br/>Please attack a `.json` file.

## stattrack commands
 - Usage: `?stattrack commands [timespan=1 day, 0:00:00] `

Get command usage stats.<br/><br/>**Arguments**<br/><br/>`<timespan>` How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>**Examples:**<br/>- `?stattrack commands 3w2d`<br/>- `?stattrack commands 5d`<br/>- `?stattrack commands all`

## stattrack status
 - Usage: `?stattrack status [timespan=1 day, 0:00:00] <metrics> `

Get status stats.<br/><br/>You can just run this command on its own to see all metrics,<br/>or specify some metrics - see below.<br/><br/>**Arguments**<br/><br/>`[timespan]` How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>`[metrics]` The metrics to show. Valid options: `online`, `idle`, `offline`, `dnd`.<br/>Defaults to all of them.<br/><br/>**Examples:**<br/>- `?stattrack status` - show all metrics, 1 day<br/>- `?stattrack status 3w2d` - show all metrics, 3 weeks 2 days<br/>- `?stattrack status 5d dnd online` - show dnd & online, 5 days<br/>- `?stattrack status all online idle` - show online & idle, all time

## stattrack system
 - Usage: `?stattrack system `
 - Aliases: `sys`

Get system metrics.

### stattrack system cpu
 - Usage: `?stattrack system cpu [timespan=1 day, 0:00:00] `

Get CPU stats.<br/><br/>**Arguments**<br/><br/><timespan> How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>**Examples:**<br/>- `?stattrack system cpu 3w2d`<br/>- `?stattrack system cpu 5d`<br/>- `?stattrack system cpu all`

### stattrack system mem
 - Usage: `?stattrack system mem [timespan=1 day, 0:00:00] `
 - Aliases: `memory and ram`

Get memory usage stats.<br/><br/>**Arguments**<br/><br/><timespan> How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>**Examples:**<br/>- `?stattrack system mem 3w2d`<br/>- `?stattrack system mem 5d`<br/>- `?stattrack system mem all`

## stattrack export
 - Usage: `?stattrack export `
 - Restricted to: `BOT_OWNER`

Export stattrack data.

### stattrack export json
 - Usage: `?stattrack export json `

Export as JSON with pandas orient "split" 

### stattrack export csv
 - Usage: `?stattrack export csv `

Export as CSV

## stattrack maxpoints
 - Usage: `?stattrack maxpoints <maxpoints> `
 - Restricted to: `BOT_OWNER`

Set the maximum number of points to plot. This affects the speed of graph plotting.<br/><br/>The default value is 25k (25000).<br/><br/>The more points you plot, the slower the plotting time will be.<br/><br/>This setting only affects graphs that are a longer timespan (1 month+).<br/><br/>Set maxpoints to -1 to disable this feature, therefore always plotting all points.<br/><br/>Otherwise, maxpoints must be at least 1k (1440).<br/><br/>**Examples:**<br/>- `?stattrack maxpoints 10000` - plot up to 10k points<br/>- `?stattrack maxpoints 75000` - plot up to 75k points<br/>- `?stattrack maxpoints 1440` - the minimum value possible<br/>- `?stattrack maxpoints 25000` - the default value<br/>- `?stattrack maxpoints -1` - disable, always plot all points

## stattrack servers
 - Usage: `?stattrack servers [timespan=1 day, 0:00:00] `
 - Aliases: `servers`

Get server stats.<br/><br/>**Arguments**<br/><br/>`<timespan>` How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>**Examples:**<br/>- `?stattrack servers 3w2d`<br/>- `?stattrack servers 5d`<br/>- `?stattrack servers all`

## stattrack looptime
 - Usage: `?stattrack looptime [timespan=1 day, 0:00:00] `
 - Aliases: `time and loop`

Get my loop time stats.<br/><br/>**Arguments**<br/><br/>`<timespan>` How long to look for, or `all` for all-time data. Defaults to 1 day. Must be<br/>at least 1 hour.<br/><br/>**Examples:**<br/>- `?stattrack looptime 3w2d`<br/>- `?stattrack looptime 5d`<br/>- `?stattrack looptime all`

# stattrackinfo
 - Usage: `?stattrackinfo `



# stattrackloop
 - Usage: `?stattrackloop `



