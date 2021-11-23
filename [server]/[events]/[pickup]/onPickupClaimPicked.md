### onPickupClaimPicked
```squirrel
function onPickupClaimPicked(pickup,player)
```

This function allows a player to pickup a pickup or not.

#### Arguments

- [integer] *pickup* - The pickup that's being attempted to get collected by the player
- [CPlayer] *player* - The player that's attempting to collect the pickup

#### Returns
> Integer - 1 or true if the player claims the pickup, 0 or false otherwise

### Example

```squirrel
function onPickupClaimPicked(pickup,player)
{
  if(pickup.Model == 408 && player.Skin == 1) //Big dollar pickup and the NPC cop skin
    return false;
    
  return true;
}
```
