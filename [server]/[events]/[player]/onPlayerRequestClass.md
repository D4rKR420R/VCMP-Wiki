### onPlayerRequestClass
```Squirrel
function onPlayerRequestClass( player, classID, team, skin )
```

Called when a player scrolls through the team selection screen.

#### Arguments

- [CPlayer] *player*
- [integer] *classID*
- [integer] *team*
- [integer] *skin*

#### Returns

> integer - 1 when the player scrolls through the list of pedestrians, 0 otherwise

#### Example
```Squirrel
function onPlayerRequestClass( player, classID, team, skin )
{
    Announce( "Class ID: "+ classID.tostring(), player, 3 );
}
```

It will announce a big text in your screen when you select a team using `Announce`.