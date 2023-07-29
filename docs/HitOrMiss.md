# HitOrMiss Help

A snowball bot based (but hugely different) cog.<br/><br/>And no it doesn't use slash commands.<br/>*Yet*.

# throw
 - Usage: `?throw <target> <item> `
 - Cooldown: `1 per 5.0 seconds`

Throw an item you own at a user<br/><br/>`item` is the name of the item you want to throw<br/>`target` is the user you want to throw the item at

# heal
 - Usage: `?heal `
 - Cooldown: `1 per 60.0 seconds`

Heal yourself.<br/><br/>Use a medkit if you own one, to increase your hp from anywhere near 1 to 40.

# hitormiss
 - Usage: `?hitormiss `
 - Aliases: `hom`
 - Cooldown: `2 per 5.0 seconds`

Hit or Miss

## hitormiss buy
 - Usage: `?hitormiss buy [amount=None] <item> `
 - Aliases: `purchase`

Buy a Hit Or Miss item for your inventory.<br/><br/>`?buy <item>` to buy 1 of the item.<br/>`?buy <amount> <item>` to buy a specific amount of the item.<br/><br/>where,<br/>`<item>` is the name of the item you want to buy.

## hitormiss stats
 - Usage: `?hitormiss stats [user=None] `
 - Aliases: `profile`

See yours or others Hit Or Miss stats.

## hitormiss shop
 - Usage: `?hitormiss shop `
 - Aliases: `items`

See items available to buy for Hit Or Miss.<br/><br/>User `?buy <item>` to buy an item.

## hitormiss inventory
 - Usage: `?hitormiss inventory `
 - Aliases: `inv`

See all the items that you currently own in Hit Or Miss.

## hitormiss deleteitem
 - Usage: `?hitormiss deleteitem <item> `
 - Restricted to: `BOT_OWNER`
 - Aliases: `remove, delete, and di`

Delete an item from the Hit Or Miss shop that you created.<br/><br/>Owner only command.

## hitormiss leaderboard
 - Usage: `?hitormiss leaderboard [_type=kills] [global_or_local=False] `
 - Aliases: `lb and top`

Show the top players in the Hit Or Miss leaderboard.<br/><br/>There are 6 ways learderboards can be sorted:<br/>- **Throws**: The leaderboard shows the top players who threw the most items.<br/>- **Kills**: The amount of kills users have. (default)<br/>- **Deaths**: The amount of times users have died.<br/>- **Hits**: The amount of times users have hit others.<br/>- **Misses**: The amount of times users have missed a throw.<br/>- **KDR**: The K/D ratio of user's kills to their deaths.<br/>- **All**: TO see all of the above at once. (This type won't be sorted and randomly placed.)<br/><br/>Pass any of the above exactly to the `type` parameter.<br/><br/>The leaderboard is `local` by default (only for the current server).<br/>To show the global leaderboard, pass `true` to the `global_or_local` argument.

## hitormiss createitem
 - Usage: `?hitormiss createitem `
 - Restricted to: `BOT_OWNER`
 - Aliases: `make, create, newitem, and ci`

Create a new Hit Or Miss item.<br/><br/>Owner only command.<br/>This is an interactive questionaire asking you details about the item You want to create.

