### onPlayerWeaponChange
```Squirrel
function onPlayerWeaponChange( player, lastWep, newWep )
```

Called when a player switches a weapon.

#### Arguments

- [CPlayer] *player* - player's instance
- [integer] *lastWep* - the previous weapon ID
- [integer] *newWep* - the latest weapon ID

#### Returns
> void

#### Example
```Squirrel
function onPlayerWeaponChange( player, lastWep, newWep )
{
    // Block the minigun
    if( newWep == 33 ) player.Disarm(); // Clear all his weapons
}
```

In this example, we prevented anyone in the server from using the mini-gun by disarming his weapons using the `.Disarm()` class member function.
