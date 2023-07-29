# ModRoles Help

Allow moderators to assign configured roles to users.

# assignrole
 - Usage: `?assignrole <role> <member> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Assign a role to a member.<br/><br/>NOTE: The role is case sensitive!

# unassignrole
 - Usage: `?unassignrole <role> <member> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Unassign a role from a member.<br/><br/>NOTE: The role is case sensitive!

# modroles
 - Usage: `?modroles `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Settings for assignable roles.

## modroles remove
 - Usage: `?modroles remove <role> `

Remove assignable role.

## modroles list
 - Usage: `?modroles list `

List assignable roles.

## modroles targets
 - Usage: `?modroles targets `

Settings about allowed targets.

### modroles targets allowbots
 - Usage: `?modroles targets allowbots [enabled=None] `

Allow to assign roles to bots with `?assignrole`<br/><br/>Leave empty to check current settings.

### modroles targets toprole
 - Usage: `?modroles targets toprole [enabled=None] `

Enable/disable top role check.<br/><br/>When enabled, this will only allow user to assign roles to users<br/>with lower top role than theirs.<br/><br/>Leave empty to check current settings.

## modroles add
 - Usage: `?modroles add <role> `

Add assignable role.

