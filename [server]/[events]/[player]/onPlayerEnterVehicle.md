### onPlayerEnterVehicle
```Squirrel
function onPlayerEnterVehicle( player, vehicle, door )
```

Called when a player successfully enters a vehicle.

#### Arguments

- [CPlayer] *player* - player's instance
- [CVehicle] *vehicle* - vehicle's instance
- [integer] *door* - door ID he enters from

#### Returns
> void

#### Example
```Squirrel
function onPlayerEnterVehicle( player, vehicle, door )
{
    Message( "[#FFFFFF]"+ player.Name +" is entered vehicle ID "+ vehicle.ID +"." );
}
```

We outputted a message, using the `Message` function, that a player entered a vehicle by stating the vehicle's ID using the `.ID` class property.
