### onPlayerRequestSpawn
```Squirrel
function onPlayerRequestSpawn( player )
```

Called when a player attempts to spawn.

#### Arguments

- [CPlayer] *player* - player's instance

#### Returns

> integer - 1 if the player attempts to spawn, 0 otherwise (prevents the player from spawning)

#### Example
```Squirrel
function onPlayerRequestSpawn( player )
{
    Message( "[#FFFFFFF]"+ player.Name +" will spawn..." );
    return 1;
}
```

It will message the whole server if the player attempts to spawn using `Message`.