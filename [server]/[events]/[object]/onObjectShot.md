### onObjectShot
```Squirrel
function onObjectShot(object,player,weapon)
```

This function gets called when a player is shooting an object.

> ⚠️ NOTE: Due to a bug in VC:MP, this function gets called for all rendered players when the object is hit with explosions.

#### Arguments

- [integer] *object* - The object that's being shot. This doesn't work with grenades, flamethrowers and melee weapons.
- [CPlayer] *player* - The player that's shooting the object.
- [integer] *weapon* - The weapon being used.

#### Returns
> Void

#### Example
```Squirrel
onObjectShot(object,player,weapon)
{
  for(int i =0 ; i < 30; i++)
  {
    if(object.ID == Targets[i])
      PlayerStats[player.ID].Score += 1;
  }
}
```
