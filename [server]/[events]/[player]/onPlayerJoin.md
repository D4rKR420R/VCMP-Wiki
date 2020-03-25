### onPlayerJoin
```Squirrel
function onPlayerJoin( player )
```

Called when a player joins the server.

#### Arguments

- CPlayer *player*

#### Returns

- void

#### Example
```Squirrel
function onPlayerJoin( player )
{
    Message( "[#FFFFFF]"+ player.Name +" joined the server." );
}
```

It will message the whole server when a player joins the server using the `Message` function.