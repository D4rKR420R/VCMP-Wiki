### CreateCheckpoint
```Squirrel
CreateCheckpoint(player, world, isSphere, pos, rgb, radius)
```

### Arguments

- [CPlayer/null] *player* - the player to stream the checkpoint. If you pass a *null* argument, it will stream it to everyone
- [int] *world* - the world you want to stream the checkpoint
- [bool] *isSphere* - *true* to stream a CSphere object
- [Vector] *pos* - the checkpoint's position
- [cRGB] *RGB* - the checkpoint's color
- [int] *radius* - the diameter of the checkpoint

### Returns
> void

### Example
```Squirrel
function onPlayerCommand(player, cmd, arg)
{
  // ...
  if(cmd == "createcheckpoint") {
    // Creates a checkpoint that everyone can access it within the same world
    CreateCheckpoint(null, 0, false, player.Pos, RGB(255, 0, 255), 2);
  }
}
```
