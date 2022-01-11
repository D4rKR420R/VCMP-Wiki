### ClientMessage
```Squirrel
ClientMessage(message, player, r, g, b)
```

Sends a pre-colored message to a specific player.

#### Arguments

- [string] *message* - The message to be sent.
- [CPlayer] *player* - The player to send the message to.
- [integer] *r* - R parameter of RGB color.
- [integer] *g* - G parameter of RGB color.
- [integer] *b* - B parameter of RGB color.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerJoin(player)
{
    ClientMessage("Hi, " + player.Name + ". Welcome to the server!", player, 0, 255, 0);
}
```

> Hexadecimal color codes can be used to color the message string, enclosed with square brackets.

```Squirrel
ClientMessage("[#00FF00]Hi, [#FFFFFF]" + player.Name + "[#00FF00]. Welcome to the server!", player, 255, 255, 255);
```