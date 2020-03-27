### onPlayerCrouchChange
```Squirrel
function onPlayerCrouchChange( player, isCrouchingNow )
```

Called when a player crouches or stands up.

#### Arguments

- [CPlayer] *player* - player's instance
- [integer] *isCrouchingNow* - the condition of his stance

#### Returns
> void

#### Example
```Squirrel
function onPlayerCrouchChange( player, isCrouchingNow )
{
    if( isCrouchingNow == true ) Message( "[#FFFFFF]"+ player.Name +" is crouching." );
    else Message( "[#FFFFFF]"+ player.Name +" stands." );
}
```

This will message the server his stance, using the `Message` function.
