### KeyBind::OnUp
```Squirrel
function KeyBind::OnUp(key)
```

Called when a keybind is released.

#### Arguments
- [int] *key* - Index of the keybind released.

#### Returns
> void

#### Example
```Squirrel
lshift <- KeyBind(16);
// you can get the keycodes using /recordkey

function KeyBind::OnDown(key)
{
    if(key == lshift)
    {
        Console.Print("You pressed left shift");
    }
}

function KeyBind::OnUp(key)
{
    if(key == lshift)
    {
        Console.Print("You released left shift");
    }
}
```