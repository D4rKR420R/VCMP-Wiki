### OnSphereEntered
```Squirrel
function OnSphereEntered(player, sphere)
```

Called when a player enters a sphere.

> :warning: NOTE: Be aware that spheres are a little buggy based on my experience with them.

### Arguments

- [CPlayer] *player* - the player who enters the sphere
- [CSphere] *sphere* - the sphere object

### Returns
> void

### Example
```Squirrel
function OnSphereEntered(player, sphere) {
  MessagePlayer("You have entered sphere "+ sphere.ID +".", player);
}
```

This will output the ID of the sphere once a player enters a sphere.
