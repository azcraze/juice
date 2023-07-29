# NotSoBot Help

Rewrite of many NotSoBot commands to work on RedBot V3

# magik
 - Usage: `?magik [urls=None] [scale=2] [scale_msg=] `
 - Aliases: `imagemagic, imagemagick, magic, magick, cas, and liquid`
 - Cooldown: `2 per 20.0 seconds`

Apply magik to an image.

# gmagik
 - Usage: `?gmagik [urls=None] [frame_delay=1] `
 - Cooldown: `1 per 20.0 seconds`

Attempt to do magik on a gif

# caption
 - Usage: `?caption [urls=None] [text=Caption] [color=white] [size=40] [x=0] [y=0] `

Add caption to an image<br/><br/>`[urls]` are the image urls or users or previous images in chat to add a caption to.<br/>`[text=Caption]` is the text to caption on the image.<br/>`[color=white]` is the color of the text.<br/>`[size=40]` is the size of the text<br/>`[x=0]` is the height the text starts at between 0 and 100% where 0 is the top and 100 is the bottom of the image.<br/>`[y=0]` is the width the text starts at between 0 and 100% where 0 is the left and 100 is the right of the image.

# triggered
 - Usage: `?triggered [urls=None] `
 - Cooldown: `1 per 5.0 seconds`

Generate a Triggered GIF for a user or image

# aesthetics
 - Usage: `?aesthetics <text> `
 - Aliases: `aes`

Returns inputed text in aesthetics

# ascii
 - Usage: `?ascii <text> `
 - Aliases: `expand`
 - Cooldown: `1 per 5.0 seconds`

Convert text into ASCII

# iascii
 - Usage: `?iascii [urls=None] `
 - Cooldown: `1 per 5.0 seconds`
 - Checks: `NotSoBot`

Generate an ascii art image of last image in chat or from URL

# gascii
 - Usage: `?gascii [urls=None] `
 - Cooldown: `1 per 10.0 seconds`
 - Checks: `NotSoBot`

Gif to ASCII

# rip
 - Usage: `?rip [name=None] [text] `

Generate tombstone image with name and optional text

# merge
 - Usage: `?merge [vertical=True] <urls> `
 - Cooldown: `1 per 5.0 seconds`

Merge/Combine Two Photos<br/><br/>`[vertical=True]` `true` or `false` to merge vertically.<br/>`[urls]` The Image URL's you want to merge together. If not supplied<br/>images are searched from message history.

# emojify
 - Usage: `?emojify <txt> `

Replace characters in text with emojis

# jpeg
 - Usage: `?jpeg [urls=None] [quality=1] `
 - Aliases: `needsmorejpeg, jpegify, and magik2`
 - Cooldown: `2 per 5.0 seconds`

Add more JPEG to an Image<br/><br/>Needs More JPEG!<br/>`[urls]` is optional, if not provided will search chat for a valid image.<br/>`[quality]` is the quality of the new jpeg image to make

# vw
 - Usage: `?vw [urls=None] [txt] `
 - Aliases: `vaporwave, vape, and vapewave`
 - Cooldown: `2 per 5.0 seconds`

Add vaporwave flavours to an image

# minecraftachievement
 - Usage: `?minecraftachievement <txt> `
 - Aliases: `achievement`

Generate a Minecraft Achievement

# watermark
 - Usage: `?watermark [urls=None] [mark=None] [x=0] [y=0] [transparency=0] `
 - Aliases: `wm`

Add a watermark to an image<br/><br/>`[urls]` are the image urls or users or previous images in chat to add a watermark to.<br/>`[mark]` is the image to use as the watermark. By default the brazzers icon is used.<br/>`[x=0]` is the height the watermark will be at between 0 and 100% where 0 is the top and 100 is the bottom of the image.<br/>`[y=0]` is the width the watermark will be at between 0 and 100% where 0 is the left and 100 is the right of the image.<br/>`[transparency=0]` is a value from 0 to 100 which determines the percentage the watermark will be transparent.

# glitch
 - Usage: `?glitch [urls=None] [iterations=None] [amount=None] [seed=None] `
 - Aliases: `jpglitch`
 - Cooldown: `2 per 5.0 seconds`

Glitch a gif or png

# pixelate
 - Usage: `?pixelate [urls=None] [pixels=9] `
 - Aliases: `pixel`

Pixelate an image

# waaw
 - Usage: `?waaw [urls=None] `
 - Aliases: `magik3 and mirror`
 - Cooldown: `2 per 5.0 seconds`

Mirror an image vertically right to left

# haah
 - Usage: `?haah [urls=None] `
 - Aliases: `magik4 and mirror2`
 - Cooldown: `2 per 5.0 seconds`

Mirror an image vertically left to right

# woow
 - Usage: `?woow [urls=None] `
 - Aliases: `magik5 and mirror3`
 - Cooldown: `2 per 5.0 seconds`

Mirror an image horizontally top to bottom

# hooh
 - Usage: `?hooh [urls=None] `
 - Aliases: `magik6 and mirror4`
 - Cooldown: `2 per 5.0 seconds`

Mirror an image horizontally bottom to top

# flipimg
 - Usage: `?flipimg [urls=None] `

Rotate an image 180 degrees

# flop
 - Usage: `?flop [urls=None] `

Flip an image horizontally

# invert
 - Usage: `?invert [urls=None] `
 - Aliases: `inverse and negate`

Invert the colours of an image

# rotate
 - Usage: `?rotate [degrees=90] [urls=None] `

Rotate image X degrees

