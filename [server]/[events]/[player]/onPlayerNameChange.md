### onPlayerNameChange
```Squirrel
function onPlayerNameChange( player, oldName, newName )
```

Called when a player changes his name in-game.

> :warning: NOTE: Changing a player's name using the `.Name` property triggers this callback. It does not work for players joining the server.

#### Arguments

- [CPlayer] *player* - player's instance
- [string] *oldName* - previous nickname
- [string] *newName* - new nickname

#### Returns
> void

#### Example
```Squirrel
function onPlayerNameChange( player, oldName, newName )
{
    Message( "[#FFFFFF]"+ oldName +" changed his name to "+ newName +"!" );
}
```

We outputted a message to the server, using the `Message` function, when a player changes his name.
