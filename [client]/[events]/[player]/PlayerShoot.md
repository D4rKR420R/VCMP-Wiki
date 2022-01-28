### Player::PlayerShoot
```Squirrel
function Player::PlayerShoot(player, weapon, hitEntity, hitPosition)
```

Called when a player shoots an entity.

> :warning: Note: This function is not called for shotguns and snipers. And in case of tear gas, explosives and incendiaries, hitEntity and hitPosition are not returned.

#### Arguments
- [CPlayer] *player* - The player who shot.
- [int] *weapon* - ID of the weapon shot.
- [entity] *hitEntity* - The entity (player, building, vehicle) shot. `null` if nothing is hit.
- [Vector] *hitPosition* - The position of collision. `null` if nothing is hit.

#### Returns
> void

#### Example
```Squirrel
function Player::PlayerShoot(player, weapon, hitEntity, hitPosition)
{
    if(hitEntity != null && hitEntity.Type == OBJ_BUILDING)
    {
        Console.Print("Model: " + hitEntity.ModelIndex);
    }
}
```

This will return the model ID of the building shot.