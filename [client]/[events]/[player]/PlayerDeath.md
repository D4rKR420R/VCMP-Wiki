### Player::PlayerDeath
```Squirrel
function Player::PlayerDeath(player)
```

Called when a player dies.

#### Arguments
- [CPlayer] *player* - The player who died.


#### Returns
> void

#### Example
```Squirrel
function Player::PlayerDeath(player) 
{
    Console.Print( player.Name + " has died." );
}
```
