# Unbelievaboat Help

Unbelievaboat Commands.

# unbset
 - Usage: `?unbset `
 - Aliases: `unb-set`
 - Checks: `server_only and check_global_setting_admin`

Manage various settings for Unbelievaboat.

## unbset fine-rate
 - Usage: `?unbset fine-rate <min_or_max> <amount> `
 - Aliases: `finerate`
 - Checks: `server_only and check_global_setting_admin`

Set the min or max fine rate for crimes.

## unbset interest-rate
 - Usage: `?unbset interest-rate <amount> `
 - Aliases: `interestrate`
 - Checks: `server_only and check_global_setting_admin`

Set the interest rate if unable to pay a fine from wallet.

## unbset wallet
 - Usage: `?unbset wallet `
 - Checks: `server_only and check_global_setting_admin`

Wallet Settings.

### unbset wallet max
 - Usage: `?unbset wallet max <amount> `
 - Checks: `server_only and check_global_setting_admin`

Set the max a wallet can have.

### unbset wallet toggle
 - Usage: `?unbset wallet toggle <on_or_off> `
 - Checks: `server_only and check_global_setting_admin`

Toggle the wallet system.

## unbset add-reply
 - Usage: `?unbset add-reply <job> <reply> `
 - Checks: `check_global_setting_admin and server_only`

Add a custom reply for working or crime.<br/><br/>Put {amount} in place of where you want the amount earned to be.

## unbset default-replies
 - Usage: `?unbset default-replies <enable> `
 - Checks: `server_only and check_global_setting_admin`

Whether to use the default replies to work and crime.

## unbset betting
 - Usage: `?unbset betting <min_or_max> <amount> `
 - Checks: `server_only and check_global_setting_admin`

Set the min or max betting amounts.

## unbset del-reply
 - Usage: `?unbset del-reply <job> <id> `
 - Checks: `check_global_setting_admin and server_only`

Delete a custom reply.

## unbset payout
 - Usage: `?unbset payout <job> <min_or_max> <amount> `
 - Checks: `server_only and check_global_setting_admin`

Set the min or max payout for working or crimes.

## unbset list-replies
 - Usage: `?unbset list-replies <job> `
 - Checks: `server_only and check_global_setting_admin`

List custom replies.

## unbset settings
 - Usage: `?unbset settings `
 - Checks: `check_global_setting_admin and server_only`

Current unbelievaboat settings.

## unbset failure-rate
 - Usage: `?unbset failure-rate <job> <amount> `
 - Aliases: `failurerate`
 - Checks: `server_only and check_global_setting_admin`

Set the failure rate for crimes and robbing.

## unbset cooldown
 - Usage: `?unbset cooldown <job> <time> `
 - Checks: `server_only`

Set the cooldown for the work, crime or rob commands. Minimum cooldown is 30 seconds.<br/><br/>The time can be formatted as so `1h30m` etc. Valid times are hours, minutes and seconds.

# cooldowns
 - Usage: `?cooldowns `
 - Checks: `server_only`

List your remaining cooldowns..

# roulette
 - Usage: `?roulette <amount> <bet> `
 - Checks: `roulette_disabled_check and server_only`

Bet on the roulette wheel.<br/><br/>**Current supported bets**:<br/>Single   - Any single number.<br/>Colors   - Red/Black<br/>Halfs    - 1st/2nd half<br/>Even Odd - Even or Odd<br/>Dozens   - 1st/2nd/3rd Dozen (Groups of 12)<br/>Colums   - 1st/2nd/3rd Column.<br/>- This is based on the English version of the roulette wheel.

## roulette start
 - Usage: `?roulette start `
 - Checks: `roulette_disabled_check`

Start a game of roulette.

# rouletteset
 - Usage: `?rouletteset `
 - Restricted to: `ADMIN`
 - Checks: `server_only and check_global_setting_admin`

Manage settings for roulette.

## rouletteset toggle
 - Usage: `?rouletteset toggle `
 - Checks: `server_only and check_global_setting_admin`

Toggle roulette on and off.

## rouletteset payouts
 - Usage: `?rouletteset payouts <type> <payout> `
 - Checks: `server_only, check_global_setting_admin, and roulette_disabled_check`

Set payouts for roulette winnings.<br/><br/>Note: payout is what your prize is multiplied by.<br/>Valid types:<br/>zero<br/>single<br/>color<br/>dozen<br/>odd_or_even<br/>halfs<br/>column

## rouletteset settings
 - Usage: `?rouletteset settings `

Roulette Settings.

## rouletteset time
 - Usage: `?rouletteset time <time> `
 - Checks: `server_only, check_global_setting_admin, and roulette_disabled_check`

Set the time for roulette wheel to start spinning.

# wallet
 - Usage: `?wallet `
 - Checks: `server_only and wallet_disabled_check`

Wallet commands.

## wallet balance
 - Usage: `?wallet balance [user=None] `
 - Checks: `server_only`

Show the user's wallet balance.<br/><br/>Defaults to yours.

## wallet set
 - Usage: `?wallet set <user> <amount> `
 - Checks: `server_only, check_global_setting_admin, and wallet_disabled_check`

Set a users wallet balance.

## wallet leaderboard
 - Usage: `?wallet leaderboard [top=10] `
 - Checks: `server_only`

Print the wallet leaderboard.

# deposit
 - Usage: `?deposit <amount> `
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only and wallet_disabled_check`

Deposit cash from your wallet to your bank.

# withdraw
 - Usage: `?withdraw <amount> `
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `server_only and wallet_disabled_check`

Withdraw cash from your bank to your wallet.

# addmoneyrole
 - Usage: `?addmoneyrole <amount> <role> [destination=wallet] `
 - Restricted to: `ADMIN`
 - Aliases: `addcashrole`
 - Checks: `server_only and check_global_setting_admin`

Add money to the balance of all users within a role.<br/><br/>Valid arguements are 'banks' or 'wallet'.

# removemoneyrole
 - Usage: `?removemoneyrole <amount> <role> [destination=wallet] `
 - Restricted to: `ADMIN`
 - Aliases: `removecashrole`
 - Checks: `server_only and check_global_setting_admin`

Remove money from the bank balance of all users within a role.<br/><br/>Valid arguements are 'banks' or 'wallet'.

# work
 - Usage: `?work `
 - Checks: `server_only`

Work for some cash.

# crime
 - Usage: `?crime `
 - Checks: `server_only`

Commit a crime, more risk but higher payout.

# rob
 - Usage: `?rob <user> `
 - Checks: `wallet_disabled_check and server_only`

Rob another user.

