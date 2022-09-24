### OnPlayerEnterVehicle
```Squirrel
function OnPlayerEnterVehicle(player, vehicle, door)
```

Called when a player successfully entered a vehicle.

### Arguments

- [CPlayer] *player* - player's instance, who entered the vehicle
- [CVehicle] *vehicle* - vehicle's instance
- [int] *door* - the ID of the door, in which the player accessed the vehicle from

### Returns
> integer - 1 if the player successfully entered the vehicle, otherwise 0

### Example
```Squirrel
const TANK_ID = 162;

function OnPlayerEnterVehicle(player, vehicle, door)
{
  // Eject the player out of the seat if he enters a tank
  if(vehicle.ID == TANK_ID) player.Eject();
}
```
