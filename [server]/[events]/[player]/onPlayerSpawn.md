### onPlayerSpawn
```Squirrel
function onPlayerSpawn( player )
```

Called when a player spawns.

#### Arguments

- [CPlayer] *player* - player's instance

#### Returns

> void

#### Example

```Squirrel
function onPlayerSpawn( player )
{
    // Give the player a couple of weapons
    player.SetWeapon( 19, 9999 );
    player.SetWeapon( 26, 9999 );
}
```

This will give the player a *Pump-Action Shotgun* and *M4* with infinite ammo when spawned.
