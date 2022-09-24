### OnPlayerEnteringVehicle
```Squirrel
function OnPlayerEnteringVehicle(player, vehicle, door)
```

Called when a player is in the stage on entering the vehicle.

### Arguments

- [CPlayer] *player* - player's instance, who is entering the vehicle
- [CVehicle] *vehicle* - vehicle's instance
- [int] *door* - the ID of the door, in which the player is accessing the vehicle

### Returns
> void

### Example
```Squirrel
function OnPlayerEnteringVehicle(player, vehicle, door) {
  MessagePlayer("You are entering a "+ GetVehicleNameFromModel(vehicle.Model) +" in door #"+ door +".", player);
}
```

It will output a message when a player is about to enter a vehicle.
