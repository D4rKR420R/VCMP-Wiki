### onPlayerSpectate
```Squirrel
function onPlayerSpectate( player, target )
```

Called when a player is spectating another.

#### Arguments

- [CPlayer] *player* - spectator
- [CPlayer] *target* - the one who's spectating at

#### Returns
> void

#### Example
```Squirrel
function onPlayerSpectate( player, target )
{
    MessagePlayer( "[#FFFFFF]"+ player.Name +" is spectating you! Hide your nudes NOW!", player );
    MessagePlayer( "[#FFFFFF] Spectating "+ target.Name +".", player );
}
```

:sweat_smile: I guess privacy is easily invaded...
