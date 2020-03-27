### onPlayerArmourChange
```Squirrel
function onPlayerArmourChange( player, lastArmour, newArmour )
```

Called when a player's lost or gained armour.

#### Arguments

- [CPlayer] *player* - player's instance
- [integer] *lastArmour* - his previous armour points
- [integer] *newArmour* - his new armour points

#### Returns
> void

#### Example
```Squirrel
function onPlayerArmourChange( player, lastArmour, newArmour )
{
    // Check if the player gained armour
    if( newArmour > lastArmour ) Message( "[#FFFFFF]"+ player.Name +" gained armour!" );
    // Otherwise, he lost
    else Message( "[#FFFFFF]"+ player.Name +" lost armour!" );
}
```

It will send a message to the server, using the `Message` function, whether he lost or gained armor points.
