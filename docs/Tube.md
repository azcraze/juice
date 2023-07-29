# Tube Help

A YouTube subscription cog<br/><br/>Thanks to mikeshardmind(Sinbad) for the RSS cog as reference

# tube
 - Usage: `?tube `

Post when new videos are added to a YouTube channel

## tube rolemention
 - Usage: `?tube rolemention <channelYouTube> <rolemention> `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Adds a role mention in front of the message

## tube ownerlist
 - Usage: `?tube ownerlist `
 - Restricted to: `BOT_OWNER`

List current subscriptions for all servers

## tube update
 - Usage: `?tube update `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Update feeds and post new videos

## tube setinterval
 - Usage: `?tube setinterval <interval> `
 - Restricted to: `BOT_OWNER`

Set the interval in seconds at which to check for updates<br/><br/>Very low values will probably get you rate limited<br/><br/>Default is 300 seconds (5 minutes)

## tube list
 - Usage: `?tube list `
 - Checks: `server_only`

List current subscriptions

## tube ownerupdate
 - Usage: `?tube ownerupdate `
 - Restricted to: `BOT_OWNER`

Update feeds and post new videos for all servers

## tube unsubscribe
 - Usage: `?tube unsubscribe <channelYouTube> [channelDiscord=None] `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Unsubscribe a Discord channel from a YouTube channel<br/><br/>If no Discord channel is specified and the asAnnouncement flag not set to True, the subscription will be removed from all channels

## tube demo
 - Usage: `?tube demo `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Post the latest video from all subscriptions

## tube setcache
 - Usage: `?tube setcache <size> `
 - Restricted to: `BOT_OWNER`

Set the number of video IDs to cache<br/><br/>Very low values may result in reposting of videos<br/><br/>Default is 500

## tube subscribe
 - Usage: `?tube subscribe <channelYouTube> [channelDiscord=None] [publish=False] `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Subscribe a Discord channel to a YouTube channel<br/><br/>If no discord channel is specified, the current channel will be subscribed<br/><br/>Adding channels by name is not supported at this time. The YouTube channel ID for this can be found in channel links on videos.<br/><br/>For example, to subscribe to the channel Ctrl Shift Face, you would search YouTube for the name, then on one of the videos in the results copy the channel link. It should look like this:<br/>https://www.youtube.com/channel/UCKpH0CKltc73e4wh0_pgL3g<br/><br/>Now take the last part of the link as the channel ID:<br/>`?tube subscribe UCKpH0CKltc73e4wh0_pgL3g`<br/><br/>Setting the `publish` flag will cause new videos to be published to the specified channel. Using this on non-announcement channels may result in errors.

## tube customize
 - Usage: `?tube customize <channelYouTube> [customMessage=False] `
 - Restricted to: `ADMIN`
 - Checks: `server_only`

Add a custom message to videos from a YouTube channel<br/><br/>You can use any keys available in the RSS object in your custom message<br/>by surrounding the key in perecent signs, e.g.:<br/>?tube customize UCKpH0CKltc73e4wh0_pgL3g "It's ya boi %author% wish a fresh vid: %title%\nWatch, like, subscribe, give monies, etc.<br/><br/>You can also remove customization by not specifying any message.

