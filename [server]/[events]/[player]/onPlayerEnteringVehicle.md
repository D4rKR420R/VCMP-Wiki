### onPlayerEnteringVehicle
```Squirrel
function onPlayerEnteringVehicle( player, vehicle, door )
```

Called when a player is entering a vehicle.

#### Arguments

- [CPlayer] *player* - player's instance
- [CVehicle] *vehicle* - the vehicle's instance
- [integer] *door* - door ID he's entering from

#### Returns
> integer - 1 if the player attempts to enter the vehicle, 0 otherwise

#### Example
```Squirrel
function onPlayerEnteringVehicle( player, vehicle, door )
{
    Message( "[#FFFFFF]"+ player.Name +" is entering vehicle ID "+ vehicle.ID +"." );
}
```

We outputted a message, using the `Message` function, that a player was entering a vehicle by stating the vehicle's ID using the `.ID` class property.
