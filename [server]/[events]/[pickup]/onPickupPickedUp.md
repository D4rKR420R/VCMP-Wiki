### onPickupPickedUp
```squirrel
function onPickupPickedUp(player, pickup)
```

This event gets called when a player succesfully collects a pickup.

#### Arguments

- [CPlayer] *player* - The player that collected the pickup.
- [integer] *pickup* - The pickup that just got collected.

#### Returns
> Void

### Example
```squirrel
function onPickupPickedUp(pickup,player)
{
  if(pickup.Model == 408)
  {
    player.Money += 100 + rand() % 400;
  }
}
```
