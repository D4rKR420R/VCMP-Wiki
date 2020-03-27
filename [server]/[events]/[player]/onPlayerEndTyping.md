### onPlayerEndTyping
```Squirrel
function onPlayerEndTyping( player )
```

Called when a player stops typing in the chat.

#### Arguments

- [CPlayer] *player* - player's instance

#### Returns
> void

#### Example
```Squirrel
function onPlayerEndTyping( player )
{
    Message( "[#FFFFFF]"+ player.Name +" is stopped typing!" );
}
```

Outputs a message, using the `Message` function, when a player stopped typing.
