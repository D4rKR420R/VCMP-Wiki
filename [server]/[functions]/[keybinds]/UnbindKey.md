### UnbindKey
```Squirrel
UnbindKey(key)
```

Unbinds a previously bound key.

#### Arguments
- [int] *key* - The key index to unbind.

#### Returns
> `bool` false if the key was unbound without an error.

#### Examples
```Squirrel
function onScriptLoad()
{
    lshift <- BindKey(true, 0xA0, 0, 0);
}

function onPlayerCommand(player, command, text)
{
    if(command == "unbind")
    {
        if(!UnbindKey(lshift))
        MessagePlayer("Key unbound successfully", player);
    }
    return 1;
}
```