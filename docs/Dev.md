# Dev Help

Various development focused utilities!

# mock
 - Usage: `?mock <user> <command> `
 - Restricted to: `BOT_OWNER`
 - Checks: `server_only`

Mock another user invoking a command.<br/><br/>The prefix must not be entered.

# mockmsg
 - Usage: `?mockmsg <user> [content] `
 - Restricted to: `BOT_OWNER`
 - Checks: `server_only`

Dispatch a message event as if it were sent by a different user.<br/><br/>Current message is used as a base (including attachments, embeds, etc.),<br/>the content and author of the message are replaced with the given arguments.<br/><br/>Note: If `content` isn't passed, the message needs to contain embeds, attachments,<br/>or anything else that makes the message non-empty.

# debug (Hybrid Command)
 - Usage: `?debug <code> `
 - Slash Usage: `/debug <code> `
 - Restricted to: `BOT_OWNER`

Evaluate a statement of python code.<br/><br/>The bot will always respond with the return value of the code.<br/>If the return value of the code is a coroutine, it will be awaited,<br/>and the result of that will be the bot's response.<br/><br/>Note: Only one statement may be evaluated. Using certain restricted<br/>keywords, e.g. yield, will result in a syntax error. For multiple<br/>lines or asynchronous code, see ?repl or ?eval.<br/><br/>Environment Variables:<br/>    `ctx`      - the command invocation context<br/>    `bot`      - the bot object<br/>    `channel`  - the current channel object<br/>    `author`   - the command author's member object<br/>    `server`    - the current server object<br/>    `message`  - the command's message object<br/>    `_`        - the result of the last dev command<br/>    `aiohttp`  - the aiohttp library<br/>    `asyncio`  - the asyncio library<br/>    `discord`  - the discord.py library<br/>    `commands` - the redbot.core.commands module<br/>    `cf`       - the redbot.core.utils.chat_formatting module<br/>(See `?setdev getenvironment` for more.)

# eval (Hybrid Command)
 - Usage: `?eval <body> `
 - Slash Usage: `/eval <body> `
 - Restricted to: `BOT_OWNER`

Execute asynchronous code.<br/><br/>This command wraps code into the body of an async function and then<br/>calls and awaits it. The bot will respond with anything printed to<br/>stdout, as well as the return value of the function.<br/><br/>The code can be within a codeblock, inline code or neither, as long<br/>as they are not mixed and they are formatted correctly.<br/><br/>Environment Variables:<br/>    `ctx`      - the command invocation context<br/>    `bot`      - the bot object<br/>    `channel`  - the current channel object<br/>    `author`   - the command author's member object<br/>    `server`    - the current server object<br/>    `message`  - the command's message object<br/>    `_`        - the result of the last dev command<br/>    `aiohttp`  - the aiohttp library<br/>    `asyncio`  - the asyncio library<br/>    `discord`  - the discord.py library<br/>    `commands` - the redbot.core.commands module<br/>    `cf`       - the redbot.core.utils.chat_formatting module<br/>(See `?setdev getenvironment` for more.)

# repl (Hybrid Command)
 - Usage: `?repl `
 - Slash Usage: `/repl `
 - Restricted to: `BOT_OWNER`

Open an interactive REPL.<br/><br/>The REPL will only recognise code as messages which start with a<br/>backtick. This includes codeblocks, and as such multiple lines can be<br/>evaluated.<br/><br/>Use `exit()` or `quit` to exit the REPL session, prefixed with<br/>a backtick so they may be interpreted.<br/><br/>Environment Variables:<br/>    `ctx`      - the command invocation context<br/>    `bot`      - the bot object<br/>    `channel`  - the current channel object<br/>    `author`   - the command author's member object<br/>    `server`    - the current server object<br/>    `message`  - the command's message object<br/>    `_`        - the result of the last dev command<br/>    `aiohttp`  - the aiohttp library<br/>    `asyncio`  - the asyncio library<br/>    `discord`  - the discord.py library<br/>    `commands` - the redbot.core.commands module<br/>    `cf`       - the redbot.core.utils.chat_formatting module

