# Pupper Help

Pet the doggo!

# pets
 - Usage: `?pets `
 - Restricted to: `MOD`
 - Aliases: `pupper`
 - Checks: `server_only`

Manage your pet.

## pets hello
 - Usage: `?pets hello [message] `

Set the pet greeting message.

## pets delete
 - Usage: `?pets delete [amount=0] `

Set how long to wait before deleting the thanks message.<br/>To leave the thanks message with no deletion, use 0 as the amount.<br/>10 is the default.<br/>Max is 5 minutes (300).

## pets cooldown
 - Usage: `?pets cooldown [seconds=None] `

Set the pet appearance cooldown in seconds.<br/><br/>300s/5 minute minimum. Default is 3600s/1 hour.

## pets credits
 - Usage: `?pets credits <min_amt> <max_amt> `

Set the pet credits range on successful petting.

## pets thanks
 - Usage: `?pets thanks [message] `

Set the pet thanks message.

## pets channel
 - Usage: `?pets channel `
 - Restricted to: `MOD`
 - Checks: `server_only`

Channel management for pet appearance.

### pets channel add
 - Usage: `?pets channel add <channel> `

Add a text channel for pets.

### pets channel remove
 - Usage: `?pets channel remove <channel> `

Remove a text channel from petting.

### pets channel addall
 - Usage: `?pets channel addall `

Add all valid channels for the server that the bot can speak in.

### pets channel removeall
 - Usage: `?pets channel removeall `

Remove all petting channels from the list.

## pets toggle
 - Usage: `?pets toggle `

Toggle pets on the server.

