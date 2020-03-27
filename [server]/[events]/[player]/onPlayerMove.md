### onPlayerMove
```Squirrel
function onPlayerMove( player, lastX, lastY, lastZ, newX, newY, newZ )
```

Called when a player moves.

> :warning: NOTE: This callback is called continuosly, so careful what code you run in it, otherwise it could possibly affect your server's performace. Short-hand operations are recommended.

#### Arguments

- [CPlayer] *player* - player's instance
- [float] *lastX* - last X-coordinate
- [float] *lastY* - last Y-coordinate
- [float] *lastZ* - last Z-coordinate
- [float] *newX* - new X-coordinate
- [float] *newY* - new Y-coordinate
- [float] *newZ* - new Z-coordinate

#### Returns
> void