# GetDocs Help

A cog to get and display some documentations in Discord! Use `[p]listsources` to get a list of all the available sources.

# getdocs (Hybrid Command)
 - Usage: `?getdocs [source=None] [query] `
 - Slash Usage: `/getdocs [source=None] [query] `
 - Aliases: `getdoc, docs, and doc`

View rich documentation for a specific node/query.<br/><br/>The name must be exact, or else rtfm is invoked instead.<br/><br/>Arguments:<br/>- `source`: The name of the documentation to use. Defaults to the one configured with `?setgetdocs defaultsource`.<br/>- `query`: The documentation node/query. (`random` to get a random documentation)

# rtfm (Hybrid Command)
 - Usage: `?rtfm [source=None] [limit=10] [with_std=False] [query] `
 - Slash Usage: `/rtfm [source=None] [limit=10] [with_std=False] [query] `
 - Aliases: `rtfd`

Show all items matching your search.<br/><br/>Arguments:<br/>- `source`: The name of the documentation to use. Defaults to the one configured with `?setgetdocs defaultsource`.<br/>- `limit`: The limit of objects to be sent.<br/>- `with_std`: Also display links to non-API documentation.<br/>- `query`: Your search. (`events` to get all dpy events, for `discord.py`, `redbot` and `pylav` source only)

# listsources (Hybrid Command)
 - Usage: `?listsources [_sorted=False] [status=available] `
 - Slash Usage: `/listsources [_sorted=False] [status=available] `
 - Aliases: `listdocsources, listrtfmsources, and listsource`

Shows a list of all sources, those that are available or those that are disabled.

# setgetdocs (Hybrid Command)
 - Usage: `?setgetdocs `
 - Slash Usage: `/setgetdocs `
 - Restricted to: `BOT_OWNER`

Commands to configure GetDocs.

## setgetdocs getdebugloopsstatus (Hybrid Command)
 - Usage: `?setgetdocs getdebugloopsstatus `
 - Slash Usage: `/setgetdocs getdebugloopsstatus `

Get an embed to check loops status.

## setgetdocs enablesources (Hybrid Command)
 - Usage: `?setgetdocs enablesources <sources> `
 - Slash Usage: `/setgetdocs enablesources <sources> `
 - Aliases: `enablesource`

Enable Documentations source(s).

## setgetdocs modalconfig (Hybrid Command)
 - Usage: `?setgetdocs modalconfig [confirmation=False] `
 - Slash Usage: `/setgetdocs modalconfig [confirmation=False] `
 - Aliases: `configmodal`

Set all settings for the cog with a Discord Modal.

## setgetdocs disablesources (Hybrid Command)
 - Usage: `?setgetdocs disablesources <sources> `
 - Slash Usage: `/setgetdocs disablesources <sources> `
 - Aliases: `disablesource`

Disable Documentations source(s).

## setgetdocs defaultsource (Hybrid Command)
 - Usage: `?setgetdocs defaultsource <value> `
 - Slash Usage: `/setgetdocs defaultsource <value> `

Set the documentations source.<br/><br/>Default value: discord.py<br/>Dev: <class 'getdocs.getdocs.SourceConverter'>

## setgetdocs stats (Hybrid Command)
 - Usage: `?setgetdocs stats `
 - Slash Usage: `/setgetdocs stats `

Show stats about all documentations sources.

## setgetdocs showsettings (Hybrid Command)
 - Usage: `?setgetdocs showsettings [with_dev=False] `
 - Slash Usage: `/setgetdocs showsettings [with_dev=False] `

Show all settings for the cog with defaults and values.

## setgetdocs caching (Hybrid Command)
 - Usage: `?setgetdocs caching <value> `
 - Slash Usage: `/setgetdocs caching <value> `

Enable or disable Documentations caching when loading the cog.<br/><br/>If the option is disabled, a web request will be executed when the command `?getdocs` is run only for the searched item.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setgetdocs resetsetting (Hybrid Command)
 - Usage: `?setgetdocs resetsetting <setting> `
 - Slash Usage: `/setgetdocs resetsetting <setting> `

Reset a setting.

