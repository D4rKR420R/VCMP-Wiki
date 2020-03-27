### onPlayerChat
```Squirrel
function onPlayerChat( player, message )
```

Called when a player sent a message to the public.
> :warning: NOTE: The server has an in-built message system. If you wish to change it, you will have to insert a `return 0;` in the function and call your own function for the ability to customize the message (e.g. color-coding, tags).

#### Arguments

- [CPlayer] *player* - player's instance
- [string] *message* - the message he sent to the chat

#### Returns
> integer - 1 if the message was sent successfully, 0 otherwise (prevents the message from being sent).

#### Example
```Squirrel
function onPlayerChat( player, message )
{
    print( player.Name +": "+ message );
    return 1;
}
```

This will print the message, not only to the server, but the terminal as well!