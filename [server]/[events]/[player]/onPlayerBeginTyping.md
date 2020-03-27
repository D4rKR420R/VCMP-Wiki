### onPlayerBeginTyping
```Squirrel
function onPlayerBeginTyping( player )
```

Called when a player is typing in the chat.

#### Arguments

- [CPlayer] *player* - player's instance

#### Returns

> void

#### Example
```Squirrel
function onPlayerBeginTyping( player )
{
    Message( "[#FFFFFF]"+ player.Name +" is currently typing!" );
}
```

Outputs a message, using the `Message` function, when a player is typing.
