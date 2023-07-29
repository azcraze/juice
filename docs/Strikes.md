# Strikes Help

Strike users to keep track of misbehaviour.

# strike
 - Usage: `?strike <member> <reason> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Strike a user.

# delstrike
 - Usage: `?delstrike <strike_id> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Remove a single strike by its ID.

# delstrikes
 - Usage: `?delstrikes <member> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Remove all strikes from a member.

# strikes
 - Usage: `?strikes <member> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Show all previous strikes for a user.

# allstrikes
 - Usage: `?allstrikes [num_days=30] `
 - Restricted to: `MOD`
 - Checks: `server_only`

Show all recent individual strikes.<br/><br/>`[num_days]` is the number of past days of strikes to display.<br/>Defaults to 30. When 0, all strikes from the beginning of time<br/>will be counted shown.

# strikecounts
 - Usage: `?strikecounts [num_days=0] [limit=100] [sort_by=count] [sort_order=desc] `
 - Restricted to: `MOD`
 - Checks: `server_only`

Show the strike count for multiple users.<br/><br/>`[num_days]` is the number of past days of strikes to count.<br/>Defaults to 0, which means all strikes from the beginning of<br/>time will be counted.<br/><br/>`[limit]` is the maximum amount of members to show the<br/>strike count for. Defaults to 100.<br/><br/>`[sort_by]` is the column to sort the table by. May be one of<br/>either *count* or *date*. Defaults to *count*.<br/><br/>`[sort_order]` is the order to sort in. It may be one of either<br/>*desc* for descending or *asc* for ascending. Defaults to<br/>*desc*.

