### BindKey
```Squirrel
BindKey(press, key1, key2, key3)
```

BindKey allows the server to be informed when a player presses a key or a combination of up to three keys.

#### Arguments
- [bool] *press* - Call the key function on key press or release.
- [int] *key1, key2, key3* - Key codes to bind.

> The key codes can be found [here](https://docs.microsoft.com/en-us/windows/win32/inputdev/virtual-key-codes?redirectedfrom=MSDN).

#### Returns
> `int` The index of keybind.

#### Examples
```Squirrel
function onScriptLoad()
{
    lshift <- BindKey(true, 0xA0, 0, 0);
}

function onKeyDown(player, key)
{
    if(key == lshift)
    {
        MessagePlayer("You pressed the left shift key", player);
    }
}
```