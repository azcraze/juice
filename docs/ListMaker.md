# ListMaker Help

Make lists to store data.

# listmaker
 - Usage: `?listmaker `

Group command for ListMaker.

## listmaker header
 - Usage: `?listmaker header <list_name> [text=None] `

Set the text to be used as a header for a list.<br/><br/>Wrap anything that requires spaces in quotes.<br/>The text `{date}` will be replaced by the date the list was last updated.

## listmaker role
 - Usage: `?listmaker role <list_name> <role_id> `

Toggle if a role_id should be allowed to edit a list.<br/><br/>Wrap the list name in quotes if it requires spaces.

## listmaker add
 - Usage: `?listmaker add <list_name> <values> `

Add a row of data to a list.<br/><br/>Specify the list name first and the data for each column after.<br/>Wrap anything that requires spaces in quotes.<br/>Multiple rows can be added at once by continuing to specify rows.<br/><br/>Example:<br/>`?listmaker add "My friends" "Robert Smith" 26`

## listmaker list
 - Usage: `?listmaker list [show_all=False] `

List the existing listmaker lists.<br/><br/>Also shows the user id of the author of each list.<br/>Use the parameter `show_all` to see all lists.

## listmaker remove
 - Usage: `?listmaker remove <list_name> <row_number> `

Remove a row of data from a list.<br/><br/>Specify the list name first and the row number after.<br/>Wrap the list name in quotes if it requires spaces.<br/><br/>Example:<br/>`?listmaker remove "My friends" 3`

## listmaker sort
 - Usage: `?listmaker sort <list_name> [column_name=None] [reverse=False] `

Set the list to be sorted by a particular column.<br/><br/>Wrap anything that requires spaces in quotes.<br/>Use the parameter `reverse` to sort the other way.

## listmaker create
 - Usage: `?listmaker create <list_name> <column_names> `

Create a new list.<br/><br/>Specify the list name first and the name of each column after.<br/>Wrap any names that require spaces in quotes.<br/><br/>Example:<br/>`?listmaker create "My friends" name age`

## listmaker show
 - Usage: `?listmaker show <list_name> [show_index=False] `

View the data of a list.<br/><br/>Wrap the list name in quotes if it requires spaces.<br/>Use the parameter `show_index` to enable list indexes.<br/><br/>Example:<br/>`?listmaker show "My friends"`

## listmaker delete
 - Usage: `?listmaker delete <list_name> `

Delete a list.<br/><br/>This deletes the list and all of its contents permanently.<br/>Wrap the list name in quotes if it requires spaces.<br/><br/>Example:<br/>`?listmaker delete "My friends"`

