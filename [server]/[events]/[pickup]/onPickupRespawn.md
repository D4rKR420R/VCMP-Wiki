### onPickupRespawn
```squirrel
function onPickupRespawn(pickup)
```

This function gets called when a pickup respawns. (i.e the auto respawning timer finishes)

#### Arguments

- [integer] *pickup* - The pickup that just respawned.

#### Returns
> Void

#### Example
```squirrel
function onPickupRespawn(pickup)
{
  if(pickup.Model == 408)
  {
    Message("The place "+RobberyPickups[pickup.ID]+" can be robbed again!");
  }
}
```
