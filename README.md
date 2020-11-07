# pocket-utils

CLI tools for interacting with the [Pocket API](https://getpocket.com/developer/docs/overview).

## Requirements
* [jq](https://github.com/stedolan/jq)
* [sqlite-utils](https://github.com/simonw/sqlite-utils)
* env variables required: `POCKET_CONSUMER_KEY`, `POCKET_ACCESS_TOKEN` . No simple solutions :( . You have to go through the [authentication process](https://getpocket.com/developer/docs/authentication)

## Examples

### pocket-get

Powerful and flexible wrapper around the API.
Supports all the params as found [here](https://getpocket.com/developer/docs/v3/retrieve).
Just pass pairs of param-values and will be handled appropriately. 

Example:

`pocket-get state read favorite 1 count 10 detailType complete`

### pocket-get-dump

Just execute `pocket-get-dump` and you'll get a nice `pocket.db` SQLite database,
with all your Pocket data.

### pocket-add

### pocket-add-frontpages

Nicely `cron`-able script to add the front pages (and full edition) of several newspapers to your Pocket.

I personally have this executed every morning. 
Makes it easier and faster to read content directly from Pocket.

### pocket-clear-tags

**DANGER**
This will remove ALL YOUR POCKET TAGS.
Why I need this? 
Don't ask... Keep walking.