# Simulator Help

Designates a channel that will send automated messages mimicking your friends using Markov chains. They will have your friends' avatars and nicknames too!<br/>Please use the `[p]simulator info` command for more information.

# simulator
 - Usage: `?simulator `
 - Aliases: `sim`

Main simulator command. Use me!

## simulator set
 - Usage: `?simulator set `

Set up your simulator.

### simulator set commentdelay
 - Usage: `?simulator set commentdelay <chance> `
 - Restricted to: `BOT_OWNER`

Messages will be sent randomly during simulated conversations according to this value in seconds.

### simulator set conversationdelay
 - Usage: `?simulator set conversationdelay <minutes> `
 - Restricted to: `BOT_OWNER`

Simulated conversations will occur randomly according to this value in minutes.

### simulator set showsettings
 - Usage: `?simulator set showsettings `

Show the current simulator settings

### simulator set inputchannels
 - Usage: `?simulator set inputchannels <channels> `
 - Restricted to: `BOT_OWNER`

Set a series of channels that will feed the simulator.

### simulator set outputchannel
 - Usage: `?simulator set outputchannel <channel> `
 - Restricted to: `BOT_OWNER`

Set the channel the simulator will run in.

### simulator set inputrole
 - Usage: `?simulator set inputrole <role> `
 - Restricted to: `BOT_OWNER`

Members must have this role to participate in the simulator.

## simulator info
 - Usage: `?simulator info `
 - Aliases: `help`

How this works

## simulator start
 - Usage: `?simulator start `
 - Restricted to: `BOT_OWNER`

Start the simulator in the configured channel.

## simulator count
 - Usage: `?simulator count <word> [user=None] `

Count instances of a word, globally or for a user

## simulator feed
 - Usage: `?simulator feed [days=None] `
 - Restricted to: `BOT_OWNER`

Feed past messages into the simulator from the configured channels from scratch.

## simulator stop
 - Usage: `?simulator stop `
 - Restricted to: `BOT_OWNER`

Stop the simulator.

## simulator stats
 - Usage: `?simulator stats [user=None] `

Statistics about the simulator, globally or for a user

# dontsimulateme
 - Usage: `?dontsimulateme `

Excludes you from your messages being read and analyzed by the simulator.

