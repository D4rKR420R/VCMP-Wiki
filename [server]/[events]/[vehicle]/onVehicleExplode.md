### onVehicleExplode

```Squirrel
function onVehicleExplode( vehicle )
```


This event is called by the server when a vehicle blows up.
#### Arguments

- [CVehicle] *vehicle* - The vehicle that was destroyed.

#### Returns
> Void

### Example

```Squirrel
function onVehicleExplode(vehicle)
{
  Message(""+vehicle.ID+" blew up");
}
```
