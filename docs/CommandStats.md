# CommandStats Help

Command Statistics.

# cmd
 - Usage: `?cmd [command] `
 - Restricted to: `BOT_OWNER`

Group command for command stats.<br/><br/>This command does not log the issuing command.

## cmd cogstats
 - Usage: `?cmd cogstats [cogname] `

Show command stats per cog, all cogs or per session.

### cmd cogstats session
 - Usage: `?cmd cogstats session [cogname] `

Cog stats in this session.

## cmd repo
 - Usage: `?cmd repo [repo=None] `
 - Restricted to: `BOT_OWNER`
 - Checks: `downloadercheck`

Show command stats per Repo or by repo.

## cmd servers
 - Usage: `?cmd servers `
 - Restricted to: `BOT_OWNER`

Leaderboard of servers by most commands used.

## cmd csv
 - Usage: `?cmd csv `

Return a CSV of all command actions.

## cmd session
 - Usage: `?cmd session [command] `

Session command stats.

## cmd server
 - Usage: `?cmd server [server=None] [command] `
 - Aliases: `server`

Guild Command Stats.

## cmd search
 - Usage: `?cmd search <command> `

Search for command stats

## cmd automated
 - Usage: `?cmd automated `

Automated command stats.<br/><br/>Commands that have `ctx.assume_yes` will qualify as automated.

