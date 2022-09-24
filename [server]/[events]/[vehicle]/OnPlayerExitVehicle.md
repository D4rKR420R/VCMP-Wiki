### OnPlayerExitVehicle
```Squirrel
function OnPlayerExitVehicle(player, vehicle)
```

Called when a player exited the vehicle.

### Arguments

- [CPlayer] *player* - the player's instance, who exited the vehicle
- [CVehicle] *vehicle* - the vehicle's instance

### Returns
> integer - 1 if the player exited the vehicle, otherwise 0

### Example
```Squirrel
function OnPlayerExitVehicle(player, vehicle) {
  Message(player.Name "+ exited "+ GetVehicleNameFromModel(vehicle.Model), player);
}
```

It will output a message when a player exits a vehicle.
