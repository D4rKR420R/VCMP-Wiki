### onVehicleRespawn
```Squirrel
function onVehicleRespawn(vehicle)
```
This function gets called when a vehicle respawns.

#### Arguments

- [CVehicle] *vehicle* - The vehicle that's respawning.

#### Returns
> Void

#### Example

```Squirrel
function onVehicleRespawn(vehicle)
{
  if(vehicle.ID == VEH_RHINO)
    vehicle.Health = 3000;
}
```