# replpause (Hybrid Command)
 - Usage: `?replpause [toggle=None] `
 - Slash Usage: `/replpause [toggle=None] `
 - Restricted to: `BOT_OWNER`
 - Aliases: `replresume`

Pauses/resumes the REPL running in the current channel.

# bypasscooldowns (Hybrid Command)
 - Usage: `?bypasscooldowns [toggle=None] [time] `
 - Slash Usage: `/bypasscooldowns [toggle=None] [time] `
 - Restricted to: `BOT_OWNER`

Give bot owners the ability to bypass cooldowns.<br/><br/>Does not persist through restarts.

# setdev (Hybrid Command)
 - Usage: `?setdev `
 - Slash Usage: `/setdev `
 - Restricted to: `BOT_OWNER`

Commands to configure Dev.

## setdev resetsetting (Hybrid Command)
 - Usage: `?setdev resetsetting <setting> `
 - Slash Usage: `/setdev resetsetting <setting> `

Reset a setting.

## setdev resetlocals (Hybrid Command)
 - Usage: `?setdev resetlocals `
 - Slash Usage: `/setdev resetlocals `
 - Aliases: `rlocals`

Reset its own locals in evals.

## setdev richtracebacks (Hybrid Command)
 - Usage: `?setdev richtracebacks <value> `
 - Slash Usage: `/setdev richtracebacks <value> `

Use `rich` to display tracebacks.<br/><br/>Default value: False<br/>Dev: <class 'bool'>

## setdev getenvironment (Hybrid Command)
 - Usage: `?setdev getenvironment [show_values=True] `
 - Slash Usage: `/setdev getenvironment [show_values=True] `
 - Aliases: `getenv, getformattedenvironment, and getformattedenv`

Display all Dev environment values.

## setdev showsettings (Hybrid Command)
 - Usage: `?setdev showsettings [with_dev=False] `
 - Slash Usage: `/setdev showsettings [with_dev=False] `

Show all settings for the cog with defaults and values.

## setdev outputmode (Hybrid Command)
 - Usage: `?setdev outputmode <value> `
 - Slash Usage: `/setdev outputmode <value> `

Set the output mode. `repr` is to display the repr of the result. `repr_or_str` is to display in the same way, but a string as a string. `str` is to display the string of the result.<br/><br/>Default value: repr<br/>Dev: typing.Literal['repr', 'repr_or_str', 'str']

## setdev downloaderalreadyagreed (Hybrid Command)
 - Usage: `?setdev downloaderalreadyagreed <value> `
 - Slash Usage: `/setdev downloaderalreadyagreed <value> `

If enabled, Downloader will no longer prompt you to type `I agree` when adding a repo, even after a bot restart.<br/><br/>Default value: False<br/>Dev: <class 'bool'>

## setdev ansiformatting (Hybrid Command)
 - Usage: `?setdev ansiformatting <value> `
 - Slash Usage: `/setdev ansiformatting <value> `

Use the `ansi` formatting for results.<br/><br/>Default value: False<br/>Dev: <class 'bool'>

## setdev uselastlocals (Hybrid Command)
 - Usage: `?setdev uselastlocals <value> `
 - Slash Usage: `/setdev uselastlocals <value> `

Use the last locals for each evals. Locals are only registered for `?eval`, but can be used in other commands.<br/><br/>Default value: False<br/>Dev: <class 'bool'>

## setdev modalconfig (Hybrid Command)
 - Usage: `?setdev modalconfig [confirmation=False] `
 - Slash Usage: `/setdev modalconfig [confirmation=False] `
 - Aliases: `configmodal`

Set all settings for the cog with a Discord Modal.

## setdev autoimports (Hybrid Command)
 - Usage: `?setdev autoimports <value> `
 - Slash Usage: `/setdev autoimports <value> `

Enable or disable auto imports.<br/><br/>Default value: True<br/>Dev: <class 'bool'>

## setdev sendinteractive (Hybrid Command)
 - Usage: `?setdev sendinteractive <value> `
 - Slash Usage: `/setdev sendinteractive <value> `

Send results with `commands.Context.send_interactive`, not a Menu.<br/><br/>Default value: False<br/>Dev: <class 'bool'>

