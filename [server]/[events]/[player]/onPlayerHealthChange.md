### onPlayerHealthChange
```Squirrel
function onPlayerHealthChange( player, lastHP, newHP )
```

Called when a player gained/lost health.

#### Arguments

- [CPlayer] *player* - player's instance
- [integer] *lastHP* - previous health points
- [integer] *newHP* - latest health points

#### Returns
> void

#### Example
```Squirrel
function onPlayerHealthChange( player, lastHP, newHP )
{
    // Check if the player gained HP
    if( newHP > lastHP ) Message( "[#FFFFFF]"+ player.Name +" gained HP!" );
    // Otherwise, he lost
    else Message( "[#FFFFFF]"+ player.Name +" lost HP!" );
}
```

It will send a message to the server, using the `Message` function, whether he lost or gained health points.
