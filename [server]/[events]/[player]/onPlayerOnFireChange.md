### onPlayerOnFireChange
```Squirrel
function onPlayerFireChange( player, isOnFireNow )
```

Called when a player is caught on fire.

#### Arguments

- [CPlayer] *player* - player's instance
- [integer] *isOnFireNow* - condition

#### Returns
> void

#### Example
```Squirrel
function onPlayerFireChange( player, isOnFireNow )
{
    if( isOnFireNow == 1 ) Message( "[#FFFFFF]"+ player.Name +" is on fire!" );
}
```

In this example, we sent a message to the server using the `Message` function to let everyone know a player is caught on fire.
