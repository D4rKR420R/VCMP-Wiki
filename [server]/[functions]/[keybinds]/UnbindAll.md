### UnbindAll
```Squirrel
UnbindAll()
```

Unbinds all previously bound keys

#### Returns
> void

#### Examples
```Squirrel
function onScriptLoad()
{
    lshift <- BindKey(true, 0xA0, 0, 0);
}

function onPlayerCommand(player, command, text)
{
    if(command == "unbindall")
    {
        UnbindAll();
        MessagePlayer("All keys were unbound", player);
    }
    return 1;
}
```