### KeyBind::OnDown
```Squirrel
function KeyBind::OnDown(key)
```

Called when a keybind is pressed.

#### Arguments
- [int] *key* - Index of the keybind pressed.

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