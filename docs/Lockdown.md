# Lockdown Help

Locks down the current server<br/><br/>To get started, you will need to set up a role to be used when locking<br/>down your server. This role needs to be above all roles it should affect<br/>in the hierarchy as it will be used to determine who should be affected<br/>by the lockdown and this role will be applied to each user. The <br/>role's permissions should be set up to deny access to things the affected <br/>users should not be able to do during a lockdown (such as sending messages, <br/>talking in voice channels, adding reactions, etc).<br/><br/>Once you've set up the role, you can create a new profile with<br/>`[p]lockdownset addprofile` (which takes the role (ID, mention, or name)<br/>as an argument).<br/><br/>Please note that `[p]lockdown` will not work if no profiles are<br/>available as this cog depends on using roles to run a lockdown.

# lockdown
 - Usage: `?lockdown <profile> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Enables lockdown for this server<br/><br/>A profile ID must be specified. To list profiles,<br/>do `?lockdownset listprofiles`

# unlockdown
 - Usage: `?unlockdown `
 - Restricted to: `MOD`
 - Checks: `server_only`

Ends the lockdown for this server

# lockdownset
 - Usage: `?lockdownset `
 - Restricted to: `MOD`
 - Checks: `server_only`

Settings for lockdown

## lockdownset reset
 - Usage: `?lockdownset reset `
 - Restricted to: `GUILD_OWNER`

Removes all lockdown profiles for the current server.

## lockdownset removeprofile
 - Usage: `?lockdownset removeprofile <profile_id> `
 - Restricted to: `ADMIN`

Removes the lockdown profile with the specified IDs<br/><br/>To see a list of profiles and their IDs,<br/>do `?lockdownset listprofiles`

## lockdownset addprofile
 - Usage: `?lockdownset addprofile <role> `
 - Restricted to: `ADMIN`

Adds a lockdown profile.<br/><br/>Role is the role to be applied when triggering a lockdown<br/>with this profile.

## lockdownset listprofiles
 - Usage: `?lockdownset listprofiles `

List all lockdown profiles for the server.

