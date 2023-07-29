# EmbedUtils Help

Create, post, and store embeds.

# embed
 - Usage: `?embed <channel> <color> <title> <description> `
 - Restricted to: `MOD`
 - Checks: `server_only`

Post a simple embed.<br/><br/>Put the title in quotes if it is multiple words.

## embed fromfile
 - Usage: `?embed fromfile [channel=None] `
 - Aliases: `fromjsonfile and fromdatafile`

Post an embed from a valid JSON file.

## embed edit
 - Usage: `?embed edit <message> <color> <title> <description> `
 - Restricted to: `MOD`

Edit a message sent by JuiceBot's embeds.

### embed edit message
 - Usage: `?embed edit message <source> <target> [index=0] `
 - Aliases: `frommsg and frommessage`

Edit a message's embed using another message's embed.

### embed edit fromfile
 - Usage: `?embed edit fromfile <message> `
 - Aliases: `fromjsonfile and fromdatafile`

Edit a message's embed using a valid JSON file.

### embed edit yamlfile
 - Usage: `?embed edit yamlfile <message> `
 - Aliases: `fromyamlfile`

Edit a message's embed using a valid YAML file.

### embed edit yaml
 - Usage: `?embed edit yaml <message> <data> `
 - Aliases: `fromyaml`

Edit a message's embed using valid YAML.

### embed edit pastebin
 - Usage: `?embed edit pastebin <message> <data> `
 - Aliases: `frompaste`

Edit a message's embed using a pastebin link which contains valid JSON or YAML.

### embed edit json
 - Usage: `?embed edit json <message> <data> `
 - Aliases: `fromjson and fromdata`

Edit a message's embed using valid JSON.

### embed edit store
 - Usage: `?embed edit store <message> <name> `
 - Aliases: `stored`

Edit a message's embed using an embed that's stored on this server.

#### embed edit store global
 - Usage: `?embed edit store global <message> <name> `

Edit a message's embed using an embed that's stored globally.

## embed json
 - Usage: `?embed json [channel=None] <data> `
 - Aliases: `fromjson and fromdata`

Post embeds from valid JSON.

## embed yamlfile
 - Usage: `?embed yamlfile [channel=None] `
 - Aliases: `fromyamlfile`

Post an embed from a valid YAML file.

## embed message
 - Usage: `?embed message <message> [index=0] [channel=None] `
 - Aliases: `frommsg and frommessage`

Post an embed from a message.

## embed download
 - Usage: `?embed download <message> [index=0] `

Download a JSON file for a message's embed.

## embed post
 - Usage: `?embed post <channel> <embed_names> `
 - Aliases: `view, drop, and show`

Post stored embeds.

### embed post global
 - Usage: `?embed post global <channel> <embed_names> `

Post global stored embeds.

## embed global
 - Usage: `?embed global `
 - Restricted to: `BOT_OWNER`

Store embeds for global use.

### embed global json
 - Usage: `?embed global json <name> <locked> <data> `
 - Aliases: `fromjson and fromdata`

Store an embed from valid JSON globally.<br/><br/>The `locked` argument specifies whether the embed should be locked to owners only.

### embed global simple
 - Usage: `?embed global simple <name> <locked> <color> <title> <description> `

Store a simple embed globally.<br/><br/>Put the title in quotes if it is multiple words.<br/>The `locked` argument specifies whether the embed should be locked to owners only.

### embed global remove
 - Usage: `?embed global remove <name> `
 - Aliases: `delete, rm, and del`

Remove a global embed.

### embed global pastebin
 - Usage: `?embed global pastebin <name> <locked> <data> `
 - Aliases: `frompaste`

Store an embed from valid JSON or YAML globally using a pastebin link.<br/><br/>The `locked` argument specifies whether the embed should be locked to owners only.

### embed global list
 - Usage: `?embed global list `

View global embeds.

### embed global lock
 - Usage: `?embed global lock <name> [true_or_false=None] `

Lock/unlock a global embed.

### embed global message
 - Usage: `?embed global message <name> <message> <locked> [index=0] `
 - Aliases: `frommsg and frommessage`

