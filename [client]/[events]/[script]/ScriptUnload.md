### Script::ScriptUnload
```Squirrel
function Script::ScriptUnload()
```

Called when your main script is unloaded.

#### Arguments
- None

#### Returns
> void

#### Example
```Squirrel
function Script::ScriptUnload()
{
    Console.Print("Script unloaded successfully!");
}
```