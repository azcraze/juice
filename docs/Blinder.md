# Blinder Help

Create custom roles that remove certain roles and hide channels from users.

# blinder
 - Usage: `?blinder `
 - Checks: `server_only`

Group command for blinder.

## blinder remove
 - Usage: `?blinder remove <role> `
 - Restricted to: `GUILD_OWNER`

Stop a role from being managed by blinder.<br/><br/>Surround the role in quotes if its name requires a space.

## blinder enable
 - Usage: `?blinder enable <role> `

Enable a blinder for yourself.<br/><br/>Surround the role in quotes if its name requires a space.

## blinder edit
 - Usage: `?blinder edit <role> [remove_roles=[]] `
 - Restricted to: `GUILD_OWNER`

Edit what roles are removed by a managed role.<br/><br/>Specify the role to be edited first.<br/>Specify any roles that should be removed when this role is applied after.<br/>Surround each role in quotes if its name requires a space.

## blinder forceenable
 - Usage: `?blinder forceenable <member> <role> `
 - Restricted to: `GUILD_OWNER`

Enable a blinder for a particular member.<br/><br/>Surround the member and role in quotes if their name requires a space.

## blinder add
 - Usage: `?blinder add <role> [remove_roles=[]] `
 - Restricted to: `GUILD_OWNER`

Add a role to be managed by blinder.<br/><br/>Specify the role to be managed first.<br/>Specify any roles that should be removed when this role is applied after.<br/>Surround each role in quotes if its name requires a space.

## blinder toggleall
 - Usage: `?blinder toggleall <role> `
 - Restricted to: `GUILD_OWNER`

Set every role in the server to be removed when this role is applied.<br/><br/>Surround the role in quotes if its name requires a space.

## blinder list
 - Usage: `?blinder list `
 - Restricted to: `GUILD_OWNER`

List the roles currently managed by blinder.

## blinder forcedisable
 - Usage: `?blinder forcedisable <member> <role> `
 - Restricted to: `GUILD_OWNER`

Disable a blinder for a particular member.<br/><br/>Surround the member and role in quotes if their name requires a space.

## blinder disable
 - Usage: `?blinder disable <role> `

Disable a blinder for yourself.<br/><br/>Surround the role in quotes if its name requires a space.

