# MessageCounter Help

# messagestats
 - Usage: `?messagestats `
 - Restricted to: `ADMIN`

Commands for tracking how many messages matched patterns.

## messagestats info
 - Usage: `?messagestats info <word> `

Checks the complete info of a tracked word.

## messagestats notifyme
 - Usage: `?messagestats notifyme <word> `

Whenever the word appears in a message on this server you will receive a DM from this bot.

## messagestats delcounter
 - Usage: `?messagestats delcounter <word> `

Deletes the counter for this word.

## messagestats checkcounter
 - Usage: `?messagestats checkcounter <word> `

Checks how many messages containing this word have been sent since we started counting.

## messagestats dontnotifyme
 - Usage: `?messagestats dontnotifyme <word> `

Turn off the notifyme trigger.

## messagestats dontnotifychannel
 - Usage: `?messagestats dontnotifychannel <channel> <word> `

Turn off the notifychannel trigger.

## messagestats list
 - Usage: `?messagestats list `

Lists all words we are looking for in this server with their stored info.

## messagestats addcounter
 - Usage: `?messagestats addcounter <word> `

Adds a counter for how many times a message with this word has been sent in this server.

## messagestats notifychannel
 - Usage: `?messagestats notifychannel <channel> <word> `

Whenever a message containing this word appears in this server a message is sent to the set channel.

## messagestats resetcounter
 - Usage: `?messagestats resetcounter <word> `

Resets the counter of the word to 0 and the started-counting date to now.

