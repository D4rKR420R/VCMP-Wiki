### OnSphereExited
```Squirrel
function onSphereExited(player, sphere)
```

Called when a player exits a sphere.

### Arguments

- [CPlayer] *player* - the player's instance, who exited the sphere
- [CSphere] *sphere* - the sphere's instance

### Returns
> void

### Example
```Squirrel
function OnSphereExited(player, sphere) {
  MessagePlayer("You exited sphere "+ sphere.ID +".", player);
}
```

It will output the sphere's ID when a player exits the sphere.
