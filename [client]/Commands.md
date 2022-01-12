## Client commands
Client-side commands that can be used via the console.

### /q `or` /quit
Disconnect from the server and quit the game.

### /disconnect
Disconnects from the server without quitting the game.

### /reconnect
Reconnect to the server.

### /connect `<ip> <port> [<nickname> [<server password> [<user password>]]]`
Connect to a server. Fields enclosed in square brackets are optional.

> Note: /connect and /reconnect only works if you are disconnected from the server.

### /allowredirect
Allows the server to redirect you to another server.

### /kill
Attempt to commit suicide.

### /screenshot
Takes a screenshot of the game.

### font `[gap] [fontname]`
Changes the font family of console input area.

> Note: This does not change font of the whole console. To change that, you need to use `/setconfig con_fontname [fontname]`.

### /showdebug `[0/1]`
Show or hide client debuglog ingame.

> Note: /showdebug is non-persistent, it will be reset once you quit the game. Use `/setconfig game_showdebug [0/1]` for a persistent change.

### /traceshots
Toggles shot position logging. If enabled, logs the position of shot along with properties of shot building.

> Note: /traceshots is non-persistent, it will be reset once you the quit the game. Only the shots that collide with buildings are logged. Shots from shotguns and snipers are not logged.

### /msg `[playerID] [text]`
Send a private message to a player.

### /infgetweaponid `[weapon_name]`
Get the ID of a weapon from (part of) its name.

### /infgetweaponname `[weapon_id]`
Get the name of a weapon from its ID.

### /infgetvehicleid `[vehicle_name]`
Get the model ID of a vehicle from (part of) its name.

### /infgetmodelname `[model_id]`
Get the name of a vehicle from its model ID.

### /infmodelsearch `[model_name]`
Search object model IDs matching (part of) its model name.

### /vehmodelcount
Displays the count of distinct vehicle models encountered by the client.

### /listconfig
Lists the config values of the client stored in `vcmp_config.txt`.

### /getconfig `[name]`
Gets the value of a specified configuration.

### /setconfig `[name] [value]`
Sets the value of a specified configuration.

> Documentation for client config can be found on [this topic.](https://forum.vc-mp.org/?topic=12.0)

### /recordkey
Displays the key code of the key pressed after using this command.
