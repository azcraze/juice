# PayDay Help

Customizable PayDay system<br/><br/>More detailed docs: <https://cogs.yamikaitou.dev/payday.html>

# freecredits
 - Usage: `?freecredits `
 - Checks: `server_only_check`

More options to get free credits

## freecredits hourly
 - Usage: `?freecredits hourly `
 - Checks: `cmd_check`

Get some free currency every hour

## freecredits yearly
 - Usage: `?freecredits yearly `
 - Checks: `cmd_check`

Get some free currency every year (365 days)

## freecredits quarterly
 - Usage: `?freecredits quarterly `
 - Checks: `cmd_check`

Get some free currency every quarter (122 days)

## freecredits monthly
 - Usage: `?freecredits monthly `
 - Checks: `cmd_check`

Get some free currency every month (30 days)

## freecredits weekly
 - Usage: `?freecredits weekly `
 - Checks: `cmd_check`

Get some free currency every week (7 days)

## freecredits daily
 - Usage: `?freecredits daily `
 - Checks: `cmd_check`

Get some free currency every day

## freecredits times
 - Usage: `?freecredits times `
 - Checks: `cmd_all`

Display remaining time for all options

## freecredits all
 - Usage: `?freecredits all `
 - Checks: `cmd_all`

Claim all available freecredits

# pdconfig
 - Usage: `?pdconfig `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Configure the `freecredits` options<br/><br/>More detailed docs: <https://cogs.yamikaitou.dev/payday.html#pdconfig>

## pdconfig settings
 - Usage: `?pdconfig settings `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Print the `freecredits` options

## pdconfig reset
 - Usage: `?pdconfig reset <person> <options> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Forcibly reset the time for a user. WARNING, this will allow the user to claim the credits right away<br/><br/>For <options>, you can provide any combination of the following (seperate by a space to include multiple)<br/>hour<br/>day<br/>week<br/>month<br/>quarter<br/>year

## pdconfig yearly
 - Usage: `?pdconfig yearly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `year`
 - Checks: `is_owner_if_bank_global`

Configure the `yearly` options<br/><br/>Setting this to 0 will disable the command

## pdconfig hourly
 - Usage: `?pdconfig hourly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `hour`
 - Checks: `is_owner_if_bank_global`

Configure the `hourly` options<br/><br/>Setting this to 0 will disable the command

## pdconfig debug
 - Usage: `?pdconfig debug <person> `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Pull some config data for a specific user/member, useful for Support questions

## pdconfig monthly
 - Usage: `?pdconfig monthly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `month`
 - Checks: `is_owner_if_bank_global`

Configure the `monthly` options<br/><br/>Setting this to 0 will disable the command

## pdconfig quarterly
 - Usage: `?pdconfig quarterly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `quarter`
 - Checks: `is_owner_if_bank_global`

Configure the `quarterly` options<br/><br/>Setting this to 0 will disable the command

## pdconfig weekly
 - Usage: `?pdconfig weekly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `week`
 - Checks: `is_owner_if_bank_global`

Configure the `weekly` options<br/><br/>Setting this to 0 will disable the command

## pdconfig streaks
 - Usage: `?pdconfig streaks `
 - Restricted to: `GUILD_OWNER`
 - Checks: `is_owner_if_bank_global`

Configure the `streaks` options

### pdconfig streaks quarterly
 - Usage: `?pdconfig streaks quarterly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `quarter`
 - Checks: `is_owner_if_bank_global`

Configure the `quarterly` streaks value<br/><br/>Setting this to 0 will disable the streak bonus

### pdconfig streaks monthly
 - Usage: `?pdconfig streaks monthly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `month`
 - Checks: `is_owner_if_bank_global`

Configure the `monthly` streaks value<br/><br/>Setting this to 0 will disable the streak bonus

### pdconfig streaks weekly
 - Usage: `?pdconfig streaks weekly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `week`
 - Checks: `is_owner_if_bank_global`

Configure the `weekly` streaks value<br/><br/>Setting this to 0 will disable the streak bonus

### pdconfig streaks hourly
 - Usage: `?pdconfig streaks hourly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `hour`
 - Checks: `is_owner_if_bank_global`

Configure the `hourly` streaks value<br/><br/>Setting this to 0 will disable the streak bonus

### pdconfig streaks percent
 - Usage: `?pdconfig streaks percent <state> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `percentage`
 - Checks: `is_owner_if_bank_global`

Configure streaks to be a percentage or flat amount<br/><br/><state> should be any of these combinations, `on/off`, `yes/no`, `1/0`, `true/false`

### pdconfig streaks daily
 - Usage: `?pdconfig streaks daily <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `day`
 - Checks: `is_owner_if_bank_global`

Configure the `daily` streaks value<br/><br/>Setting this to 0 will disable the streak bonus

### pdconfig streaks yearly
 - Usage: `?pdconfig streaks yearly <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `year`
 - Checks: `is_owner_if_bank_global`

Configure the `yearly` streaks value<br/><br/>Setting this to 0 will disable the streak bonus

## pdconfig daily
 - Usage: `?pdconfig daily <value> `
 - Restricted to: `GUILD_OWNER`
 - Aliases: `day`
 - Checks: `is_owner_if_bank_global`

Configure the `daily` options<br/><br/>Setting this to 0 will disable the command

