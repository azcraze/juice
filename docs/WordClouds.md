# WordClouds Help

Word Clouds

# wordcloud
 - Usage: `?wordcloud <argv> `
 - Aliases: `wc`
 - Cooldown: `1 per 15.0 seconds`
 - Checks: `server_only`

Generate a wordcloud. Optional arguments are channel, user, and<br/>message limit (capped at 10,000).

# wcset
 - Usage: `?wcset `
 - Restricted to: `MOD`
 - Checks: `server_only`

WordCloud image settings

## wcset colormask
 - Usage: `?wcset colormask [on_off=None] `

Turn color masking on/off

## wcset clearmask
 - Usage: `?wcset clearmask `

Clear image file for masking

## wcset upload
 - Usage: `?wcset upload [url=None] `
 - Restricted to: `BOT_OWNER`

Upload an image mask through Discord

## wcset listmask
 - Usage: `?wcset listmask `

List image files available for masking

## wcset clearwords
 - Usage: `?wcset clearwords `

Clear the excluded word list.<br/>Default excluded list will be used.

## wcset maskfile
 - Usage: `?wcset maskfile <filename> `

Set local image file for masking<br/>- place masks in the cog's data folder/masks/

## wcset exclude
 - Usage: `?wcset exclude <word> `

Add a word to the excluded list.<br/>This overrides the default excluded list!

## wcset maxwords
 - Usage: `?wcset maxwords <count> `

Set maximum number of words to appear in the word cloud<br/>Set to 0 for default (4000).

## wcset bgcolor
 - Usage: `?wcset bgcolor <color> `

Set background color. Use 'clear' for transparent.