Store an embed from a message globally.<br/><br/>The `locked` argument specifies whether the embed should be locked to owners only.

### embed global info
 - Usage: `?embed global info <name> `

Get info about an embed that is stored globally.

### embed global yamlfile
 - Usage: `?embed global yamlfile <name> <locked> `
 - Aliases: `fromyamlfile`

Store an embed from a valid YAML file globally.<br/><br/>The `locked` argument specifies whether the embed should be locked to owners only.

### embed global fromfile
 - Usage: `?embed global fromfile <name> <locked> `
 - Aliases: `fromjsonfile and fromdatafile`

Store an embed from a valid JSON file globally.<br/><br/>The `locked` argument specifies whether the embed should be locked to owners only.

## embed webhook
 - Usage: `?embed webhook <embeds> `
 - Restricted to: `ADMIN`
 - Checks: `webhook_check`

Send embeds through webhooks.<br/><br/>Running this command with stored embed names will send up to 10 embeds through a webhook.

### embed webhook global
 - Usage: `?embed webhook global <embeds> `

Send global embeds through webhooks.<br/><br/>Running this command with global stored embed names will send up to 10 embeds through a webhook.

### embed webhook json
 - Usage: `?embed webhook json <embeds> `
 - Aliases: `fromjson and fromdata`

Send embeds through webhooks using JSON.

### embed webhook message
 - Usage: `?embed webhook message <message> [index=0] `
 - Aliases: `frommsg and frommessage`

Send embeds through webhooks.

### embed webhook yamlfile
 - Usage: `?embed webhook yamlfile `
 - Aliases: `fromyamlfile`

Send embeds through webhooks, using JSON files.

### embed webhook pastebin
 - Usage: `?embed webhook pastebin <embeds> `
 - Aliases: `frompaste`

Send embeds through webhooks using a pastebin link with valid YAML or JSON.

### embed webhook fromfile
 - Usage: `?embed webhook fromfile `
 - Aliases: `fromjsonfile and fromdatafile`

Send embeds through webhooks, using JSON files.

### embed webhook yaml
 - Usage: `?embed webhook yaml <embeds> `
 - Aliases: `fromyaml`

Send embeds through webhooks using YAML.

## embed pastebin
 - Usage: `?embed pastebin [channel=None] <data> `
 - Aliases: `frompaste`

Post embeds from a pastebin link containing valid JSON or YAML.

## embed info
 - Usage: `?embed info <name> `

Get info about an embed that is stored on this server.

## embed yaml
 - Usage: `?embed yaml [channel=None] <data> `
 - Aliases: `fromyaml`

Post embeds from valid YAML.

## embed store
 - Usage: `?embed store `
 - Restricted to: `MOD`

Store embeds for server use.

### embed store simple
 - Usage: `?embed store simple <name> <color> <title> <description> `

Store a simple embed on this server.<br/><br/>Put the title in quotes if it is multiple words.

### embed store pastebin
 - Usage: `?embed store pastebin <name> <data> `
 - Aliases: `frompaste`

Store an embed from valid JSON or YAML from a pastebin link on this server.

### embed store fromfile
 - Usage: `?embed store fromfile <name> `
 - Aliases: `fromjsonfile and fromdatafile`

Store an embed from a valid JSON file on this server.

### embed store yamlfile
 - Usage: `?embed store yamlfile <name> `
 - Aliases: `fromyamlfile`

Store an embed from a valid YAML file on this server.

### embed store list
 - Usage: `?embed store list `

View stored embeds.

### embed store yaml
 - Usage: `?embed store yaml <name> <data> `
 - Aliases: `fromyaml`

Store an embed from valid YAML on this server.

### embed store download
 - Usage: `?embed store download <embed> `

Download a JSON file for a stored embed.

### embed store remove
 - Usage: `?embed store remove <name> `
 - Aliases: `delete, rm, and del`

Remove a stored embed on this server.

### embed store message
 - Usage: `?embed store message <name> <message> [index=0] `
 - Aliases: `frommsg and frommessage`

Store an embed from a message on this server.

### embed store json
 - Usage: `?embed store json <name> <data> `
 - Aliases: `fromjson and fromdata`

Store an embed from valid JSON on this server.

