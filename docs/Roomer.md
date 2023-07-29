# Roomer Help

# roomer
 - Usage: `?roomer `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Roomer settings

## roomer private
 - Usage: `?roomer private `

Change settings for private rooms

### roomer private disable
 - Usage: `?roomer private disable `

Disable private rooms

### roomer private startchannel
 - Usage: `?roomer private startchannel <vc> `

Set a channel that users will join to start using private rooms.<br/>I recommend not allowing talking permissions here.

### roomer private enable
 - Usage: `?roomer private enable `

Enable private rooms

## roomer text
 - Usage: `?roomer text `

Change settings for private text channels.

### roomer text disable
 - Usage: `?roomer text disable `

Enable private text channels.

### roomer text enable
 - Usage: `?roomer text enable `

Enable private text channels.

## roomer auto
 - Usage: `?roomer auto `

Automation settings.

### roomer auto enable
 - Usage: `?roomer auto enable `

Enable automatic voicechannel creation.

### roomer auto name
 - Usage: `?roomer auto name <name> `

Set the name that is used for automatically created voicechannels.

### roomer auto disable
 - Usage: `?roomer auto disable `

Disable automatic voicechannel creation.

### roomer auto channel
 - Usage: `?roomer auto channel `

Manage channels related to automated voicechannels.

#### roomer auto channel remove
 - Usage: `?roomer auto channel remove <channel> `

Remove a start channel used for automatic voicechannels.

#### roomer auto channel add
 - Usage: `?roomer auto channel add <channel> `

Add a start channel used for automatic voicechannels.

# vc
 - Usage: `?vc `
 - Checks: `server_only`

Voicechannel commands.

## vc create
 - Usage: `?vc create [public=False] <name> `

Create a private voicechannel.

## vc hidden
 - Usage: `?vc hidden [true_or_false=True] `
 - Checks: `server_only`

Hide or unhide a voicechannel you own.

## vc join
 - Usage: `?vc join <key> `
 - Checks: `server_only`

Join a private room.

# tc
 - Usage: `?tc `
 - Checks: `server_only`

Textchannel commands.

## tc create
 - Usage: `?tc create [public=False] <name> `

Create a private text channel.

## tc close
 - Usage: `?tc close `

Close the current private text cannel.

## tc join
 - Usage: `?tc join <key> `

Join a private text channel.

