### onPlayerExitVehicle
```Squirrel
function onPlayerExitVehicle( player, vehicle )
```

#### Arguments

- [CPlayer] *player* - player's instance
- [CVehicle] *vehicle* - vehicle's instance

#### Returns
> void

#### Example
```Squirrel
function onPlayerExitVehicle( player, vehicle )
{
    Message( "[#FFFFFF]"+ player.Name +" is exited vehicle ID "+ vehicle.ID +"." );
}
```

We outputted a message, using the `Message` function, that a player exited a vehicle by stating the vehicle's ID using the `.ID` class property.
