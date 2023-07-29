# RunCode Help

A cog to compile and run codes in some languages! Use `[p]setruncode listlanguages` to get a list of all the available languages.

# runcode (Hybrid Command)
 - Usage: `?runcode [verbose=False] [language=None] [parameters=None] [code] `
 - Slash Usage: `/runcode [verbose=False] [language=None] [parameters=None] [code] `
 - Aliases: `executecode`

Run a code in a langage, with Wandbox API.<br/><br/>Arguments:<br/>- `verbose`: Without this mode, only the programme output will be sent, without any additional information. In case of an error, it will be used automatically.<br/>- `language`: If not specified, the command will try to "guess" with the file extension or Discord Markdown syntax.<br/>- `parameters`: Optional option to send with the request. `engine:1/cpython-3.10.2`, `input:<input>`, `compiler_options:option1|option2|option3` and `runtime_options:option1|option2|option3`.<br/>- `code`: May be normal code, but also an attached file, or a link from [pastebin](https://pastebin.com), [Github gist](https://gist.github.com) or another "raw" website.<br/>          If you use a link, your command must end with this syntax: `link=<link>` (no space around `=`). You may also not provide it and upload an attachment instead.

# runtio (Hybrid Command)
 - Usage: `?runtio <verbose> <language> [parameters=None] [code] `
 - Slash Usage: `/runtio <verbose> <language> [parameters=None] [code] `
 - Aliases: `tiorun`

Run a code in a langage, with Tio API.<br/><br/>Arguments:<br/>- `verbose`: Without this mode, only the programme output will be sent, without any additional information. In case of an error, it will be used automatically.<br/>- `language`: If not specified, the command will try to "guess" with the file extension or Discord Markdown syntax.<br/>- `parameters`: Optional option to send with the request. `inputs:input1|input2|input3`, `compiler_flags:flag1|flag2|flag3`, `command_line_options:option1|option2|option3` and `args:arg1|arg2|arg3`.<br/>- `code`: May be normal code, but also an attached file, or a link from [pastebin](https://pastebin.com), [Github gist](https://gist.github.com) or another "raw" website.<br/>          If you use a link, your command must end with this syntax: `link=<link>` (no space around `=`). You may also not provide it and upload an attachment instead.

# setruncode (Hybrid Command)
 - Usage: `?setruncode `
 - Slash Usage: `/setruncode `

View RunCode options.

## setruncode listengines (Hybrid Command)
 - Usage: `?setruncode listengines <language> `
 - Slash Usage: `/setruncode listengines <language> `

Shows a list of all the available engines for a specified language, only for Wandbox API.<br/><br/>Arguments:<br/>- `language`: The language name.

## setruncode listextensions (Hybrid Command)
 - Usage: `?setruncode listextensions `
 - Slash Usage: `/setruncode listextensions `

Lists all the languages extensions.

## setruncode listlanguages (Hybrid Command)
 - Usage: `?setruncode listlanguages <api> `
 - Slash Usage: `/setruncode listlanguages <api> `

Shows a list of all the available languages, or Wandbox or Tio API.

## setruncode listidentifiers (Hybrid Command)
 - Usage: `?setruncode listidentifiers `
 - Slash Usage: `/setruncode listidentifiers `

Lists all the languages identifiers recognized by the bot, only for Wandbox API.

