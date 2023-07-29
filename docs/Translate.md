# Translate Help

Free Google Translations<br/><br/>Translate some text using Google Translate for free.

# translate
 - Usage: `?translate <to_language> [optional_input] `

Translate the given text to another language (auto-detect source language).<br/><br/>You can provide a message ID/link, some text, or just reply to the original message.

# translatefrom
 - Usage: `?translatefrom <source_language> <to_language> [optional_input] `

Translate the given text from a specified origin language to another language.<br/><br/>You can by provide a message ID/link, some text, or just reply to the original message.

# language
 - Usage: `?language [optional_input] `

Find out what language the given text is in.<br/><br/>You can by provide a message ID/link, some text, or just reply to the original message.

# translateset
 - Usage: `?translateset `
 - Restricted to: `ADMIN`

Translate Settings

## translateset auto
 - Usage: `?translateset auto `

View and set the auto-translation channels for this server.

### translateset auto confidence
 - Usage: `?translateset auto confidence [confidence=None] `

Set the source language confidence threshold in terms of percentage (leave blank to remove).

### translateset auto set
 - Usage: `?translateset auto set <channel> <language> `

Set an auto-translation channel.

### translateset auto remove
 - Usage: `?translateset auto remove <channels> `
 - Aliases: `delete`

Remove an auto-translation channel.

