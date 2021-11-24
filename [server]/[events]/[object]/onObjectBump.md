### onObjectBump
```Squirrel
function onObjectBump(object,player);
```

This event gets called when an player interacts with an object by touching it. The object must be collidable.

#### Arguments

- [CObject] *object* - The object that's being touched.
- [CPlayer] *player* - The player that's touching the object.

#### Returns
> Void

### Example

```Squirrel
function onObjectBump(object,player)
{
  if(object.Model == ZOMBIE_OBJ_MODEL)
    player.Health -= 1;
}
```
