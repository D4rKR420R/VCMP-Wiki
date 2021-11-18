### onVehicleMove

```Squirrel
function onVehicleMove(vehicle, LastX, LastY, LastZ, NewX, NewY, NewZ)
```

This event gets called when the vehicle's position is different compared to the last registered vehicle position in the previous onServerFrame plugin call.

> ⚠️ NOTE: Computationally expensive operations in this event and alike events (onPlayerMove, onServerFrame) may cause lagging.

#### Arguments

- [CVehicle] *vehicle* - Vehicle that moved.
- [float] *lastX* - Last X coordinate.
- [float] *lastY* - Last Y coordinate.
- [float] *lastZ* - Last Z coordinate.
- [float] *NewX* - The new X coordinate of the vehicle.
- [float] *NewY* - The new Y coordinate of the vehicle.
- [float] *NewZ* - The new Z coordinate of the vehicle.

#### Returns
> Void

### Example
```Squirrel
SpeedLimit <- 0.5;

function onVehicleMove(vehicle, LastX, LastY, LastZ, NewX, NewY, NewZ)
{
  local delta = Vector(NewX - LastX,NewY - LastY, NewZ - LastZ);
  if(sqrt(delta.X * delta.X + delta.Y * delta.Y + delta.Z * delta.Z) > SpeedLimit)
  {
    //Car too fast do somethin
  }
}
```
