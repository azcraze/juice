# UpdateRed Help

Update Red from Discord.<br/><br/>To get the most out of this cog, run red with systemd or pm2 on<br/>Linux, or the launcher on Windows, then use the `[p]restart`<br/>command to restart the bot after updating.

# update
 - Usage: `?update [version=stable] <extras> `
 - Restricted to: `BOT_OWNER`
 - Aliases: `updatered`

Update Red with pip.<br/><br/>The optional `version` argument can be set to any one of the<br/>following:<br/> - `stable` (default) - Update to the latest release on PyPI.<br/> - `pre` - Update to the latest pre-release, if available.<br/> - `dev` - Update from source control, i.e. V3/develop on<br/> GitHub.<br/> - Any specific version, e.g. `3.0.0b19`.<br/><br/>You may also specify any number of `extras`, which are extra<br/>requirements you wish to install with Red. For example, to<br/>update mongo requirements with Red, run the command with<br/>`?update <version> mongo`.<br/><br/>Please note that when specifying any invalid arguments, the cog<br/>will naively try to run the update command with those arguments,<br/>possibly resulting in a misleading error message.

# urlupdate
 - Usage: `?urlupdate <url> `
 - Restricted to: `BOT_OWNER`

Update Red directly from a pip-installable URL.

