### onVehicleHealthChange
```Squirrel
function onVehicleHealthChange(vehicle,lastHP,newHP);
```

This event is called when the vehicle in question has it's health increased or decreased. (i.e damaged or healed)

> ⚠️ NOTE: Due to a bug in VC:MP vehicle.Health doesn't report values greater than 1000 correctly.

#### Arguments

- [CVehicle] *vehicle*
- [float] *lastHP*
- [float] *newHP*

#### Returns
> Void
