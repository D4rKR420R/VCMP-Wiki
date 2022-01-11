### ClientMessageToAll
```Squirrel
ClientMessageToAll(message, r, g, b)
```

Sends a pre-colored message to all players in server.

#### Arguments

- [string] *message* - The message to be sent.
- [integer] *r* - R parameter of RGB color.
- [integer] *g* - G parameter of RGB color.
- [integer] *b* - B parameter of RGB color.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerJoin(player)
{
    ClientMessageToAll(player.Name + " has joined the server!", 0, 255, 0);
}
```

> Hexadecimal color codes can be used as well with the message, enclosed with square brackets.