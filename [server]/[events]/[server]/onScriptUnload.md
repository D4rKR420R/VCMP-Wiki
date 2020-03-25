### onServerUnload
```Squirrel
function onScriptUnload()
```

Called when the server unloads your script.

#### Arguments

- None

#### Returns

> void

#### Example
```Squirrel
function onScriptUnload()
{
    print( "Script unloaded!" ); 
}
```

It will print this message if the script fully unloads.
